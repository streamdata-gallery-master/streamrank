---
swagger: "2.0"
info:
  title: Twilio
  description: Twilio is a cloud communications Infrastructure as a Service(IaaS)
    company based in San Francisco, California. Twilio allows software developers
    to programmatically make and receive phone calls and send and receive text messages
    using its web service APIs. Twilio's services are accessed over HTTP and are billed
    based on usage.
  termsOfService: https://www.twilio.com/legal/tos
  version: v1
host: api.twilio.com
basePath: /2010-04-01/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Accounts/{AccountSid}/SMS/Messages.{format}:
    get:
      summary: GetSMSList
      description: GetSMSList
      operationId: getsmslist
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: format
        description: By default, Twilios REST API returns XML
      responses:
        200:
          description: Successful response
          schema:
            type: array
            items:
              $ref: '#/definitions/Response_Message'
        302:
          description: A common redirect response; you can GET the representation
            at the URI in the Location response header
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        304:
          description: Your client's cached version of the representation is still
            up to date
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        401:
          description: The supplied credentials, if any, are not sufficient to access
            the resource
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        404:
          description: You know this one
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        429:
          description: Your application is sending too many simultaneous requests
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        500:
          description: We couldn't return the representation due to an internal server
            error
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
        503:
          description: We are temporarily unable to return the representation
          schema:
            type: array
            items:
              $ref: '#/definitions/Exception'
      tags:
      - sms messages
