swagger: "2.0"
x-collection-name: CollabNet
x-complete: 1
info:
  title: Foundation API
  version: 1.0.0
basePath: /ctfrest/foundation/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /projects/requests/count:
    get:
      summary: Gets the number of pending project requests
      description: Gets the number of pending project requests.
      operationId: getProjectRequestCount
      x-api-path-slug: projectsrequestscount-get
      responses:
        200:
          description: OK
      tags:
      - Number
      - Of
      - Pending
      - Project
      - Requests