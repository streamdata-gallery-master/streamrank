---
swagger: "2.0"
info:
  title: Curb Search API
  description: 'The curb search API is a read-only service to describe what you can
    do on a curb.A curb is defined as one side of one roadway, so every street has
    at least twocurbs (those with medians could have four, say).To see the curb search
    API in action and examine example requests and responses, check outour &lt;a href=&quot;https://coord.co/explorer&quot;
    target=&quot;_blank&quot;&gt;curb explorer tool&lt;/a&gt;, which is builtentirely
    on this API!Curbs'' geometries are positioned along the edge of the roadway, meaning
    that curbs meet atthe corners of intersections. Curbs will never cross over each
    other. In general, curbs startand end at intersections, though behavior at ''T''
    intersections, alleys, pedestrian paths,and other crossings will vary by city.##
    How We Model Curb RulesEvery segment of a curb has, at any given time, a **primary
    use** and**permitted uses**. The primary use is what the regulator has defined
    as the desired use of thecurb at that time. The permitted uses comprise everything
    that is allowed, including the primaryuse if any. We distinguish these so that
    we can tell apart areas signed, say, &quot;PASSENGER LOADINGZONE&quot; from those
    signed &quot;NO STANDING&quot; (which may also allow passenger pick-up and drop-off).A
    segment of curb can also have a **vehicle type**. In this case, only vehicles
    of this type areallowed to perform the permitted uses on this segment, though
    other vehicles mayhave a smaller list of permitted uses.For instance an area signed
    &quot;COMMERCIAL VEHICLE LOADING ONLY ALL OTHERS NO STOPPING&quot; would have:  *
    A vehicle type of `commercial`  * A primary use of `load_goods`  * A permitted
    use of `load_passengers`  * No uses in `other_vehicles_permitted`.On the other
    hand, an area signed &quot;TRUCK PARKING ALL OTHERS NO STANDING&quot; might have:  *
    A vehicle type of `truck`  * A primary use of `park`  * Permitted uses of `load_goods`
    and `load_passengers`  * `load_passengers` in `other_vehicles_permitted`.### Uses
    and Vehicle TypesThe different uses are:  * **`park`**: leave a vehicle somewhere
    for a period of time.  * **`load_goods`**: load and unload goods from a vehicle.
    The vehicle may be left unattended for a    few minutes during this process.  *
    **`load_passengers`**: load and unload passengers from a vehicle. The vehicle
    may not be left    unattended during passenger loading.  * **`none`**: If a segment
    has no primary use (e.g., it is signed &quot;NO PARKING&quot;), its primary    use
    will be specified as `none`. It can still have permitted uses (for instance,    in
    most cities, drivers are still allowed to load and unload passengers in &quot;NO
    PARKING&quot;    areas).The different vehicle types are:  * **`all`**: If a segment
    of curb has a vehicle type of `all`, this means that all kinds of    vehicles
    (including private cars) can engage in its permitted uses.  * **`taxi`**: any
    for-hire passenger vehicle. This includes medallion taxis, livery companies, and    ridesharing
    companies like Lyft and Uber.  * **`commercial`**: a vehicle used for transporting
    goods commercially. The exact definition    varies by city, but usually, commercial
    vehicles must have commercial license plates.  * **`truck`**: a large vehicle
    used for transporting goods commercially. The exact definition    varies by city,
    but usually, trucks have three or more axles in addition to meeting the    requirements
    of a commercial vehicle.  * **`motorcycle`**: a two-wheeled motorized vehicle.
    This includes full-sized motorcycles as    well as mopeds.### Geometry and DirectionEvery
    curb has a specific direction, and thus a start and an end. Regardless of the
    direction oftravel, all curbs are oriented to the right of their respective streets.
    This means that if youwalk from the start of the curb to the end, the street will
    be on your left-hand side the wholetime.Each segment has distances, in meters,
    defining their linear position along the curb. These aremeasured from the start
    of the curb. Note that, if you restrict the segments you return usingquery parameters,
    you may not get a given curb''s complete geometry. But querying with norestrictions
    will always return all the segments on a curb. When you do this, the segments
    willalways be connected in both geometry and distance: every subsequent segment
    will start atexactly the point the last one ended, and its `distance_start_meters`
    will be the lastsegment''s `distance_end_meters`. This allows you to reconstruct
    a linear view of any curb andto know what the regulations are at every point.###
    Temporary RulesIn some cities, we have data about temporary changes to parking
    regulations. These can be due toconstruction, events, or other activities that
    use the road. We take these temporary regulationsinto account as soon as we find
    out about them, but not all regulations arrive at the same time,so it''s always
    possible for future temporary regulations to change. Temporary regulations thatare
    in the past will never change.In `time_rules` requests, you don''t have to do
    anything special for temporary regulations: weuse them automatically to compute
    the regulations that apply at the requested time. For`all_rules` requests, you
    can use the `temp_rules_window_start` and `temp_rules_window_end`parameters to
    control the time/date range of the rules we return. We will return any temporaryrule
    that takes effect at any time within this window, even if it is on the edge (for
    instance,a rule that starts before `temp_rules_window_start` and ends within the
    window will bereturned).Temporary rules override **all other rules** on their
    segment for their specified time period.## Getting rules at a particular timeThe
    simplest methods to call are[`bybounds/time_rules`](#reference/0/all-rules-for-curbs-within-a-bounding-box-at-a-particular-time),[`bylocation/time_rules`](#reference/0/rules-at-a-point-in-time-for-curbs-near-a-location),
    and[`bycurb/{id}/time_rules`](#reference/0/rules-at-a-point-in-time-for-a-single-curb).All
    three of these methods take a particular starting time and tell you how long (if
    at all)you can perform any given use at each segment of curb starting at this
    time, and how much itwill cost. In all cases, the response data has the same format:
    a GeoJSON `FeatureCollection`where each feature is a curb segment with its own
    usage information.### Sample request```curl -G &quot;https://api.coord.co/v1/search/curbs/bycurb/bnljOjEwNDMzNQ/time_rules?time=2018-06-12T11:00:00-04:00&amp;access_key=&lt;your_api_key&gt;&quot;```###
    Sample response```{  &quot;features&quot;: [    // ... some features omitted for
    brevity.    {      // Each feature contains the geography of just the portion
    of the curb that it applies to.      &quot;geometry&quot;: {        &quot;coordinates&quot;:
    [          [-73.9775270524428, 40.75197120090719],          [-73.9773964310734,
    40.751917110446385]        ],        &quot;type&quot;: &quot;LineString&quot;      },      &quot;properties&quot;:
    {        &quot;metadata&quot;: {          // The ID of this curb (note that all
    features that are on the same curb have the same          // curb_id.)          &quot;curb_id&quot;:
    &quot;bnljOjEwNDMzNQ&quot;,          // distance_start_meters and distance_end_meters
    represent the distance from the          // beginning of the curb that this feature
    starts/ends at.          &quot;distance_end_meters&quot;: 18.653505116785006,          &quot;distance_start_meters&quot;:
    6.1,          // Additional metadata about this curb.          &quot;end_street_name&quot;:
    &quot;LEXINGTON AVENUE&quot;,          &quot;side_of_street&quot;: &quot;SW&quot;,          &quot;start_street_name&quot;:
    &quot;EAST 42 STREET&quot;,          &quot;street_name&quot;: &quot;EAST 42 STREET&quot;,          &quot;time_zone&quot;:
    &quot;America/New_York&quot;        },        // Using the curb for the purposes
    designated below is free.        &quot;price&quot;: [{&quot;price_per_hour&quot;:
    {&quot;amount&quot;: 0, &quot;currency&quot;: &quot;USD&quot;}}],        // The
    rules for this curb feature are specified by a sign.        &quot;reasons&quot;:
    [&quot;sign&quot;],        &quot;uses&quot;: {          // The only permitted
    use for this part of the curb is loading/unloading passengers.          &quot;permitted&quot;:
    [            {&quot;use&quot;: &quot;load_passengers&quot;, &quot;vehicle_type&quot;:
    &quot;all&quot;}          ],                    // There is no primary use (this
    means that this is signed as NO STANDING rather than          // as a specific
    passenger loading zone).          &quot;use&quot;: &quot;none&quot;,          &quot;vehicle_type&quot;:
    &quot;all&quot;        }      },      &quot;type&quot;: &quot;Feature&quot;    },    {      &quot;geometry&quot;:
    {        &quot;coordinates&quot;: [          [-73.9773964310734, 40.751917110446385],          [-73.97715562215994,
    40.75181739119557],          [-73.97689946982429, 40.75171053502362],          [-73.97624207098005,
    40.75143628919809]        ],        &quot;type&quot;: &quot;LineString&quot;      },      &quot;properties&quot;:
    {        &quot;metadata&quot;: {          &quot;curb_id&quot;: &quot;bnljOjEwNDMzNQ&quot;,          &quot;distance_end_meters&quot;:
    129.7443128858502,          &quot;distance_start_meters&quot;: 18.653505116785006,          &quot;end_street_name&quot;:
    &quot;LEXINGTON AVENUE&quot;,          &quot;side_of_street&quot;: &quot;SW&quot;,          &quot;start_street_name&quot;:
    &quot;EAST 42 STREET&quot;,          &quot;street_name&quot;: &quot;EAST 42 STREET&quot;,          &quot;time_zone&quot;:
    &quot;America/New_York&quot;        },        // Using this curb costs 3 dollars
    and 50 cents per hour.        &quot;price&quot;: [{&quot;price_per_hour&quot;:
    {&quot;amount&quot;: 350, &quot;currency&quot;: &quot;USD&quot;}}],        //
    This curbs rules are specified by signs and parking meter data.        &quot;reasons&quot;:
    [&quot;sign&quot;, &quot;meter&quot;],        &quot;uses&quot;: {          //
    This curb allows parking for commercial vehicles and loading goods/passengers
    for          // any vehicle (commercial or otherwise). Note that in all cases,
    the use ends at           // 2PM (3 hours after the requested time). It turns
    out that this is because the curb          // is signed for three-hour parking,
    but this could have meant that there was, e.g.,          // a &quot;NO STOPPING&quot;
    regulation that takes effect at 2PM.          &quot;permitted&quot;: [            {              &quot;end_time&quot;:
    &quot;2018-06-12T14:00:00.000-04:00&quot;,              &quot;use&quot;: &quot;load_goods&quot;,              &quot;vehicle_type&quot;:
    &quot;all&quot;            },            {              &quot;end_time&quot;:
    &quot;2018-06-12T14:00:00.000-04:00&quot;,              &quot;use&quot;: &quot;load_passengers&quot;,              &quot;vehicle_type&quot;:
    &quot;all&quot;            },            {              &quot;end_time&quot;:
    &quot;2018-06-12T14:00:00.000-04:00&quot;,              &quot;use&quot;: &quot;park&quot;,              &quot;vehicle_type&quot;:
    &quot;commercial&quot;            }          ],          // The primary use case
    for this portion of the curb is commercial vehicle parking          // until 4PM.          &quot;primary_until&quot;:
    &quot;2018-06-12T16:00:00.000-04:00&quot;,          &quot;use&quot;: &quot;park&quot;,          &quot;vehicle_type&quot;:
    &quot;commercial&quot;        }      },      &quot;type&quot;: &quot;Feature&quot;    },    {      &quot;geometry&quot;:
    {        &quot;coordinates&quot;: [          [-73.97624207098005, 40.75143628919809],          [-73.97617870763244,
    40.751409856030875]        ],        &quot;type&quot;: &quot;LineString&quot;      },      &quot;properties&quot;:
    {        &quot;metadata&quot;: {          &quot;curb_id&quot;: &quot;bnljOjEwNDMzNQ&quot;,          &quot;distance_end_meters&quot;:
    135.8443128858502,          &quot;distance_start_meters&quot;: 129.7443128858502,          &quot;end_street_name&quot;:
    &quot;LEXINGTON AVENUE&quot;,          &quot;side_of_street&quot;: &quot;SW&quot;,          &quot;start_street_name&quot;:
    &quot;EAST 42 STREET&quot;,          &quot;street_name&quot;: &quot;EAST 42 STREET&quot;,          &quot;time_zone&quot;:
    &quot;America/New_York&quot;        },        // Because this feature is too close
    to the intersection, it doesn''t permit any uses.        &quot;price&quot;: null,        &quot;reasons&quot;:
    [&quot;intersection&quot;],        &quot;uses&quot;: {          &quot;permitted&quot;:
    null,          &quot;use&quot;: &quot;none&quot;,          &quot;vehicle_type&quot;:
    &quot;all&quot;        }      },      &quot;type&quot;: &quot;Feature&quot;    }  ],  &quot;type&quot;:
    &quot;FeatureCollection&quot;}```## Getting all rules If you want to analyze all
    of a curb''s rules across time, you can call[`bybounds/all_rules`](#reference/0/all-rules-for-curbs-within-a-bounding-box),[`bylocation/all_rules`](#reference/0/all-rules-for-curbs-near-a-location),
    and[`bycurb/{id}/all_rules`]#reference/0/all-rules-for-a-single-curb).These methods
    give you comprehensive information for the relevant curbs, but require you to
    domore work to figure out what a given vehicle can do at a given time. These methods
    return a GeoJSON`FeatureCollection` where each feature is a curb segment with
    its own usage information, but withdifferent properties than the methods that
    take a time parameter.### Sample request```curl -G &quot;https://api.coord.co/v1/search/curbs/bycurb/bnljOjEwNDMzNQ/all_rules?access_key=&lt;your_api_key&gt;&quot;```###
    Sample response```{  &quot;features&quot;: [    // ... some features omitted for
    brevity.    {      // Note that geometry and metadata are structured the same
    in &quot;all_rules&quot; and &quot;time_rules&quot;      // requests.      &quot;geometry&quot;:
    {        &quot;coordinates&quot;: [          [-73.9773964310734, 40.751917110446385],          [-73.97715562215994,
    40.75181739119557],          [-73.97689946982429, 40.75171053502362],          [
    -73.97624207098005, 40.75143628919809]        ],        &quot;type&quot;: &quot;LineString&quot;      },      &quot;properties&quot;:
    {        &quot;metadata&quot;: {          &quot;curb_id&quot;: &quot;bnljOjEwNDMzNQ&quot;,          &quot;distance_end_meters&quot;:
    129.7443128858502,          &quot;distance_start_meters&quot;: 18.653505116785006,          &quot;end_street_name&quot;:
    &quot;LEXINGTON AVENUE&quot;,          &quot;side_of_street&quot;: &quot;SW&quot;,          &quot;start_street_name&quot;:
    &quot;EAST 42 STREET&quot;,          &quot;street_name&quot;: &quot;EAST 42 STREET&quot;,          &quot;time_zone&quot;:
    &quot;America/New_York&quot;        },        // Every feature can have multiple
    rules that apply at different times. There is always        // exactly one rule
    that applies at any one time.        &quot;rules&quot;: [          // Rule 1:
    passenger loading only from 7am-10am and 4pm-7pm Mon-Sat.          {            //
    &quot;other_vehicles_permitted&quot; describes what vehicles not matching &quot;vehicle_type&quot;
    can            // do when this rule applies. It is empty when &quot;vehicle_type&quot;
    is &quot;all&quot;, as it is for            // this rule.            &quot;other_vehicles_permitted&quot;:
    [],            &quot;permitted&quot;: [&quot;load_passengers&quot;],            &quot;price&quot;:
    [{&quot;price_per_hour&quot;: {&quot;amount&quot;: 0, &quot;currency&quot;: &quot;USD&quot;}}],            &quot;primary&quot;:
    &quot;none&quot;,            &quot;reasons&quot;: [&quot;sign&quot;],            &quot;times&quot;:
    [              {                &quot;days&quot;: [1, 2, 3, 4, 5, 6],                &quot;time_of_day_end&quot;:
    &quot;10:00&quot;,                &quot;time_of_day_start&quot;: &quot;07:00&quot;              },              {                &quot;days&quot;:
    [1, 2, 3, 4, 5, 6],                &quot;time_of_day_end&quot;: &quot;19:00&quot;,                &quot;time_of_day_start&quot;:
    &quot;16:00&quot;              }            ],            &quot;vehicle_type&quot;:
    &quot;all&quot;          },          // Rule 2: 3-hour pay parking for commercial
    vehicles from 10am-4pm Mon-Sat.          {            // Any vehicle can stay
    here at most three hours.            &quot;max_duration_h&quot;: 3,            //
    This rule has &quot;vehicle_type&quot; of &quot;commercial&quot;, so &quot;other_vehicles_permitted&quot;            //
    describes what non-commercial vehicles can do while &quot;permitted&quot; describes
    what            // commercial vehicles can do.            &quot;other_vehicles_permitted&quot;:
    [&quot;load_goods&quot;, &quot;load_passengers&quot;],            &quot;permitted&quot;:
    [&quot;park&quot;, &quot;load_goods&quot;, &quot;load_passengers&quot;],            &quot;price&quot;:
    [{&quot;price_per_hour&quot;: {&quot;amount&quot;: 350, &quot;currency&quot;:
    &quot;USD&quot;}}],            // The primary use is parking.            &quot;primary&quot;:
    &quot;park&quot;,            &quot;reasons&quot;: [&quot;sign&quot;, &quot;meter&quot;],            &quot;times&quot;:
    [              {                &quot;days&quot;: [1, 2, 3, 4, 5, 6],                &quot;time_of_day_end&quot;:
    &quot;16:00&quot;,                &quot;time_of_day_start&quot;: &quot;10:00&quot;              }            ],            //
    The primary vehicle type is commercial.            &quot;vehicle_type&quot;: &quot;commercial&quot;          },          //
    Rule 3: free parking all day Sunday, before 7am, after 7pm.          {            &quot;other_vehicles_permitted&quot;:
    [],            &quot;permitted&quot;: [&quot;park&quot;, &quot;load_goods&quot;,
    &quot;load_passengers&quot;],            &quot;price&quot;: [{&quot;price_per_hour&quot;:
    {&quot;amount&quot;: 0, &quot;currency&quot;: &quot;USD&quot;}}],            &quot;primary&quot;:
    &quot;park&quot;,            // reasons is null because free parking is the default
    regulation in the absence of            // any other information.            &quot;reasons&quot;:
    null,              &quot;times&quot;: [              {                &quot;days&quot;:
    [0],                &quot;time_of_day_end&quot;: &quot;24:00&quot;,                &quot;time_of_day_start&quot;:
    &quot;00:00&quot;              },              {                &quot;days&quot;:
    [1, 2, 3, 4, 5, 6],                &quot;time_of_day_end&quot;: &quot;07:00&quot;,                &quot;time_of_day_start&quot;:
    &quot;00:00&quot;              },              {                &quot;days&quot;:
    [1, 2, 3, 4, 5, 6],                &quot;time_of_day_end&quot;: &quot;24:00&quot;,                &quot;time_of_day_start&quot;:
    &quot;19:00&quot;              }            ],            &quot;vehicle_type&quot;:
    &quot;all&quot;          }        ],        // No temporary rules in effect for
    the coming week for this curb segment.        &quot;temporary_rules&quot;: null      },      &quot;type&quot;:
    &quot;Feature&quot;    }  ],  &quot;type&quot;: &quot;FeatureCollection&quot;}```'
  version: 1.0.0
host: api.coord.co
basePath: /v1/search/curbs
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /bylocation/all_rules:
    get:
      summary: Find the rules for curbs near a location.
      description: |-
        Find all of the curbs within a given radius of a particular point, and return all of their
        rules across all times of day, days of the week, times of year, etc
      operationId: get_by_location
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: latitude
        description: Latitude to return results for
        type: string
        format: string
      - in: query
        name: longitude
        description: Longitude to return results for
        type: string
        format: string
      - in: query
        name: radius_km
        description: Distance, in kilometers, from (latitude, longitude) we will return
          results for
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - find
      - rulescurbs
      - near
      - location
definitions:
  BikeLocationFeature:
    properties:
      id:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  BikeLocationFeatureProperties:
    properties:
      is_renting:
        description: This is a default description.
        type: x-summary
      is_returning:
        description: This is a default description.
        type: x-summary
      last_reported:
        description: This is a default description.
        type: x-summary
      lat:
        description: This is a default description.
        type: x-summary
      location_id:
        description: This is a default description.
        type: x-summary
      lon:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      num_bikes_available:
        description: This is a default description.
        type: x-summary
      num_docks_available:
        description: This is a default description.
        type: x-summary
      region_id:
        description: This is a default description.
        type: x-summary
  BikeLocationList:
    properties:
      features:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  Error:
    properties:
      code:
        description: This is a default description.
        type: x-summary
      message:
        description: This is a default description.
        type: x-summary
  FlatFeature:
    properties:
      properties:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  FlatFeatureCollection:
    properties:
      features:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  LatLng:
    properties:
      lat:
        description: This is a default description.
        type: x-summary
      lng:
        description: This is a default description.
        type: x-summary
  LineString:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  Money:
    properties:
      amount:
        description: This is a default description.
        type: x-summary
      currency:
        description: This is a default description.
        type: x-summary
  MultiPolygonGeometry:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  NamedLocation:
    properties:
      name:
        description: This is a default description.
        type: x-summary
  ParkingCondition:
    properties:
      absolute_time_end_ts:
        description: This is a default description.
        type: x-summary
      absolute_time_start_ts:
        description: This is a default description.
        type: x-summary
      day_times:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
  ParkingLocationMetadata:
    properties:
      address:
        description: This is a default description.
        type: x-summary
      amenities:
        description: This is a default description.
        type: x-summary
      created:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      last_updated:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      online_access_type:
        description: This is a default description.
        type: x-summary
      operator_name:
        description: This is a default description.
        type: x-summary
      time_zone:
        description: This is a default description.
        type: x-summary
  ParkingRate:
    properties:
      absolute_end_time:
        description: This is a default description.
        type: x-summary
      absolute_start_time:
        description: This is a default description.
        type: x-summary
      arrival_window_end:
        description: This is a default description.
        type: x-summary
      arrival_window_start:
        description: This is a default description.
        type: x-summary
      days:
        description: This is a default description.
        type: x-summary
      departure_window_end:
        description: This is a default description.
        type: x-summary
      departure_window_start:
        description: This is a default description.
        type: x-summary
      max_duration_m:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      rate_type:
        description: This is a default description.
        type: x-summary
  ParkingRule:
    properties:
      price_mechanism:
        description: This is a default description.
        type: x-summary
      prices:
        description: This is a default description.
        type: x-summary
      spaces_total:
        description: This is a default description.
        type: x-summary
  ParkingSession:
    properties:
      billing_info:
        description: This is a default description.
        type: x-summary
      end_time:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      location_id:
        description: This is a default description.
        type: x-summary
      resource_id:
        description: This is a default description.
        type: x-summary
      start_time:
        description: This is a default description.
        type: x-summary
      user_id:
        description: This is a default description.
        type: x-summary
  Partner:
    properties:
      api_access_enabled:
        description: This is a default description.
        type: x-summary
      api_keys:
        description: This is a default description.
        type: x-summary
      creation_time:
        description: This is a default description.
        type: x-summary
      first_login_time:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      is_provider:
        description: This is a default description.
        type: x-summary
      name:
        description: This is a default description.
        type: x-summary
      prod_enabled:
        description: This is a default description.
        type: x-summary
      secret_keys:
        description: This is a default description.
        type: x-summary
      whitelisted_domains:
        description: This is a default description.
        type: x-summary
  Plate:
    properties:
      state:
        description: This is a default description.
        type: x-summary
      text:
        description: This is a default description.
        type: x-summary
  PointGeometry:
    properties:
      coordinates:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  PricingRule:
    properties:
      end_duration_h:
        description: This is a default description.
        type: x-summary
      minimum_hours_paid:
        description: This is a default description.
        type: x-summary
      start_duration_h:
        description: This is a default description.
        type: x-summary
  RedemptionInfo:
    properties:
      barcode:
        description: This is a default description.
        type: x-summary
  Reservation:
    properties:
      duration_m:
        description: This is a default description.
        type: x-summary
      id:
        description: This is a default description.
        type: x-summary
      lease_expiration_time:
        description: This is a default description.
        type: x-summary
      plate:
        description: This is a default description.
        type: x-summary
      resource_id:
        description: This is a default description.
        type: x-summary
      start_time:
        description: This is a default description.
        type: x-summary
      status:
        description: This is a default description.
        type: x-summary
      user_id:
        description: This is a default description.
        type: x-summary
      vehicle_id:
        description: This is a default description.
        type: x-summary
  SegmentMetadata:
    properties:
      curb_id:
        description: This is a default description.
        type: x-summary
      distance_end_meters:
        description: This is a default description.
        type: x-summary
      distance_start_meters:
        description: This is a default description.
        type: x-summary
      end_street_name:
        description: This is a default description.
        type: x-summary
      side_of_street:
        description: This is a default description.
        type: x-summary
      start_street_name:
        description: This is a default description.
        type: x-summary
      street_name:
        description: This is a default description.
        type: x-summary
      time_zone:
        description: This is a default description.
        type: x-summary
  SegmentRule:
    properties:
      max_duration_h:
        description: This is a default description.
        type: x-summary
      other_vehicles_permitted:
        description: This is a default description.
        type: x-summary
      permitted:
        description: This is a default description.
        type: x-summary
      price:
        description: This is a default description.
        type: x-summary
      reasons:
        description: This is a default description.
        type: x-summary
      times:
        description: This is a default description.
        type: x-summary
  SegmentRulesFeature:
    properties:
      type:
        description: This is a default description.
        type: x-summary
  SegmentRulesFeatureCollection:
    properties:
      features:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  SegmentRulesFeatureProperties:
    properties:
      rules:
        description: This is a default description.
        type: x-summary
      temporary_rules:
        description: This is a default description.
        type: x-summary
  SegmentTemporaryRule:
    properties:
      end:
        description: This is a default description.
        type: x-summary
      max_duration_h:
        description: This is a default description.
        type: x-summary
      other_vehicles_permitted:
        description: This is a default description.
        type: x-summary
      permitted:
        description: This is a default description.
        type: x-summary
      price:
        description: This is a default description.
        type: x-summary
      reasons:
        description: This is a default description.
        type: x-summary
      start:
        description: This is a default description.
        type: x-summary
  SegmentTimeFeature:
    properties:
      type:
        description: This is a default description.
        type: x-summary
  SegmentTimeFeatureCollection:
    properties:
      features:
        description: This is a default description.
        type: x-summary
      type:
        description: This is a default description.
        type: x-summary
  SegmentTimeFeatureProperties:
    properties:
      price:
        description: This is a default description.
        type: x-summary
      reasons:
        description: This is a default description.
        type: x-summary
  SegmentTimeUse:
    properties:
      end_time:
        description: This is a default description.
        type: x-summary
  SegmentTimeUses:
    properties:
      permitted:
        description: This is a default description.
        type: x-summary
      primary_until:
        description: This is a default description.
        type: x-summary
  TimeAndDay:
    properties:
      day_of_year_end:
        description: This is a default description.
        type: x-summary
      day_of_year_start:
        description: This is a default description.
        type: x-summary
      days:
        description: This is a default description.
        type: x-summary
      time_of_day_end:
        description: This is a default description.
        type: x-summary
      time_of_day_start:
        description: This is a default description.
        type: x-summary
  TimeRange:
    properties:
      max_value:
        description: This is a default description.
        type: x-summary
      min_value:
        description: This is a default description.
        type: x-summary
  TimestampedLatLng:
    properties:
      lat:
        description: This is a default description.
        type: x-summary
      lng:
        description: This is a default description.
        type: x-summary
      timestamp:
        description: This is a default description.
        type: x-summary
  TransactionRequirements:
    properties:
      jwt_claims:
        description: This is a default description.
        type: x-summary
      linked_account:
        description: This is a default description.
        type: x-summary
      users_api_fields:
        description: This is a default description.
        type: x-summary
  Vehicle:
    properties:
      license_plate:
        description: This is a default description.
        type: x-summary
x-collection-name: Coord
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---