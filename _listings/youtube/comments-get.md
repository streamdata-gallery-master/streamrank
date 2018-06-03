---
swagger: "2.0"
info:
  title: YouTube
  description: YouTube allows users to upload, view, rate, share, add to favorites,
    report, comment on videos, and subscribe to other users. It offers a wide variety
    of user-generated and corporate media videos. Available content includes video
    clips, TV show clips, music videos, short and documentary films, audio recordings,
    movie trailers, live streams, and other content such as video blogging, short
    original videos, and educational videos. Most of the content on YouTube is uploaded
    by individuals, but media corporations including CBS, the BBC, Vevo, and Hulu
    offer some of their material via YouTube as part of the YouTube partnership program.
    Unregistered users can only watch videos on the site, while registered users are
    permitted to upload an unlimited number of videos and add comments to videos.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: 1.0.0
host: www.googleapis.com
basePath: /youtube/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /comments:
    get:
      summary: Get Comments
      description: Returns a list of comments that match the API request parameters
      operationId: getComments
      parameters:
      - in: query
        name: id
        description: The id parameter specifies a comma-separated list of comment
          IDs for the resources that are being retrieved
      - in: query
        name: maxResults
        description: The maxResults parameter specifies the maximum number of items
          that should be returned in the result set
      - in: query
        name: pageToken
        description: The pageToken parameter identifies a specific page in the result
          set that should be returned
      - in: query
        name: parentId
        description: The parentId parameter specifies the ID of the comment for which
          replies should be retrieved
      - in: query
        name: part
        description: The part parameter specifies a comma-separated list of one or
          more comment resource properties that the API response will include
      - in: query
        name: textFormat
        description: This parameter indicates whether the API should return comments
          formatted as HTML or as plain text
      responses:
        200:
          description: OK
      tags:
      - comments
