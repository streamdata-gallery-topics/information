---
swagger: "2.0"
x-collection-name: Browshot
x-complete: 1
info:
  title: Browshot
  description: take-screenshots-of-any-website-in-real-time
  termsOfService: https://browshot.com/terms
  contact:
    name: API Support
    url: https://browshot.com/contact
    email: support@browshot.com
  version: 1.17.0
host: api.browshot.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /account/info:
    get:
      summary: Get information about your account
      description: Get information about your account.
      operationId: GetAccountInfo
      x-api-path-slug: accountinfo-get
      parameters:
      - in: query
        name: details
        description: level of information returned
      responses:
        200:
          description: OK
      tags:
      - Account
      - Info
  /batch/info:
    get:
      summary: Get the batch status
      description: Get the status of a batch requested through the API or through
        the dashboard.
      operationId: GetBatchInfo
      x-api-path-slug: batchinfo-get
      parameters:
      - in: query
        name: id
        description: batch ID
      responses:
        200:
          description: OK
      tags:
      - Batch
      - Info
  /browser/info:
    get:
      summary: Get information about a browser
      description: Get information about a browser.
      operationId: GetBrowserInfo
      x-api-path-slug: browserinfo-get
      parameters:
      - in: query
        name: id
        description: browser ID
      responses:
        200:
          description: OK
      tags:
      - Browser
      - Info
  /instance/info:
    get:
      summary: Get information about an instance
      description: Get information about an instance.
      operationId: GetInstanceInfo
      x-api-path-slug: instanceinfo-get
      parameters:
      - in: query
        name: id
        description: instance ID
      responses:
        200:
          description: OK
      tags:
      - Instance
      - Info
  /screenshot/info:
    get:
      summary: Query screenshot status
      description: Once a screenshot has been requested, its status must be checked
        until it is either "error" or "finished".
      operationId: GetScreenshotInfo
      x-api-path-slug: screenshotinfo-get
      parameters:
      - in: query
        name: details
        description: level of details about the screenshot and the page
      - in: query
        name: id
        description: screenshot ID received from /api/v1/screenshot/create
      responses:
        200:
          description: OK
      tags:
      - Screenshot
      - Info
---