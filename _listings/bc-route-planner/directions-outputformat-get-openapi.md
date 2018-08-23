---
swagger: "2.0"
x-collection-name: BC Route Planner
x-complete: 0
info:
  title: BC Route Planner Get the directions, path, distance and travel time between
    a series of geographic points
  description: Represents the turn-by-turn directions, geometry, distance, and time
    of the shortest path or fastest path between given start and end points
  termsOfService: http://www.data.gov.bc.ca/local/dbc/docs/license/API_Terms_of_Use.pdf
  contact:
    name: Data BC
    url: https://forms.gov.bc.ca/databc-contact-us/
    email: DataBCBA@gov.bc.ca
  version: 1.2.0
host: router.api.gov.bc.ca
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /directions.{outputFormat}:
    get:
      summary: Get the directions, path, distance and travel time between a series
        of geographic points
      description: Represents the turn-by-turn directions, geometry, distance, and
        time of the shortest path or fastest path between given start and end points
      operationId: represents-the-turnbyturn-directions-geometry-distance-and-time-of-the-shortest-path-or-fastest-path
      x-api-path-slug: directions-outputformat-get
      parameters:
      - in: query
        name: criteria
        description: Routing criteria to optimize (e
      - in: query
        name: distanceUnit
        description: distance unit of measure (e
      - in: path
        name: outputFormat
        description: Format of representation
      - in: query
        name: outputSRS
        description: The EPSG code of the spatial reference system (SRS) to use for
          output geometries
      - in: query
        name: points
        description: 'Example: -123'
      - in: query
        name: routeDescription
        description: Route description (e
      responses:
        200:
          description: OK
      tags:
      - Directions
      - OutputFormat
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