---
swagger: "2.0"
info:
  title: GitHub
  description: GitHub is the best place to share code with friends, co-workers, classmates,
    and complete strangers. Over 24 million people use GitHub to build amazing things
    together across 67 million repositories. With the collaborative features of GitHub.com
    and GitHub Business, it has never been easier for individuals and teams to write
    faster, better code.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search/issues:
    get:
      summary: Get Search Issues
      description: Find issues by state and keyword
      operationId: find-issues-by-state-and-keyword-this-method-returns-up-to-100-results-per-page
      x-api-path-slug: searchissues-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: 'The q search term can also contain any combination of the supported
          issue search qualifiers:'
      - in: query
        name: sort
        description: The sort field
      responses:
        200:
          description: OK
      tags:
      - search
      - issues
definitions:
  asset:
    properties:
      content_type:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      download_count:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      label:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      uploader:
        description: This is a default description.
        type: get
  assetPatch:
    properties:
      label:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  blob:
    properties:
      content:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
  blobs:
    properties:
      sha:
        description: This is a default description.
        type: get
  branch:
    properties:
      _links:
        description: This is a default description.
        type: get
      commit:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  comment:
    properties:
      body:
        description: This is a default description.
        type: get
  commentBody:
    properties:
      body:
        description: This is a default description.
        type: get
  commit:
    properties:
      author:
        description: This is a default description.
        type: get
      commit:
        description: This is a default description.
        type: get
      committer:
        description: This is a default description.
        type: get
      files:
        description: This is a default description.
        type: get
      parents:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      stats:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  commitBody:
    properties:
      body:
        description: This is a default description.
        type: get
      line:
        description: This is a default description.
        type: get
      number:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      position:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  commitComments:
    properties:
      body:
        description: This is a default description.
        type: get
      commit_id:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      line:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      position:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  compare-commits:
    properties:
      ahead_by:
        description: This is a default description.
        type: get
      base_commit:
        description: This is a default description.
        type: get
      behind_by:
        description: This is a default description.
        type: get
      commits:
        description: This is a default description.
        type: get
      diff_url:
        description: This is a default description.
        type: get
      files:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      patch_url:
        description: This is a default description.
        type: get
      permalink_url:
        description: This is a default description.
        type: get
      status:
        description: This is a default description.
        type: get
  contents-path:
    properties:
      _links:
        description: This is a default description.
        type: get
      content:
        description: This is a default description.
        type: get
      encoding:
        description: This is a default description.
        type: get
      git_url:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  createDownload:
    properties:
      accesskeyid:
        description: This is a default description.
        type: get
      acl:
        description: This is a default description.
        type: get
      bucket:
        description: This is a default description.
        type: get
      content_type:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      download_count:
        description: This is a default description.
        type: get
      expirationdate:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      mime_type:
        description: This is a default description.
        type: get
  createFile:
    properties:
      commit:
        description: This is a default description.
        type: get
      content:
        description: This is a default description.
        type: get
  createFileBody:
    properties:
      committer:
        description: This is a default description.
        type: get
      content:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
  deleteFile:
    properties:
      commit:
        description: This is a default description.
        type: get
      content:
        description: This is a default description.
        type: get
  deleteFileBody:
    properties:
      committer:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  deployment:
    properties:
      description:
        description: This is a default description.
        type: get
      payload:
        description: This is a default description.
        type: get
      ref:
        description: This is a default description.
        type: get
  deployment-resp:
    properties:
      created_at:
        description: This is a default description.
        type: get
      creator:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      payload:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      statuses_url:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  deployment-statuses-create:
    properties:
      description:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      target_url:
        description: This is a default description.
        type: get
  downloadBody:
    properties:
      content_type:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
  downloads:
    properties:
      content_type:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      download_count:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  editTeam:
    properties:
      name:
        description: This is a default description.
        type: get
  emojis:
    properties:
      100:
        description: This is a default description.
        type: get
      1234:
        description: This is a default description.
        type: get
      "+1":
        description: This is a default description.
        type: get
      -1:
        description: This is a default description.
        type: get
      8ball:
        description: This is a default description.
        type: get
      a:
        description: This is a default description.
        type: get
      ab:
        description: This is a default description.
        type: get
  event:
    properties:
      actor:
        description: This is a default description.
        type: get
      commit_id:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      event:
        description: This is a default description.
        type: get
      issue:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  events:
    properties:
      actor:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      org:
        description: This is a default description.
        type: get
      payload:
        description: This is a default description.
        type: get
      public:
        description: This is a default description.
        type: get
      repo:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  feeds:
    properties:
      current_user_actor_url:
        description: This is a default description.
        type: get
      current_user_organization_url:
        description: This is a default description.
        type: get
      current_user_public:
        description: This is a default description.
        type: get
      current_user_url:
        description: This is a default description.
        type: get
      timeline_url:
        description: This is a default description.
        type: get
      user_url:
        description: This is a default description.
        type: get
  fork:
    properties:
      clone_url:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      fork:
        description: This is a default description.
        type: get
      forks:
        description: This is a default description.
        type: get
      forks_count:
        description: This is a default description.
        type: get
      full_name:
        description: This is a default description.
        type: get
      git_url:
        description: This is a default description.
        type: get
      homepage:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
  forkBody:
    properties:
      organization:
        description: This is a default description.
        type: get
  gist:
    properties:
      comments:
        description: This is a default description.
        type: get
      comments_url:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      files:
        description: This is a default description.
        type: get
      forks:
        description: This is a default description.
        type: get
      git_pull_url:
        description: This is a default description.
        type: get
      git_push_url:
        description: This is a default description.
        type: get
      history:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
  gitCommit:
    properties:
      author:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      parents:
        description: This is a default description.
        type: get
      tree:
        description: This is a default description.
        type: get
  gitRefPatch:
    properties:
      force:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  gitignore-lang:
    properties:
      name:
        description: This is a default description.
        type: get
      source:
        description: This is a default description.
        type: get
  headBranch:
    properties:
      object:
        description: This is a default description.
        type: get
      ref:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  headBranchBody:
    properties:
      force:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  hookBody:
    properties:
      active:
        description: This is a default description.
        type: get
      add_events:
        description: This is a default description.
        type: get
  issue:
    properties:
      assignee:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      labels:
        description: This is a default description.
        type: get
      milestone:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  issueBody:
    properties:
      assignee:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      labels:
        description: This is a default description.
        type: get
      milestone:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  issuesComment:
    properties:
      body:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      user:
        description: This is a default description.
        type: get
  key:
    properties:
      id:
        description: This is a default description.
        type: get
      key:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  keyBody:
    properties:
      key:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  label:
    properties:
      color:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  markdown:
    properties:
      context:
        description: This is a default description.
        type: get
      mode:
        description: This is a default description.
        type: get
      text:
        description: This is a default description.
        type: get
  merge:
    properties:
      merged:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  mergePullBody:
    properties:
      commit_message:
        description: This is a default description.
        type: get
  mergesBody:
    properties:
      base:
        description: This is a default description.
        type: get
      commit_message:
        description: This is a default description.
        type: get
      head:
        description: This is a default description.
        type: get
  mergesConflict:
    properties:
      message:
        description: This is a default description.
        type: get
  mergesSuccessful:
    properties:
      author:
        description: This is a default description.
        type: get
      comments_url:
        description: This is a default description.
        type: get
      commit:
        description: This is a default description.
        type: get
      committer:
        description: This is a default description.
        type: get
      merged:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      parents:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  meta:
    properties:
      git:
        description: This is a default description.
        type: get
      hooks:
        description: This is a default description.
        type: get
  milestone:
    properties:
      closed_issues:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      creator:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      due_on:
        description: This is a default description.
        type: get
      number:
        description: This is a default description.
        type: get
      open_issues:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  milestoneBody:
    properties:
      description:
        description: This is a default description.
        type: get
      due_on:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  milestoneUpdate:
    properties:
      description:
        description: This is a default description.
        type: get
      due_on:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  notificationMarkRead:
    properties:
      last_read_at:
        description: This is a default description.
        type: get
  notifications:
    properties:
      id:
        description: This is a default description.
        type: get
      last_read_at:
        description: This is a default description.
        type: get
      reason:
        description: This is a default description.
        type: get
      repository:
        description: This is a default description.
        type: get
      subject:
        description: This is a default description.
        type: get
      unread:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  orgTeamsPost:
    properties:
      name:
        description: This is a default description.
        type: get
      repo_names:
        description: This is a default description.
        type: get
  organization:
    properties:
      avatar_url:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      company:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      followers:
        description: This is a default description.
        type: get
      following:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      location:
        description: This is a default description.
        type: get
  organizationAsTeamMember:
    properties:
      errors:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
  participationStats:
    properties:
      all:
        description: This is a default description.
        type: get
      owner:
        description: This is a default description.
        type: get
  patchGist:
    properties:
      description:
        description: This is a default description.
        type: get
  patchOrg:
    properties:
      billing_email:
        description: This is a default description.
        type: get
      company:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      location:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  postComment:
    properties:
      body:
        description: This is a default description.
        type: get
  postGist:
    properties:
      description:
        description: This is a default description.
        type: get
      files:
        description: This is a default description.
        type: get
      public:
        description: This is a default description.
        type: get
  postRepo:
    properties:
      auto_init:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      gitignore_template:
        description: This is a default description.
        type: get
      has_downloads:
        description: This is a default description.
        type: get
      has_issues:
        description: This is a default description.
        type: get
      has_wiki:
        description: This is a default description.
        type: get
      homepage:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      private:
        description: This is a default description.
        type: get
      team_id:
        description: This is a default description.
        type: get
  pullRequest:
    properties:
      _links:
        description: This is a default description.
        type: get
      additions:
        description: This is a default description.
        type: get
      base:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      changed_files:
        description: This is a default description.
        type: get
      closed_at:
        description: This is a default description.
        type: get
      comments:
        description: This is a default description.
        type: get
      commits:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      deletions:
        description: This is a default description.
        type: get
  pullUpdate:
    properties:
      body:
        description: This is a default description.
        type: get
      state:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  pullsComment:
    properties:
      _links:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      commit_id:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      position:
        description: This is a default description.
        type: get
      updated_at:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
      user:
        description: This is a default description.
        type: get
  pullsCommentPost:
    properties:
      body:
        description: This is a default description.
        type: get
      commit_id:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      position:
        description: This is a default description.
        type: get
  pullsPost:
    properties:
      base:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      head:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  putSubscription:
    properties:
      created_at:
        description: This is a default description.
        type: get
      ignored:
        description: This is a default description.
        type: get
      reason:
        description: This is a default description.
        type: get
      subscribed:
        description: This is a default description.
        type: get
      thread_url:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  rate_limit:
    properties: []
  readme:
    properties:
      _links:
        description: This is a default description.
        type: get
      content:
        description: This is a default description.
        type: get
      encoding:
        description: This is a default description.
        type: get
      git_url:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      path:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      size:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  refBody:
    properties:
      object:
        description: This is a default description.
        type: get
      ref:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  refsBody:
    properties:
      ref:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
  release:
    properties:
      assets:
        description: This is a default description.
        type: get
      assets_url:
        description: This is a default description.
        type: get
      author:
        description: This is a default description.
        type: get
      body:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      draft:
        description: This is a default description.
        type: get
      html_url:
        description: This is a default description.
        type: get
      id:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      prerelease:
        description: This is a default description.
        type: get
  release-create:
    properties:
      body:
        description: This is a default description.
        type: get
      draft:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      prerelease:
        description: This is a default description.
        type: get
      tag_name:
        description: This is a default description.
        type: get
      target_commitish:
        description: This is a default description.
        type: get
  repo:
    properties:
      clone_url:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      description:
        description: This is a default description.
        type: get
      fork:
        description: This is a default description.
        type: get
      forks:
        description: This is a default description.
        type: get
      forks_count:
        description: This is a default description.
        type: get
      full_name:
        description: This is a default description.
        type: get
      git_url:
        description: This is a default description.
        type: get
      has_downloads:
        description: This is a default description.
        type: get
      has_issues:
        description: This is a default description.
        type: get
  repoCommit:
    properties:
      author:
        description: This is a default description.
        type: get
      committer:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      parents:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      tree:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  repoCommitBody:
    properties:
      author:
        description: This is a default description.
        type: get
      message:
        description: This is a default description.
        type: get
      parents:
        description: This is a default description.
        type: get
      tree:
        description: This is a default description.
        type: get
  repoEdit:
    properties:
      description:
        description: This is a default description.
        type: get
      has_downloads:
        description: This is a default description.
        type: get
      has_issues:
        description: This is a default description.
        type: get
      has_wiki:
        description: This is a default description.
        type: get
      homepage:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      private:
        description: This is a default description.
        type: get
  search-code:
    properties:
      items:
        description: This is a default description.
        type: get
      total_count:
        description: This is a default description.
        type: get
  search-issues:
    properties:
      items:
        description: This is a default description.
        type: get
      total_count:
        description: This is a default description.
        type: get
  search-issues-by-keyword:
    properties:
      issues:
        description: This is a default description.
        type: get
  search-repositories:
    properties:
      items:
        description: This is a default description.
        type: get
      total_count:
        description: This is a default description.
        type: get
  search-repositories-by-keyword:
    properties:
      repositories:
        description: This is a default description.
        type: get
  search-user-by-email:
    properties:
      user:
        description: This is a default description.
        type: get
  search-users:
    properties:
      items:
        description: This is a default description.
        type: get
      total_count:
        description: This is a default description.
        type: get
  search-users-by-keyword:
    properties:
      users:
        description: This is a default description.
        type: get
  subscribition:
    properties:
      created_at:
        description: This is a default description.
        type: get
      ignored:
        description: This is a default description.
        type: get
      reason:
        description: This is a default description.
        type: get
      repository_url:
        description: This is a default description.
        type: get
      subscribed:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  subscribitionBody:
    properties:
      ignored:
        description: This is a default description.
        type: get
      subscribed:
        description: This is a default description.
        type: get
  subscription:
    properties:
      created_at:
        description: This is a default description.
        type: get
      ignored:
        description: This is a default description.
        type: get
      reason:
        description: This is a default description.
        type: get
      subscribed:
        description: This is a default description.
        type: get
      thread_url:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  tag:
    properties:
      message:
        description: This is a default description.
        type: get
      object:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      tag:
        description: This is a default description.
        type: get
      tagger:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  tags:
    properties:
      message:
        description: This is a default description.
        type: get
      object:
        description: This is a default description.
        type: get
      tag:
        description: This is a default description.
        type: get
      tagger:
        description: This is a default description.
        type: get
      type:
        description: This is a default description.
        type: get
  team:
    properties:
      id:
        description: This is a default description.
        type: get
      members_count:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
      permission:
        description: This is a default description.
        type: get
      repos_count:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  teamMembership:
    properties:
      state:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  tree:
    properties:
      sha:
        description: This is a default description.
        type: get
      tree:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  trees:
    properties:
      base_tree:
        description: This is a default description.
        type: get
      sha:
        description: This is a default description.
        type: get
      tree:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  user:
    properties:
      avatar_url:
        description: This is a default description.
        type: get
      bio:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      collaborators:
        description: This is a default description.
        type: get
      company:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      disk_usage:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      followers:
        description: This is a default description.
        type: get
      following:
        description: This is a default description.
        type: get
  user-keys-keyId:
    properties:
      id:
        description: This is a default description.
        type: get
      key:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
      url:
        description: This is a default description.
        type: get
  user-keys-post:
    properties:
      key:
        description: This is a default description.
        type: get
      title:
        description: This is a default description.
        type: get
  user-update:
    properties:
      bio:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      company:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      hireable:
        description: This is a default description.
        type: get
      location:
        description: This is a default description.
        type: get
      name:
        description: This is a default description.
        type: get
  user-userId:
    properties:
      avatar_url:
        description: This is a default description.
        type: get
      bio:
        description: This is a default description.
        type: get
      blog:
        description: This is a default description.
        type: get
      company:
        description: This is a default description.
        type: get
      created_at:
        description: This is a default description.
        type: get
      email:
        description: This is a default description.
        type: get
      followers:
        description: This is a default description.
        type: get
      following:
        description: This is a default description.
        type: get
      gravatar_id:
        description: This is a default description.
        type: get
      hireable:
        description: This is a default description.
        type: get
x-collection-name: GitHub
x-streamrank:
  polling_total_time_average: "0.98"
  polling_size_download_average: "80476.4"
  streaming_total_time_average: "0.51"
  streaming_size_download_average: "40251.83"
  change_yes: "2093"
  change_no: "240"
  time_percentage: "48"
  size_percentage: "50"
  change_percentage: "90"
  last_run: "2018-05-12"
  days_run: "8"
  minute_run: "0"
---