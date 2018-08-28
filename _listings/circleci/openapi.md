swagger: "2.0"
x-collection-name: CircleCI
x-complete: 1
info:
  title: CircleCI
  description: the-circleci-api-is-a-restful-fullyfeatured-api-that-allows-you-to-do-almost-anything-in-circleci--you-can-access-all-information-and-trigger-all-actions--the-only-thing-we-dont-provide-access-to-is-billing-functions-which-must-be-done-from-the-circleci-web-ui-
  version: 1.0.0
host: circleci.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /project/{username}/{project}/{build_num}:
    get:
      summary: Get Project Username Project Build Num
      description: |-
        Full details for a single build. The response includes all of the fields from the build summary.
        This is also the payload for the [notification webhooks](/docs/configuration/#notify), in which case this object is the value to a key named 'payload'.
      operationId: getProjectUsernameProjectBuildNum
      x-api-path-slug: projectusernameprojectbuild-num-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Build
      - Num
    parameters:
      summary: Parameters Project Username Project Build Num
      description: Parameters project username project build num.
      operationId: parametersProjectUsernameProjectBuildNum
      x-api-path-slug: projectusernameprojectbuild-num-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Build
      - Num
  /project/{username}/{project}/{build_num}/artifacts:
    get:
      summary: Get Project Username Project Build Num Artifacts
      description: Get project username project build num artifacts.
      operationId: getProjectUsernameProjectBuildNumArtifacts
      x-api-path-slug: projectusernameprojectbuild-numartifacts-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Build
      - Num
      - Artifacts
    parameters:
      summary: Parameters Project Username Project Build Num Artifacts
      description: Parameters project username project build num artifacts.
      operationId: parametersProjectUsernameProjectBuildNumArtifacts
      x-api-path-slug: projectusernameprojectbuild-numartifacts-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Build
      - Num
      - Artifacts
  /project/{username}/{project}/{build_num}/cancel:
    parameters:
      summary: Parameters Project Username Project Build Num Cancel
      description: Parameters project username project build num cancel.
      operationId: parametersProjectUsernameProjectBuildNumCancel
      x-api-path-slug: projectusernameprojectbuild-numcancel-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Build
      - Num
      - Cancel
    post:
      summary: Add Project Username Project Build Num Cancel
      description: Cancels the build, returns a summary of the build.
      operationId: postProjectUsernameProjectBuildNumCancel
      x-api-path-slug: projectusernameprojectbuild-numcancel-post
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Build
      - Num
      - Cancel
  /project/{username}/{project}/{build_num}/retry:
    parameters:
      summary: Parameters Project Username Project Build Num Retry
      description: Parameters project username project build num retry.
      operationId: parametersProjectUsernameProjectBuildNumRetry
      x-api-path-slug: projectusernameprojectbuild-numretry-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Build
      - Num
      - Retry
    post:
      summary: Add Project Username Project Build Num Retry
      description: Retries the build, returns a summary of the new build.
      operationId: postProjectUsernameProjectBuildNumRetry
      x-api-path-slug: projectusernameprojectbuild-numretry-post
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Build
      - Num
      - Retry
  /project/{username}/{project}/{build_num}/tests:
    get:
      summary: Get Project Username Project Build Num Tests
      description: |-
        Provides test metadata for a build
        Note: [Learn how to set up your builds to collect test metadata](https://circleci.com/docs/test-metadata/)
      operationId: getProjectUsernameProjectBuildNumTests
      x-api-path-slug: projectusernameprojectbuild-numtests-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Build
      - Num
      - Tests
    parameters:
      summary: Parameters Project Username Project Build Num Tests
      description: Parameters project username project build num tests.
      operationId: parametersProjectUsernameProjectBuildNumTests
      x-api-path-slug: projectusernameprojectbuild-numtests-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Build
      - Num
      - Tests