definitions:
  Empty:
    properties: []
  GdataBlobstore2Info:
    properties:
      blobGeneration:
        description: This is a default description.
        type: parameters
      blobId:
        description: This is a default description.
        type: parameters
      downloadReadHandle:
        description: This is a default description.
        type: parameters
      readToken:
        description: This is a default description.
        type: parameters
      uploadMetadataContainer:
        description: This is a default description.
        type: parameters
  GdataCompositeMedia:
    properties:
      blobRef:
        description: This is a default description.
        type: parameters
      cosmoBinaryReference:
        description: This is a default description.
        type: parameters
      crc32cHash:
        description: This is a default description.
        type: parameters
      inline:
        description: This is a default description.
        type: parameters
      length:
        description: This is a default description.
        type: parameters
      md5Hash:
        description: This is a default description.
        type: parameters
      path:
        description: This is a default description.
        type: parameters
      referenceType:
        description: This is a default description.
        type: parameters
      sha1Hash:
        description: This is a default description.
        type: parameters
  GdataContentTypeInfo:
    properties:
      bestGuess:
        description: This is a default description.
        type: parameters
      fromBytes:
        description: This is a default description.
        type: parameters
      fromFileName:
        description: This is a default description.
        type: parameters
      fromHeader:
        description: This is a default description.
        type: parameters
      fromUrlPath:
        description: This is a default description.
        type: parameters
  GdataDiffChecksumsResponse:
    properties:
      chunkSizeBytes:
        description: This is a default description.
        type: parameters
      objectSizeBytes:
        description: This is a default description.
        type: parameters
      objectVersion:
        description: This is a default description.
        type: parameters
  GdataDiffDownloadResponse:
    properties: []
  GdataDiffUploadRequest:
    properties:
      objectVersion:
        description: This is a default description.
        type: parameters
  GdataDiffUploadResponse:
    properties:
      objectVersion:
        description: This is a default description.
        type: parameters
  GdataDiffVersionResponse:
    properties:
      objectSizeBytes:
        description: This is a default description.
        type: parameters
      objectVersion:
        description: This is a default description.
        type: parameters
  GdataDownloadParameters:
    properties:
      allowGzipCompression:
        description: This is a default description.
        type: parameters
      ignoreRange:
        description: This is a default description.
        type: parameters
  GdataMedia:
    properties:
      algorithm:
        description: This is a default description.
        type: parameters
      bigstoreObjectRef:
        description: This is a default description.
        type: parameters
      blobRef:
        description: This is a default description.
        type: parameters
      compositeMedia:
        description: This is a default description.
        type: parameters
      contentType:
        description: This is a default description.
        type: parameters
      cosmoBinaryReference:
        description: This is a default description.
        type: parameters
      crc32cHash:
        description: This is a default description.
        type: parameters
      filename:
        description: This is a default description.
        type: parameters
      hash:
        description: This is a default description.
        type: parameters
      hashVerified:
        description: This is a default description.
        type: parameters
  GdataObjectId:
    properties:
      bucketName:
        description: This is a default description.
        type: parameters
      generation:
        description: This is a default description.
        type: parameters
      objectName:
        description: This is a default description.
        type: parameters
  Job:
    properties:
      createTime:
        description: This is a default description.
        type: parameters
      expireTime:
        description: This is a default description.
        type: parameters
      id:
        description: This is a default description.
        type: parameters
      name:
        description: This is a default description.
        type: parameters
      reportTypeId:
        description: This is a default description.
        type: parameters
      systemManaged:
        description: This is a default description.
        type: parameters
  ListJobsResponse:
    properties:
      jobs:
        description: This is a default description.
        type: parameters
      nextPageToken:
        description: This is a default description.
        type: parameters
  ListReportTypesResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: parameters
      reportTypes:
        description: This is a default description.
        type: parameters
  ListReportsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: parameters
      reports:
        description: This is a default description.
        type: parameters
  Report:
    properties:
      createTime:
        description: This is a default description.
        type: parameters
      downloadUrl:
        description: This is a default description.
        type: parameters
      endTime:
        description: This is a default description.
        type: parameters
      id:
        description: This is a default description.
        type: parameters
      jobExpireTime:
        description: This is a default description.
        type: parameters
      jobId:
        description: This is a default description.
        type: parameters
      startTime:
        description: This is a default description.
        type: parameters
  ReportType:
    properties:
      deprecateTime:
        description: This is a default description.
        type: parameters
      id:
        description: This is a default description.
        type: parameters
      name:
        description: This is a default description.
        type: parameters
      systemManaged:
        description: This is a default description.
        type: parameters
  AccessPolicy:
    properties:
      allowed:
        description: This is a default description.
        type: post
      exception:
        description: This is a default description.
        type: post
  Activity:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  ActivityContentDetails:
    properties: []
  ActivityContentDetailsBulletin:
    properties: []
  ActivityContentDetailsChannelItem:
    properties: []
  ActivityContentDetailsComment:
    properties: []
  ActivityContentDetailsFavorite:
    properties: []
  ActivityContentDetailsLike:
    properties: []
  ActivityContentDetailsPlaylistItem:
    properties:
      playlistId:
        description: This is a default description.
        type: post
      playlistItemId:
        description: This is a default description.
        type: post
  ActivityContentDetailsPromotedItem:
    properties:
      adTag:
        description: This is a default description.
        type: post
      clickTrackingUrl:
        description: This is a default description.
        type: post
      creativeViewUrl:
        description: This is a default description.
        type: post
      ctaType:
        description: This is a default description.
        type: post
      customCtaButtonText:
        description: This is a default description.
        type: post
      descriptionText:
        description: This is a default description.
        type: post
      destinationUrl:
        description: This is a default description.
        type: post
      forecastingUrl:
        description: This is a default description.
        type: post
      impressionUrl:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
  ActivityContentDetailsRecommendation:
    properties:
      reason:
        description: This is a default description.
        type: post
  ActivityContentDetailsSocial:
    properties:
      author:
        description: This is a default description.
        type: post
      imageUrl:
        description: This is a default description.
        type: post
      referenceUrl:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  ActivityContentDetailsSubscription:
    properties: []
  ActivityContentDetailsUpload:
    properties:
      videoId:
        description: This is a default description.
        type: post
  ActivityListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  ActivitySnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      groupId:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  Caption:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  CaptionListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  CaptionSnippet:
    properties:
      audioTrackType:
        description: This is a default description.
        type: post
      failureReason:
        description: This is a default description.
        type: post
      isAutoSynced:
        description: This is a default description.
        type: post
      isCC:
        description: This is a default description.
        type: post
      isDraft:
        description: This is a default description.
        type: post
      isEasyReader:
        description: This is a default description.
        type: post
      isLarge:
        description: This is a default description.
        type: post
      language:
        description: This is a default description.
        type: post
      lastUpdated:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  CdnSettings:
    properties:
      format:
        description: This is a default description.
        type: post
      frameRate:
        description: This is a default description.
        type: post
      ingestionType:
        description: This is a default description.
        type: post
      resolution:
        description: This is a default description.
        type: post
  Channel:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      localizations:
        description: This is a default description.
        type: post
  ChannelAuditDetails:
    properties:
      communityGuidelinesGoodStanding:
        description: This is a default description.
        type: post
      contentIdClaimsGoodStanding:
        description: This is a default description.
        type: post
      copyrightStrikesGoodStanding:
        description: This is a default description.
        type: post
      overallGoodStanding:
        description: This is a default description.
        type: post
  ChannelBannerResource:
    properties:
      etag:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
  ChannelBrandingSettings:
    properties:
      hints:
        description: This is a default description.
        type: post
  ChannelContentDetails:
    properties:
      relatedPlaylists:
        description: This is a default description.
        type: post
  ChannelContentOwnerDetails:
    properties:
      contentOwner:
        description: This is a default description.
        type: post
      timeLinked:
        description: This is a default description.
        type: post
  ChannelConversionPing:
    properties:
      context:
        description: This is a default description.
        type: post
      conversionUrl:
        description: This is a default description.
        type: post
  ChannelConversionPings:
    properties:
      pings:
        description: This is a default description.
        type: post
  ChannelListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  ChannelLocalization:
    properties:
      description:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  ChannelProfileDetails:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelUrl:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      profileImageUrl:
        description: This is a default description.
        type: post
  ChannelSection:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      localizations:
        description: This is a default description.
        type: post
  ChannelSectionContentDetails:
    properties:
      channels:
        description: This is a default description.
        type: post
      playlists:
        description: This is a default description.
        type: post
  ChannelSectionListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  ChannelSectionLocalization:
    properties:
      title:
        description: This is a default description.
        type: post
  ChannelSectionSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      defaultLanguage:
        description: This is a default description.
        type: post
      position:
        description: This is a default description.
        type: post
      style:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  ChannelSectionTargeting:
    properties:
      countries:
        description: This is a default description.
        type: post
      languages:
        description: This is a default description.
        type: post
      regions:
        description: This is a default description.
        type: post
  ChannelSettings:
    properties:
      country:
        description: This is a default description.
        type: post
      defaultLanguage:
        description: This is a default description.
        type: post
      defaultTab:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      featuredChannelsTitle:
        description: This is a default description.
        type: post
      featuredChannelsUrls:
        description: This is a default description.
        type: post
      keywords:
        description: This is a default description.
        type: post
      moderateComments:
        description: This is a default description.
        type: post
      profileColor:
        description: This is a default description.
        type: post
      showBrowseView:
        description: This is a default description.
        type: post
  ChannelSnippet:
    properties:
      country:
        description: This is a default description.
        type: post
      customUrl:
        description: This is a default description.
        type: post
      defaultLanguage:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  ChannelStatistics:
    properties:
      commentCount:
        description: This is a default description.
        type: post
      hiddenSubscriberCount:
        description: This is a default description.
        type: post
      subscriberCount:
        description: This is a default description.
        type: post
      videoCount:
        description: This is a default description.
        type: post
      viewCount:
        description: This is a default description.
        type: post
  ChannelStatus:
    properties:
      isLinked:
        description: This is a default description.
        type: post
      longUploadsStatus:
        description: This is a default description.
        type: post
      privacyStatus:
        description: This is a default description.
        type: post
  ChannelTopicDetails:
    properties:
      topicCategories:
        description: This is a default description.
        type: post
      topicIds:
        description: This is a default description.
        type: post
  Comment:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  CommentListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  CommentSnippet:
    properties:
      authorChannelUrl:
        description: This is a default description.
        type: post
      authorDisplayName:
        description: This is a default description.
        type: post
      authorProfileImageUrl:
        description: This is a default description.
        type: post
      canRate:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      likeCount:
        description: This is a default description.
        type: post
      moderationStatus:
        description: This is a default description.
        type: post
      parentId:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      textDisplay:
        description: This is a default description.
        type: post
  CommentThread:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  CommentThreadListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  CommentThreadReplies:
    properties:
      comments:
        description: This is a default description.
        type: post
  CommentThreadSnippet:
    properties:
      canReply:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      isPublic:
        description: This is a default description.
        type: post
      totalReplyCount:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
  ContentRating:
    properties:
      acbRating:
        description: This is a default description.
        type: post
      agcomRating:
        description: This is a default description.
        type: post
      anatelRating:
        description: This is a default description.
        type: post
      bbfcRating:
        description: This is a default description.
        type: post
      bfvcRating:
        description: This is a default description.
        type: post
      bmukkRating:
        description: This is a default description.
        type: post
      catvRating:
        description: This is a default description.
        type: post
      catvfrRating:
        description: This is a default description.
        type: post
      cbfcRating:
        description: This is a default description.
        type: post
      cccRating:
        description: This is a default description.
        type: post
  FanFundingEvent:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  FanFundingEventListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  FanFundingEventSnippet:
    properties:
      amountMicros:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      commentText:
        description: This is a default description.
        type: post
      createdAt:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      displayString:
        description: This is a default description.
        type: post
  GeoPoint:
    properties:
      altitude:
        description: This is a default description.
        type: post
      latitude:
        description: This is a default description.
        type: post
      longitude:
        description: This is a default description.
        type: post
  GuideCategory:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  GuideCategoryListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  GuideCategorySnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  I18nLanguage:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  I18nLanguageListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  I18nLanguageSnippet:
    properties:
      hl:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  I18nRegion:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  I18nRegionListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  I18nRegionSnippet:
    properties:
      gl:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  ImageSettings:
    properties:
      bannerExternalUrl:
        description: This is a default description.
        type: post
      bannerImageUrl:
        description: This is a default description.
        type: post
      bannerMobileExtraHdImageUrl:
        description: This is a default description.
        type: post
      bannerMobileHdImageUrl:
        description: This is a default description.
        type: post
      bannerMobileImageUrl:
        description: This is a default description.
        type: post
      bannerMobileLowImageUrl:
        description: This is a default description.
        type: post
      bannerMobileMediumHdImageUrl:
        description: This is a default description.
        type: post
      bannerTabletExtraHdImageUrl:
        description: This is a default description.
        type: post
      bannerTabletHdImageUrl:
        description: This is a default description.
        type: post
      bannerTabletImageUrl:
        description: This is a default description.
        type: post
  IngestionInfo:
    properties:
      backupIngestionAddress:
        description: This is a default description.
        type: post
      ingestionAddress:
        description: This is a default description.
        type: post
      streamName:
        description: This is a default description.
        type: post
  InvideoBranding:
    properties:
      imageBytes:
        description: This is a default description.
        type: post
      imageUrl:
        description: This is a default description.
        type: post
      targetChannelId:
        description: This is a default description.
        type: post
  InvideoPosition:
    properties:
      cornerPosition:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  InvideoPromotion:
    properties:
      items:
        description: This is a default description.
        type: post
      useSmartTiming:
        description: This is a default description.
        type: post
  InvideoTiming:
    properties:
      durationMs:
        description: This is a default description.
        type: post
      offsetMs:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  LanguageTag:
    properties:
      value:
        description: This is a default description.
        type: post
  LiveBroadcast:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  LiveBroadcastContentDetails:
    properties:
      boundStreamId:
        description: This is a default description.
        type: post
      boundStreamLastUpdateTimeMs:
        description: This is a default description.
        type: post
      closedCaptionsType:
        description: This is a default description.
        type: post
      enableAutoStart:
        description: This is a default description.
        type: post
      enableClosedCaptions:
        description: This is a default description.
        type: post
      enableContentEncryption:
        description: This is a default description.
        type: post
      enableDvr:
        description: This is a default description.
        type: post
      enableEmbed:
        description: This is a default description.
        type: post
      enableLowLatency:
        description: This is a default description.
        type: post
      latencyPreference:
        description: This is a default description.
        type: post
  LiveBroadcastListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  LiveBroadcastSnippet:
    properties:
      actualEndTime:
        description: This is a default description.
        type: post
      actualStartTime:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      isDefaultBroadcast:
        description: This is a default description.
        type: post
      liveChatId:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      scheduledEndTime:
        description: This is a default description.
        type: post
      scheduledStartTime:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  LiveBroadcastStatistics:
    properties:
      concurrentViewers:
        description: This is a default description.
        type: post
      totalChatCount:
        description: This is a default description.
        type: post
  LiveBroadcastStatus:
    properties:
      lifeCycleStatus:
        description: This is a default description.
        type: post
      liveBroadcastPriority:
        description: This is a default description.
        type: post
      privacyStatus:
        description: This is a default description.
        type: post
      recordingStatus:
        description: This is a default description.
        type: post
  LiveChatBan:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  LiveChatBanSnippet:
    properties:
      banDurationSeconds:
        description: This is a default description.
        type: post
      liveChatId:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  LiveChatFanFundingEventDetails:
    properties:
      amountDisplayString:
        description: This is a default description.
        type: post
      amountMicros:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      userComment:
        description: This is a default description.
        type: post
  LiveChatMessage:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  LiveChatMessageAuthorDetails:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelUrl:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      isChatModerator:
        description: This is a default description.
        type: post
      isChatOwner:
        description: This is a default description.
        type: post
      isChatSponsor:
        description: This is a default description.
        type: post
      isVerified:
        description: This is a default description.
        type: post
      profileImageUrl:
        description: This is a default description.
        type: post
  LiveChatMessageDeletedDetails:
    properties:
      deletedMessageId:
        description: This is a default description.
        type: post
  LiveChatMessageListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      offlineAt:
        description: This is a default description.
        type: post
      pollingIntervalMillis:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  LiveChatMessageRetractedDetails:
    properties:
      retractedMessageId:
        description: This is a default description.
        type: post
  LiveChatMessageSnippet:
    properties:
      authorChannelId:
        description: This is a default description.
        type: post
      displayMessage:
        description: This is a default description.
        type: post
      hasDisplayContent:
        description: This is a default description.
        type: post
      liveChatId:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  LiveChatModerator:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  LiveChatModeratorListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  LiveChatModeratorSnippet:
    properties:
      liveChatId:
        description: This is a default description.
        type: post
  LiveChatPollClosedDetails:
    properties:
      pollId:
        description: This is a default description.
        type: post
  LiveChatPollEditedDetails:
    properties:
      id:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      prompt:
        description: This is a default description.
        type: post
  LiveChatPollItem:
    properties:
      description:
        description: This is a default description.
        type: post
      itemId:
        description: This is a default description.
        type: post
  LiveChatPollOpenedDetails:
    properties:
      id:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      prompt:
        description: This is a default description.
        type: post
  LiveChatPollVotedDetails:
    properties:
      itemId:
        description: This is a default description.
        type: post
      pollId:
        description: This is a default description.
        type: post
  LiveChatSuperChatDetails:
    properties:
      amountDisplayString:
        description: This is a default description.
        type: post
      amountMicros:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      tier:
        description: This is a default description.
        type: post
      userComment:
        description: This is a default description.
        type: post
  LiveChatTextMessageDetails:
    properties:
      messageText:
        description: This is a default description.
        type: post
  LiveChatUserBannedMessageDetails:
    properties:
      banDurationSeconds:
        description: This is a default description.
        type: post
      banType:
        description: This is a default description.
        type: post
  LiveStream:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  LiveStreamConfigurationIssue:
    properties:
      description:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      severity:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  LiveStreamContentDetails:
    properties:
      closedCaptionsIngestionUrl:
        description: This is a default description.
        type: post
      isReusable:
        description: This is a default description.
        type: post
  LiveStreamHealthStatus:
    properties:
      configurationIssues:
        description: This is a default description.
        type: post
      lastUpdateTimeSeconds:
        description: This is a default description.
        type: post
      status:
        description: This is a default description.
        type: post
  LiveStreamListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  LiveStreamSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      isDefaultStream:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  LiveStreamStatus:
    properties:
      streamStatus:
        description: This is a default description.
        type: post
  LocalizedProperty:
    properties:
      default:
        description: This is a default description.
        type: post
      localized:
        description: This is a default description.
        type: post
  LocalizedString:
    properties:
      language:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  MonitorStreamInfo:
    properties:
      broadcastStreamDelayMs:
        description: This is a default description.
        type: post
      embedHtml:
        description: This is a default description.
        type: post
      enableMonitorStream:
        description: This is a default description.
        type: post
  PageInfo:
    properties:
      resultsPerPage:
        description: This is a default description.
        type: post
      totalResults:
        description: This is a default description.
        type: post
  Playlist:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      localizations:
        description: This is a default description.
        type: post
  PlaylistContentDetails:
    properties:
      itemCount:
        description: This is a default description.
        type: post
  PlaylistItem:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  PlaylistItemContentDetails:
    properties:
      endAt:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      startAt:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
      videoPublishedAt:
        description: This is a default description.
        type: post
  PlaylistItemListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  PlaylistItemSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      playlistId:
        description: This is a default description.
        type: post
      position:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  PlaylistItemStatus:
    properties:
      privacyStatus:
        description: This is a default description.
        type: post
  PlaylistListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  PlaylistLocalization:
    properties:
      description:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  PlaylistPlayer:
    properties:
      embedHtml:
        description: This is a default description.
        type: post
  PlaylistSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      defaultLanguage:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      tags:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  PlaylistStatus:
    properties:
      privacyStatus:
        description: This is a default description.
        type: post
  PromotedItem:
    properties:
      customMessage:
        description: This is a default description.
        type: post
      promotedByContentOwner:
        description: This is a default description.
        type: post
  PromotedItemId:
    properties:
      recentlyUploadedBy:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
      websiteUrl:
        description: This is a default description.
        type: post
  PropertyValue:
    properties:
      property:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  ResourceId:
    properties:
      channelId:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      playlistId:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
  SearchListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      regionCode:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  SearchResult:
    properties:
      etag:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  SearchResultSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      liveBroadcastContent:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  Sponsor:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  SponsorListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  SponsorSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      sponsorSince:
        description: This is a default description.
        type: post
  Subscription:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  SubscriptionContentDetails:
    properties:
      activityType:
        description: This is a default description.
        type: post
      newItemCount:
        description: This is a default description.
        type: post
      totalItemCount:
        description: This is a default description.
        type: post
  SubscriptionListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  SubscriptionSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  SubscriptionSubscriberSnippet:
    properties:
      channelId:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  SuperChatEvent:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  SuperChatEventListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  SuperChatEventSnippet:
    properties:
      amountMicros:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      commentText:
        description: This is a default description.
        type: post
      createdAt:
        description: This is a default description.
        type: post
      currency:
        description: This is a default description.
        type: post
      displayString:
        description: This is a default description.
        type: post
      messageType:
        description: This is a default description.
        type: post
  Thumbnail:
    properties:
      height:
        description: This is a default description.
        type: post
      url:
        description: This is a default description.
        type: post
      width:
        description: This is a default description.
        type: post
  ThumbnailDetails:
    properties: []
  ThumbnailSetResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  Video:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      localizations:
        description: This is a default description.
        type: post
  VideoAbuseReport:
    properties:
      comments:
        description: This is a default description.
        type: post
      language:
        description: This is a default description.
        type: post
      reasonId:
        description: This is a default description.
        type: post
      secondaryReasonId:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
  VideoAbuseReportReason:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  VideoAbuseReportReasonListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  VideoAbuseReportReasonSnippet:
    properties:
      label:
        description: This is a default description.
        type: post
      secondaryReasons:
        description: This is a default description.
        type: post
  VideoAbuseReportSecondaryReason:
    properties:
      id:
        description: This is a default description.
        type: post
      label:
        description: This is a default description.
        type: post
  VideoAgeGating:
    properties:
      alcoholContent:
        description: This is a default description.
        type: post
      restricted:
        description: This is a default description.
        type: post
      videoGameRating:
        description: This is a default description.
        type: post
  VideoCategory:
    properties:
      etag:
        description: This is a default description.
        type: post
      id:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
  VideoCategoryListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  VideoCategorySnippet:
    properties:
      assignable:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  VideoContentDetails:
    properties:
      caption:
        description: This is a default description.
        type: post
      definition:
        description: This is a default description.
        type: post
      dimension:
        description: This is a default description.
        type: post
      duration:
        description: This is a default description.
        type: post
      hasCustomThumbnail:
        description: This is a default description.
        type: post
      licensedContent:
        description: This is a default description.
        type: post
      projection:
        description: This is a default description.
        type: post
  VideoContentDetailsRegionRestriction:
    properties:
      allowed:
        description: This is a default description.
        type: post
      blocked:
        description: This is a default description.
        type: post
  VideoFileDetails:
    properties:
      audioStreams:
        description: This is a default description.
        type: post
      bitrateBps:
        description: This is a default description.
        type: post
      container:
        description: This is a default description.
        type: post
      creationTime:
        description: This is a default description.
        type: post
      durationMs:
        description: This is a default description.
        type: post
      fileName:
        description: This is a default description.
        type: post
      fileSize:
        description: This is a default description.
        type: post
      fileType:
        description: This is a default description.
        type: post
      videoStreams:
        description: This is a default description.
        type: post
  VideoFileDetailsAudioStream:
    properties:
      bitrateBps:
        description: This is a default description.
        type: post
      channelCount:
        description: This is a default description.
        type: post
      codec:
        description: This is a default description.
        type: post
      vendor:
        description: This is a default description.
        type: post
  VideoFileDetailsVideoStream:
    properties:
      aspectRatio:
        description: This is a default description.
        type: post
      bitrateBps:
        description: This is a default description.
        type: post
      codec:
        description: This is a default description.
        type: post
      frameRateFps:
        description: This is a default description.
        type: post
      heightPixels:
        description: This is a default description.
        type: post
      rotation:
        description: This is a default description.
        type: post
      vendor:
        description: This is a default description.
        type: post
      widthPixels:
        description: This is a default description.
        type: post
  VideoGetRatingResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  VideoListResponse:
    properties:
      etag:
        description: This is a default description.
        type: post
      eventId:
        description: This is a default description.
        type: post
      items:
        description: This is a default description.
        type: post
      kind:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
      prevPageToken:
        description: This is a default description.
        type: post
      visitorId:
        description: This is a default description.
        type: post
  VideoLiveStreamingDetails:
    properties:
      activeLiveChatId:
        description: This is a default description.
        type: post
      actualEndTime:
        description: This is a default description.
        type: post
      actualStartTime:
        description: This is a default description.
        type: post
      concurrentViewers:
        description: This is a default description.
        type: post
      scheduledEndTime:
        description: This is a default description.
        type: post
      scheduledStartTime:
        description: This is a default description.
        type: post
  VideoLocalization:
    properties:
      description:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  VideoMonetizationDetails:
    properties: []
  VideoPlayer:
    properties:
      embedHeight:
        description: This is a default description.
        type: post
      embedHtml:
        description: This is a default description.
        type: post
      embedWidth:
        description: This is a default description.
        type: post
  VideoProcessingDetails:
    properties:
      editorSuggestionsAvailability:
        description: This is a default description.
        type: post
      fileDetailsAvailability:
        description: This is a default description.
        type: post
      processingFailureReason:
        description: This is a default description.
        type: post
      processingIssuesAvailability:
        description: This is a default description.
        type: post
      processingStatus:
        description: This is a default description.
        type: post
      tagSuggestionsAvailability:
        description: This is a default description.
        type: post
      thumbnailsAvailability:
        description: This is a default description.
        type: post
  VideoProcessingDetailsProcessingProgress:
    properties:
      partsProcessed:
        description: This is a default description.
        type: post
      partsTotal:
        description: This is a default description.
        type: post
      timeLeftMs:
        description: This is a default description.
        type: post
  VideoProjectDetails:
    properties:
      tags:
        description: This is a default description.
        type: post
  VideoRating:
    properties:
      rating:
        description: This is a default description.
        type: post
      videoId:
        description: This is a default description.
        type: post
  VideoRecordingDetails:
    properties:
      locationDescription:
        description: This is a default description.
        type: post
      recordingDate:
        description: This is a default description.
        type: post
  VideoSnippet:
    properties:
      categoryId:
        description: This is a default description.
        type: post
      channelId:
        description: This is a default description.
        type: post
      channelTitle:
        description: This is a default description.
        type: post
      defaultAudioLanguage:
        description: This is a default description.
        type: post
      defaultLanguage:
        description: This is a default description.
        type: post
      description:
        description: This is a default description.
        type: post
      liveBroadcastContent:
        description: This is a default description.
        type: post
      publishedAt:
        description: This is a default description.
        type: post
      tags:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  VideoStatistics:
    properties:
      commentCount:
        description: This is a default description.
        type: post
      dislikeCount:
        description: This is a default description.
        type: post
      favoriteCount:
        description: This is a default description.
        type: post
      likeCount:
        description: This is a default description.
        type: post
      viewCount:
        description: This is a default description.
        type: post
  VideoStatus:
    properties:
      embeddable:
        description: This is a default description.
        type: post
      failureReason:
        description: This is a default description.
        type: post
      license:
        description: This is a default description.
        type: post
      privacyStatus:
        description: This is a default description.
        type: post
      publicStatsViewable:
        description: This is a default description.
        type: post
      publishAt:
        description: This is a default description.
        type: post
      rejectionReason:
        description: This is a default description.
        type: post
      uploadStatus:
        description: This is a default description.
        type: post
  VideoSuggestions:
    properties:
      editorSuggestions:
        description: This is a default description.
        type: post
      processingErrors:
        description: This is a default description.
        type: post
      processingHints:
        description: This is a default description.
        type: post
      processingWarnings:
        description: This is a default description.
        type: post
      tagSuggestions:
        description: This is a default description.
        type: post
  VideoSuggestionsTagSuggestion:
    properties:
      categoryRestricts:
        description: This is a default description.
        type: post
      tag:
        description: This is a default description.
        type: post
  VideoTopicDetails:
    properties:
      relevantTopicIds:
        description: This is a default description.
        type: post
      topicCategories:
        description: This is a default description.
        type: post
      topicIds:
        description: This is a default description.
        type: post
  WatchSettings:
    properties:
      backgroundColor:
        description: This is a default description.
        type: post
      featuredPlaylistId:
        description: This is a default description.
        type: post
      textColor:
        description: This is a default description.
        type: post
  Group:
    properties:
      contentDetails:
        description: This is a default description.
        type: parameters
      etag:
        description: This is a default description.
        type: parameters
      id:
        description: This is a default description.
        type: parameters
      kind:
        description: This is a default description.
        type: parameters
      snippet:
        description: This is a default description.
        type: parameters
  GroupItem:
    properties:
      etag:
        description: This is a default description.
        type: parameters
      groupId:
        description: This is a default description.
        type: parameters
      id:
        description: This is a default description.
        type: parameters
      kind:
        description: This is a default description.
        type: parameters
      resource:
        description: This is a default description.
        type: parameters
  GroupItemListResponse:
    properties:
      etag:
        description: This is a default description.
        type: parameters
      items:
        description: This is a default description.
        type: parameters
      kind:
        description: This is a default description.
        type: parameters
  GroupListResponse:
    properties:
      etag:
        description: This is a default description.
        type: parameters
      items:
        description: This is a default description.
        type: parameters
      kind:
        description: This is a default description.
        type: parameters
      nextPageToken:
        description: This is a default description.
        type: parameters
  ResultTable:
    properties:
      columnHeaders:
        description: This is a default description.
        type: parameters
      kind:
        description: This is a default description.
        type: parameters
      rows:
        description: This is a default description.
        type: parameters
x-collection-name: YouTube
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