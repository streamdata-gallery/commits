---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Post Projects Repository Commits Sha Cherry Pick
  version: 1.0.0
  description: Post projects repository commits sha cherry pick.
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/repository/commits/{sha}/builds:
    get:
      summary: Get Projects Repository Commits Sha Builds
      description: Get builds for a specific commit of a project
      operationId: getV3ProjectsIdRepositoryCommitsShaBuilds
      x-api-path-slug: v3projectsidrepositorycommitsshabuilds-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: query
        name: scope
        description: The scope of builds to show
      - in: path
        name: sha
        description: The SHA id of a commit
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
      - Builds
  /v3/projects/{id}/repository/commits:
    get:
      summary: Get Projects Repository Commits
      description: Get a project repository commits
      operationId: getV3ProjectsIdRepositoryCommits
      x-api-path-slug: v3projectsidrepositorycommits-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: page
        description: The page for pagination
      - in: query
        name: path
        description: The file path
      - in: query
        name: per_page
        description: The number of results per page
      - in: query
        name: ref_name
        description: The name of a repository branch or tag, if not given the default
          branch is used
      - in: query
        name: since
        description: Only commits after or in this date will be returned
      - in: query
        name: until
        description: Only commits before or in this date will be returned
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
    post:
      summary: Post Projects Repository Commits
      description: This feature was introduced in GitLab 8.13
      operationId: postV3ProjectsIdRepositoryCommits
      x-api-path-slug: v3projectsidrepositorycommits-post
      parameters:
      - in: formData
        name: actions
        description: Actions to perform in commit
      - in: formData
        name: author_email
        description: Author email for commit
      - in: formData
        name: author_name
        description: Author name for commit
      - in: formData
        name: branch_name
        description: The name of branch
      - in: formData
        name: commit_message
        description: Commit message
      - in: path
        name: id
        description: The ID of a project
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
  /v3/projects/{id}/repository/commits/{sha}:
    get:
      summary: Get Projects Repository Commits Sha
      description: Get projects repository commits sha.
      operationId: getV3ProjectsIdRepositoryCommitsSha
      x-api-path-slug: v3projectsidrepositorycommitssha-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: sha
        description: A commit sha, or the name of a branch or tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
  /v3/projects/{id}/repository/commits/{sha}/diff:
    get:
      summary: Get Projects Repository Commits Sha Diff
      description: Get the diff for a specific commit of a project
      operationId: getV3ProjectsIdRepositoryCommitsShaDiff
      x-api-path-slug: v3projectsidrepositorycommitsshadiff-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: sha
        description: A commit sha, or the name of a branch or tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
      - Diff
  /v3/projects/{id}/repository/commits/{sha}/comments:
    get:
      summary: Get Projects Repository Commits Sha Comments
      description: Get projects repository commits sha comments.
      operationId: getV3ProjectsIdRepositoryCommitsShaComments
      x-api-path-slug: v3projectsidrepositorycommitsshacomments-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: path
        name: sha
        description: A commit sha, or the name of a branch or tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
      - Comments
    post:
      summary: Post Projects Repository Commits Sha Comments
      description: Post projects repository commits sha comments.
      operationId: postV3ProjectsIdRepositoryCommitsShaComments
      x-api-path-slug: v3projectsidrepositorycommitsshacomments-post
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: formData
        name: line
        description: The line number
      - in: formData
        name: line_type
        description: The type of the line
      - in: formData
        name: note
        description: The text of the comment
      - in: formData
        name: path
        description: The file path
      - in: path
        name: sha
        description: The commits SHA
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
      - Comments
  /v3/projects/{id}/repository/commits/{sha}/cherry_pick:
    post:
      summary: Post Projects Repository Commits Sha Cherry Pick
      description: Post projects repository commits sha cherry pick.
      operationId: postV3ProjectsIdRepositoryCommitsShaCherryPick
      x-api-path-slug: v3projectsidrepositorycommitsshacherry-pick-post
      parameters:
      - in: formData
        name: branch
        description: The name of the branch
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: sha
        description: A commit sha to be cherry picked
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Commits
      - Sha
      - Cherry
      - Pick
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---