definitions:
  Account:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this account.
        type: string
      DateCreated:
        description: The date that this account was created, in GMT in RFC 2822 format
        type: string
      DateUpdated:
        description: The date that this account was last updated, in GMT in RFC 2822
          format.
        type: string
      FriendlyName:
        description: A human readable description of this account, up to 64 characters
          long. By default the FriendlyName is your email address.
        type: string
      Type:
        description: "The type of this account. Either\_Trial\_or\_Full\_if youve
          upgraded."
        type: string
      Status:
        description: "The status of this account. Usually\_active, but can be\_suspended\_or\_closed."
        type: string
      AuthToken:
        description: The authorization token for this account. This token should be
          kept a secret, so no sharing.
        type: string
      Uri:
        description: The URI for this resource, relative to https://api.twilio.com.
        type: string
      SubresourceUris:
        description: The list of subresources under this account.
        type: string
      OwnerAccountSid:
        description: The Sid of the parent account for this account. The OwnerAccountSid
          of a parent account is its own sid.
        type: string
  Application:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT\_RFC 2822format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT\_RFC
          2822format."
        type: string
      FriendlyName:
        description: A human readable descriptive text for this resource, up to 64
          characters long.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that created this application."
        type: string
      ApiVersion:
        description: Requests to this application will start a new TwiML session with
          this API version.
        type: string
      VoiceUrl:
        description: The URL Twilio will request when a phone number assigned to this
          application receives a call.
        type: string
      VoiceMethod:
        description: "The HTTP method Twilio will use when requesting the above\_Url.
          Either\_GET\_or\_POST."
        type: string
      VoiceFallbackUrl:
        description: "The URL that Twilio will request if an error occurs retrieving
          or executing the TwiML requested by\_Url."
        type: string
      VoiceFallbackMethod:
        description: "The HTTP method Twilio will use when requesting the\_VoiceFallbackUrl.
          Either\_GET\_or\_POST."
        type: string
  Address:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this address.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this address."
        type: string
      FriendlyName:
        description: A human-readable description of the address. Maximum 64 characters.
        type: string
      CustomerName:
        description: Your name or business name, or that of your customer.
        type: string
      Street:
        description: The number and street address where you or your customer is located.
        type: string
      City:
        description: The city in which you or your customer is located.
        type: string
      Region:
        description: The state or region in which you or your customer is located.
        type: string
      PostalCode:
        description: The postal code in which you or your customer is located.
        type: string
      IsoCountry:
        description: The ISO country code of your or your customers address.
        type: string
  API_Key:
    properties:
      Sid:
        description: "A 34 character string that uniquely identifies this API Key.
          You will use this as the basic-auth\_user\_when authenticating to the API."
        type: string
      FriendlyName:
        description: A descriptive string for this resource, chosen by your application,
          up to 64 characters long.
        type: string
      Secret:
        description: "The secret your application uses to sign Access Tokens and to
          authenticate to the REST API (you will use this as the basic-auth\_password).\_Note
          that for security reasons, this field is ONLY returned when the API Key
          is first created."
        type: string
      DateCreated:
        description: "The date-time this API Key was created, given as a\_UTC ISO
          8601 Timestamp."
        type: string
      DateUpdated:
        description: "The date-time this API Key was most recently updated, given
          as a\_UTC ISO 8601 Timestamp."
        type: string
  Available_Phone_Number_Local:
    properties:
      FriendlyName:
        description: A nicely-formatted version of the phone number.
        type: string
      PhoneNumber:
        description: "The phone number, in\_E.164\_(i.e. +1) format."
        type: string
      Lata:
        description: "The\_LATA\_of this phone number."
        type: string
      RateCenter:
        description: "The\_rate center\_of this phone number."
        type: string
      Latitude:
        description: The latitude coordinate of this phone number.
        type: string
      Longitude:
        description: The longitude coordinate of this phone number.
        type: string
      Region:
        description: The two-letter state or province abbreviation of this phone number.
        type: string
      PostalCode:
        description: The postal (zip) code of this phone number.
        type: string
      IsoCountry:
        description: "The\_ISO country code\_of this phone number."
        type: string
      Capabilities:
        description: "This is a set of boolean properties that indicate whether a
          phone number can receive calls or messages. Possible capabilities are\_Voice,\_SMS,
          and\_MMSwith each having a value of either\_true\_or\_false."
        type: string
  Available_Phone_Number_Toll_Free:
    properties:
      FriendlyName:
        description: A nicely-formatted version of the phone number.
        type: string
      PhoneNumber:
        description: "The phone number, in\_E.164\_(i.e. +1) format."
        type: string
      IsoCountry:
        description: "The\_ISO country code\_of this phone number."
        type: string
      Capabilities:
        description: "This is a set of boolean properties that indicate whether a
          phone number can receive calls or messages. Possible capabilities are\_Voice,\_SMS,
          and\_MMSwith each having a value of either\_true\_or\_false."
        type: string
      AddressRequirements:
        description: "This indicates whether the phone number requires you or your
          customer to have an\_Address\_registered with Twilio. Possible values are\_none,\_any,\_local,
          or\_foreign."
        type: string
  Available_Phone_Number_Mobile:
    properties:
      FriendlyName:
        description: A nicely-formatted version of the phone number.
        type: string
      PhoneNumber:
        description: "The phone number, in\_E.164\_(i.e. +1) format."
        type: string
      IsoCountry:
        description: "The\_ISO country code\_of this phone number."
        type: string
      Capabilities:
        description: "This is a set of boolean properties that indicate whether a
          phone number can receive calls or messages. Possible capabilities are\_Voice,\_SMS,
          and\_MMSwith each having a value of either\_true\_or\_false."
        type: string
      AddressRequirements:
        description: "This indicates whether the phone number requires you or your
          customer to have an\_Address\_registered with Twilio. Possible values are\_none,\_any,\_local,
          or\_foreign."
        type: string
  Call:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      ParentCallSid:
        description: A 34 character string that uniquely identifies the call that
          created this leg.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for creating this
          call."
        type: string
      To:
        description: "The phone number, SIP address or Client identifier that received
          this call. Phone numbers are in\_E.164\_format (e.g. +16175551212). SIP
          addresses are formated as\_[email\_protected]/*  */. Client identifiers
          are formatted\_client:name."
        type: string
      From:
        description: "The phone number, SIP address or Client identifier that made
          this call. Phone numbers are in\_E.164\_format (e.g. +16175551212). SIP
          addresses are formated as\_[email\_protected]/*  */. Client identifiers
          are formatted\_client:name."
        type: string
      PhoneNumberSid:
        description: If the call was inbound, this is the Sid of the IncomingPhoneNumber
          that received the call. If the call was outbound, it is the Sid of the OutgoingCallerId
          from which the call was placed.
        type: string
      Status:
        description: "A string representing the status of the call. May be\_queued,\_ringing,\_in-progress,\_canceled,\_completed,\_failed,\_busy\_or\_no-answer.
          See Call Status Values below for more information."
        type: string
      StartTime:
        description: "The start time of the call, given as GMT in\_RFC 2822\_format.
          Empty if the call has not yet been dialed."
        type: string
  Call_Feedback:
    properties:
      QualityScore:
        description: "1\_to\_5\_quality score where\_1\_represents imperfect experience
          and\_5\_represents a perfect call."
        type: string
      Issue:
        description: "A list of issues experienced during the call. The issues can
          be:\_imperfect-audio,\_dropped-call,\_incorrect-caller-id,\_post-dial-delay,\_digits-not-captured,\_audio-latency,
          or\_one-way-audio."
        type: string
  Issue:
    properties:
      imperfect-audio:
        description: 'Imperfect audio quality: Choppy, echoed, or garbled audio during
          conversation.'
        type: string
      dropped-call:
        description: 'Dropped call: call initially connected but was dropped.'
        type: string
      incorrect-caller-id:
        description: "Incorrect caller ID: Call connected but caller ID displayed
          \u2018Unknown\u2019 or an incorrect number."
        type: string
      post-dial-delay:
        description: 'Post dial delay: Call connected but there was a long delay between
          dialing the phone number and the start of ringing.'
        type: string
      digits-not-captured:
        description: 'DTMF tones not captured: Failed to capture digit input on phone
          menus.'
        type: string
      unsolicited-call:
        description: 'Unsolicited call: Received telemarketer, wrong number, automated
          or other type of unsolicited call.'
        type: string
      audio-latency:
        description: 'Audio latency: Call participants can hear each other but with
          significant audio delay.'
        type: string
      one-way-audio:
        description: 'One way audio: Only one party could hear the audio during the
          conversation.'
        type: string
  Status:
    properties:
      queued:
        description: The call is ready and waiting in line before going out.
        type: string
      ringing:
        description: The call is currently ringing.
        type: string
      in-progress:
        description: The call was answered and is currently in progress.
        type: string
      canceled:
        description: The call was hung up while it was queued or ringing.
        type: string
      completed:
        description: The call was answered and has ended normally.
        type: string
      busy:
        description: The caller received a busy signal.
        type: string
      failed:
        description: The call could not be completed as dialed, most likely because
          the phone number was non-existent.
        type: string
      no-answer:
        description: The call ended without being answered.
        type: string
  Conference:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this conference.
        type: string
      FriendlyName:
        description: A user provided string that identifies this conference room.
        type: string
      Status:
        description: "A string representing the status of the conference. May be\_in-progress\_or\_completed."
        type: string
      DateCreated:
        description: "The date that this conference was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this conference was last updated, given as GMT
          in\_RFC 2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for creating this
          conference."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com."
        type: string
  Participant:
    properties:
      CallSid:
        description: A 34 character string that uniquely identifies the call that
          is connected to this conference
        type: string
      ConferenceSid:
        description: A 34 character string that identifies the conference this participant
          is in
        type: string
      DateCreated:
        description: The date that this resource was created, given in RFC 2822 format.
        type: string
      DateUpdated:
        description: The date that this resource was last updated, given in RFC 2822
          format.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that created this conference"
        type: string
      Muted:
        description: "true\_if this participant is currently muted.\_false\_otherwise."
        type: string
      StartConferenceOnEnter:
        description: "Was the\_startConferenceOnEnter\_attribute set on this participant
          (true\_or\_false)?"
        type: string
      EndConferenceOnExit:
        description: "Was the\_endConferenceOnExit\_attribute set on this participant
          (true\_orfalse)?"
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com."
        type: string
  Incoming_Phone_Number:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT\_RFC
          2822format."
        type: string
      FriendlyName:
        description: "A human readable descriptive text for this resource, up to 64
          characters long. By default, the\_FriendlyName\_is a nicely formatted version
          of the phone number."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this phone number."
        type: string
      PhoneNumber:
        description: "The incoming phone number. e.g., +16175551212 (E.164\_format)"
        type: string
      ApiVersion:
        description: Calls to this phone number will start a new TwiML session with
          this API version.
        type: string
      VoiceCallerIdLookup:
        description: "Look up the callers caller-ID name from the CNAM database ($0.01
          per look up). Either\_true\_or\_false."
        type: string
      VoiceUrl:
        description: "The URL Twilio will request when this phone number receives
          a call. The VoiceURL will no longer be used if a\_VoiceApplicationSid\_or
          a\_TrunkSidis set."
        type: string
      VoiceMethod:
        description: "The HTTP method Twilio will use when requesting the above\_Url.
          Either\_GET\_or\_POST."
        type: string
  Message:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
      DateSent:
        description: "The date that the message was sent. For incoming messages, this
          is the date that Twilio received the message. The date is given in\_RFC
          2822format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that sent this message."
        type: string
      MessagingServiceSid:
        description: "The unique id of the\_Messaging Service\_used with the message.
          The value will be null if a Messaging Service was not used."
        type: string
      From:
        description: "The phone number (in\_E.164\_format) or\_alphanumeric sender
          ID\_that initiated the message. For incoming messages, this will be the
          remote phone. For outgoing messages, this will be one of your Twilio phone
          numbers or the alphanumeric sender ID used."
        type: string
      To:
        description: "The phone number that received the message in\_E.164\_format.
          For incoming messages, this will be one of your Twilio phone numbers. For
          outgoing messages, this will be the remote phone."
        type: string
      Body:
        description: The text body of the message. Up to 1600 characters long.
        type: string
      NumMedia:
        description: This property indicates the number of media files associated
          with the message. Each message may send up to 10 media files.
        type: string
  Media:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this media."
        type: string
      ParentSid:
        description: The uniqe id of the resource that created the media.
        type: string
      ContentType:
        description: "The default\_mime-type\_of the media, for example\_image/jpeg,\_image/png,
          or\_image/gif"
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Outgoing_Caller_Id:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
      FriendlyName:
        description: "A human readable descriptive text for this resource, up to 64
          characters long. By default, the\_FriendlyName\_is a nicely formatted version
          of the phone number."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this Caller Id."
        type: string
      PhoneNumber:
        description: "The incoming phone number. Formatted with a + and country code
          e.g., +16175551212 (E.164\_format)."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com."
        type: string
  Queue:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this queue.
        type: string
      FriendlyName:
        description: A user-provided string that identifies this queue.
        type: string
      CurrentSize:
        description: The count of calls currently in the queue.
        type: string
      MaxSize:
        description: The upper limit of calls allowed to be in the queue. The default
          is 100. The maximum is 1000.
        type: string
      AverageWaitTime:
        description: The average wait time of the members of this queue in seconds.
          This is calculated at the time of the request.
        type: string
  Member:
    properties:
      CallSid:
        description: A 34 character string that uniquely identifies the call that
          is enqueued.
        type: string
      DateEnqueued:
        description: The date that the member was enqueued, given in RFC 2822 format.
        type: string
      WaitTime:
        description: The number of seconds the member has been in the queue.
        type: string
      Position:
        description: This members current position in the queue.
        type: string
  Recording:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this recording."
        type: string
      CallSid:
        description: The call during which the recording was made.
        type: string
      Duration:
        description: The length of the recording, in seconds.
        type: string
      Price:
        description: "The one-time cost of creating this recording. Example:\_-0.00250"
        type: string
      PriceUnit:
        description: "The currency used in the\_Price\_property. Example:\_USD"
        type: string
      ApiVersion:
        description: The version of the API in use during the recording.
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Short_Code:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT\_RFC
          2822format."
        type: string
      FriendlyName:
        description: "A human readable descriptive text for this resource, up to 64
          characters long. By default, the\_FriendlyName\_is just the short code."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that owns this short code."
        type: string
      ShortCode:
        description: The short code. e.g., 894546.
        type: string
      ApiVersion:
        description: SMSs to this short code will start a new TwiML session with this
          API version.
        type: string
      SmsUrl:
        description: The URL Twilio will request when receiving an incoming SMS message
          to this short code.
        type: string
      SmsMethod:
        description: "The HTTP method Twilio will use when making requests to the\_SmsUrl.
          EitherGET\_or\_POST."
        type: string
      SmsFallbackUrl:
        description: "The URL that Twilio will request if an error occurs retrieving
          or executing the TwiML from\_SmsUrl."
        type: string
  Token:
    properties:
      Username:
        description: The temporary username that uniquely identifies a Token.
        type: string
      Password:
        description: The temporary password that the username will use when authenticating
          with Twilio.
        type: string
      Ttl:
        description: The duration in seconds for which the username and password are
          valid, the default value is 86,400 (24 hours)
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that created this Token."
        type: string
      IceServers:
        description: An array representing the ephemeral credentials and the STUN
          and TURN server URIs.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
  Transcription:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      DateCreated:
        description: "The date that this resource was created, given in\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given in\_RFC
          2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_responsible for this transcription."
        type: string
      Status:
        description: "A string representing the status of the transcription:\_in-progress,\_completedor\_failed."
        type: string
      RecordingSid:
        description: "The unique id of the\_Recording\_this Transcription was made
          of."
        type: string
      Duration:
        description: The duration of the transcribed audio, in seconds.
        type: string
      TranscriptionText:
        description: The text content of the transcription.
        type: string
      Price:
        description: The charge for this transcript in the currency associated with
          the account. Populated after the transcript is completed. Note, this value
          may not be immediately available.
        type: string
      PriceUnit:
        description: "The currency in which\_Price\_is measured, in\_ISO 4127\_format
          (e.g.\_usd,\_eur,\_jpy)."
        type: string
  Usage_Records:
    properties:
      Category:
        description: "The category of usage. See\_Usage Categories\_below."
        type: string
      Description:
        description: A human-readable description of the usage category.
        type: string
      AccountSid:
        description: The Account that accrued the usage.
        type: string
      StartDate:
        description: The first date for which usage is included in this UsageRecord,
          formatted as YYYY-MM-DD. All dates are in GMT.
        type: string
      EndDate:
        description: The last date for which usage is included in this UsageRecord,
          formatted as YYYY-MM-DD. All dates are in GMT.
        type: string
      Usage:
        description: "The amount of usage (e.g. the number of call minutes). This
          is frequently the same as\_Count, but may be different for certain usage
          categories like calls, where\_Count\_represents the number of calls and\_Usage\_represents
          the number of minutes."
        type: string
      UsageUnit:
        description: "The units in which\_Usage\_is measured. For example\_minutes\_for
          calls,\_messagesfor SMS."
        type: string
      Count:
        description: The number of usage events (e.g. the number of calls).
        type: string
      CountUnit:
        description: "The units in which\_Count\_is measured. For example\_calls\_for
          calls,\_messages\_for SMS."
        type: string
      Price:
        description: The total price of the usage, in the currency associated with
          the account.
        type: string
  Usage_Trigger:
    properties:
      Sid:
        description: The triggers unique Sid.
        type: string
      DateCreated:
        description: "The date the trigger was created, given as GMT\_RFC 2822\_format."
        type: string
      DateUpdated:
        description: "The date the trigger was last updated, given as GMT\_RFC 2822\_format."
        type: string
      AccountSid:
        description: The account this trigger monitors.
        type: string
      FriendlyName:
        description: A user-specified, human-readable name for the trigger.
        type: string
      Recurring:
        description: "How this trigger recurs. Empty for non-recurring triggers. One
          of\_daily,\_monthly, or\_yearly\_for recurring triggers. A trigger will
          only fire once during each recurring period. Recurring periods are in GMT."
        type: string
      UsageCategory:
        description: "The usage category the trigger watches. One of the supported\_usage
          categories."
        type: string
      TriggerBy:
        description: "The field in the\_UsageRecord\_that fires the trigger. One of\_count,\_usage,
          or\_price, as described in the\_UsageRecords documentation."
        type: string
      TriggerValue:
        description: The value at which the trigger will fire. Must be a positive
          numeric value.
        type: string
      CurrentValue:
        description: The current value of the field the trigger is watching.
        type: string
  Callback_Url:
    properties:
      AccountSid:
        description: Your Twilio account id. It is 34 characters long, and always
          starts with the letters AC.
        type: string
      UsageTriggerSid:
        description: The unique identifier of the UsageTrigger that fired.
        type: string
      DateFired:
        description: When the UsageTrigger fired, in GMT.
        type: string
      Recurring:
        description: "How the UsageTrigger that fired recurs. Empty for non-recurring
          UsageTriggers. One of\_daily,\_monthly, or\_yearly\_for recurring UsageTriggers."
        type: string
      UsageCategory:
        description: "The usage category the UsageTrigger watches. One of the supported\_usage
          categories."
        type: string
      TriggerBy:
        description: "The field in the\_UsageRecord\_that fires the UsageTrigger.
          One of\_count,\_usage, or\_price\_as described in the\_UsageRecords documentation."
        type: string
      TriggerValue:
        description: The value at which the UsageTrigger will fire.
        type: string
      CurrentUsageValue:
        description: The current value of the usage the UsageTrigger is watching.
        type: string
      UsageRecordUri:
        description: "The URI of the\_UsageRecord\_this UsageTrigger was watching
          when it fired."
        type: string
      IdempotencyToken:
        description: "A random token generated by Twilio, and guaranteed to be unique
          for this particular firing of this UsageTrigger. See\_Best Practices with
          Usage Trigger Callbacks."
        type: string
  Credential:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      AccountSid:
        description: The unique id of the Account that responsible for this resource.
        type: string
      UserName:
        description: "\_"
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Credential_List:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies each CredentialList.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that sent this message."
        type: string
      FriendlyName:
        description: A human readable descriptive text, up to 64 characters long.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Domain:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies the SIP domain
          in Twilio.
        type: string
      FriendlyName:
        description: A human readable descriptive text, up to 64 characters long.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that sent this message."
        type: string
      ApiVersion:
        description: The version of the Twilio API used to process the message.
        type: string
      DomainName:
        description: "The unique address you reserve on Twilio to which you route
          your SIP traffic. Domain names can contain letters, digits, and \u201C-\u201D."
        type: string
      AuthType:
        description: "The types of authentication you have mapped to your domain.
          The possible values are \u201CIP_ACL\u201D and \u201CCREDENTIAL_LIST\u201D.
          If you have both setup for your domain, both will be returned comma delimited.
          If you do not, have one setup for your domain, it will not be able to receive
          any traffic."
        type: string
      VoiceUrl:
        description: The URL Twilio will request when this domain receives a call.
        type: string
      VoiceMethod:
        description: "The HTTP method Twilio will use when requesting the above Url.
          Either\_GET\_or\_POST."
        type: string
      VoiceFallbackUrl:
        description: The URL that Twilio will request if an error occurs retrieving
          or executing the TwiML requested by VoiceUrl.
        type: string
      VoiceFallbackMethod:
        description: "The HTTP method Twilio will use when requesting the VoiceFallbackUrl.
          Either\_GET\_or\_POST."
        type: string
  Ip_Access_Control_List:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that owns this resource."
        type: string
      FriendlyName:
        description: A human readable descriptive text, up to 64 characters long.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Ip_Access_Control_List_Mappings:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      AccountSid:
        description: The unique id of the Account that responsible for this resource.
        type: string
      FriendlyName:
        description: A human readable descriptive text for this resource, up to 64
          characters long.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Ip_Address:
    properties:
      Sid:
        description: A 34 character string that uniquely identifies this resource.
        type: string
      AccountSid:
        description: The unique id of the Account that responsible for this resource.
        type: string
      FriendlyName:
        description: A human readable descriptive text for this resource, up to 64
          characters long.
        type: string
      IpAddress:
        description: An IP address in dotted decimal notation from which you want
          to accept traffic. Any SIP requests from this IP address will be allowed
          by Twilio. IPv4 only supported today.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT in\_RFC
          2822\_format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT in\_RFC
          2822\_format."
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com"
        type: string
  Authorized_Connect_App:
    properties:
      DateCreated:
        description: "The date that this resource was created, given as GMT\_RFC 2822format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT\_RFC
          2822format."
        type: string
      AccountSid:
        description: "The unique id of the\_SubAccount\_this Connect App has access
          to."
        type: string
      Permissions:
        description: "The set of permissions that you have authorized for this Connect
          App. Valid permisisons are\_get-all\_or\_post-all."
        type: string
      ConnectAppSid:
        description: "The unique id of the\_Connect App\_that was authorized."
        type: string
      ConnectAppFriendlyName:
        description: A human readable name for the Connect App.
        type: string
      ConnectAppDescription:
        description: A more detailed human readable description of the Connect App.
        type: string
      ConnectAppCompanyName:
        description: The company name set for this Connect App.
        type: string
      ConnectAppHomepageUrl:
        description: The public URL for this Connect App.
        type: string
      Uri:
        description: "The URI for this resource, relative to\_https://api.twilio.com."
        type: string
  Connect_App:
    properties:
      Sid:
        description: The unique id of this Connect App.
        type: string
      DateCreated:
        description: "The date that this resource was created, given as GMT\_RFC 2822format."
        type: string
      DateUpdated:
        description: "The date that this resource was last updated, given as GMT\_RFC
          2822\_format."
        type: string
      AccountSid:
        description: "The unique id of the\_Account\_that created this ConnectApp."
        type: string
      Permissions:
        description: The set of permissions that your ConnectApp requests.
        type: string
      FriendlyName:
        description: A human readable name for the Connect App.
        type: string
      Description:
        description: A more detailed human readable description of the Connect App.
        type: string
      CompanyName:
        description: The company name set for this Connect App.
        type: string
      HomepageUrl:
        description: The public URL where users can obtain more information about
          this Connect App.
        type: string
      AuthorizeRedirectUrl:
        description: The URL the users browser will redirect to after Twilio authenticates
          the user and obtains authorization for this Connect App.
        type: string
  Response:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
  Exception:
    properties:
      Status:
        description: The HTTP status code for the exception.
        type: string
      Message:
        description: A more descriptive message regarding the exception.
        type: string
      Code:
        description: (Conditional) An error code to find help for the exception.
        type: string
      MoreInfo:
        description: (Conditional) The URL of Twilios documentation for the error
          code.
        type: string
  Response_Application:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      applications:
        description: A list of applications
        type: array
  Response_Account:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      accounts:
        description: A list of accounts.
        type: array
  Response_Address:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      addresses:
        description: A list of accounts.
        type: array
  Response_Connect_App:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      connected_apps:
        description: A list of connected applications.
        type: array
  Response_Available_Phone_Number_Local:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      available_phone_number_local:
        description: A list of available local phone numbers
        type: array
  Response_API_Key:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      api_keys:
        description: A list of api keys.
        type: array
  Response_Available_Phone_Number_Mobile:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      available_phone_numbers_mobile:
        description: A list of available mobile phone numbers.
        type: array
  Response_Authorized_Connect_App:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      authorized_connected_apps:
        description: A list of authorized connected apps.
        type: array
  Response_Call:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      calls:
        description: A list of calls.
        type: array
  Response_Call_Feedback:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      call_feedback:
        description: A list of calls.
        type: array
  Response_Conference:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      conferences:
        description: A list of conferences.
        type: array
  Response_Credential:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      credentials:
        description: A list of credentials
        type: array
  Response_Credential_List:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      credential_list:
        description: A list of credentials.
        type: array
  Response_Domain:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      domains:
        description: A list of domains.
        type: array
  Response_Incoming_Phone_Number:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      incoming_phone_numbers:
        description: A list of accounts.
        type: array
  Response_Ip_Access_Control_List:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      ip_access_control_lists:
        description: A list of ip access control lists.
        type: array
  Response_Ip_Access_Control_List_Mappings:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      ip_access_control_list_mappings:
        description: A list of ip access control list mappings.
        type: array
  Response_Issues:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      issues:
        description: A list of issues.
        type: array
  Response_Media:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      media:
        description: A list of media.
        type: array
  Response_Outgoing_Caller_Id:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      outgoing_caller_id:
        description: A list of outgoing caller ids.
        type: array
  Response_Message:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      messages:
        description: A list of messages.
        type: array
  Response_Participant:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      participants:
        description: A list of participants.
        type: array
  Response_Queue:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      queue:
        description: A list of queu.
        type: array
  Response_ShortCode:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      short_codes:
        description: A list of applications
        type: array
  Response_Status:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      status:
        description: A list of status.
        type: array
  Response_Recording:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      recordings:
        description: A list of recordings.
        type: array
  Response_Member:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      members:
        description: A list of members.
        type: array
  Response_Transcription:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      transcriptions:
        description: A list of transcriptions.
        type: array
  Response_Token:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      tokens:
        description: A list of tokens.
        type: array
  Response_Usage_Records:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      usage_records:
        description: A list of usage records.
        type: array
  Response_Usage_Trigger:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      usage_triggers:
        description: A list of usage triggers.
        type: array
  Response_Callback_Url:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      callback_urls:
        description: A list of callback urls.
        type: array
  Response_Available_Phone_Number_Toll_Free:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      available_phone_number_toll_free:
        description: A list of available toll free numbers..
        type: array
  Response_Ip_Address:
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      ip_addresses:
        description: A list of ip addresses.
        type: array
  Response_Account (Duplicate):
    properties:
      uri:
        description: The URI of the current page.
        type: string
      firstpageuri:
        description: The URI for the first page of this list.
        type: string
      nextpageuri:
        description: The URI for the next page of this list.
        type: string
      previouspageuri:
        description: The URI for the previous page of this list.
        type: string
      page:
        description: The current page number. Zero-indexed, so the first page is 0.
        type: string
      pagesize:
        description: How many items are in each page
        type: string
      accounts:
        description: A list of accounts.
        type: array
x-collection-name: Twilio
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