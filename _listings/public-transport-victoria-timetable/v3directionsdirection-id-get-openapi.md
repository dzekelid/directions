---
swagger: "2.0"
x-collection-name: Public Transport Victoria Timetable
x-complete: 0
info:
  title: PTV Timetable API - Version 3 Get V3 Directions Direction
  description: View all routes for a direction of travel.
  termsOfService: http://ptv.vic.gov.au/ptv-timetable-api/
  contact:
    name: Public Transport Victoria
    url: http://ptv.vic.gov.au/digital
  version: v3
host: timetableapi.ptv.vic.gov.au
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/directions/route/{route_id}:
    get:
      summary: Get V3 Directions Route Route
      description: View directions that a route travels in.
      operationId: Directions_ForRoute
      x-api-path-slug: v3directionsrouteroute-id-get
      parameters:
      - in: query
        name: devid
        description: Your developer id
      - in: path
        name: route_id
        description: Identifier of route; values returned by Routes API - v3/routes
      - in: query
        name: signature
        description: Authentication signature for request
      - in: query
        name: token
        description: Please ignore
      responses:
        200:
          description: OK
      tags:
      - Directions
      - Route
      - Route
      - Id
  /v3/directions/{direction_id}:
    get:
      summary: Get V3 Directions Direction
      description: View all routes for a direction of travel.
      operationId: Directions_ForDirection
      x-api-path-slug: v3directionsdirection-id-get
      parameters:
      - in: query
        name: devid
        description: Your developer id
      - in: path
        name: direction_id
        description: Identifier of direction of travel; values returned by Directions
          API - /v3/directions/route/{route_id}
      - in: query
        name: signature
        description: Authentication signature for request
      - in: query
        name: token
        description: Please ignore
      responses:
        200:
          description: OK
      tags:
      - Directions
      - Direction
      - Id
  /v3/directions/{direction_id}/route_type/{route_type}:
    get:
      summary: Get V3 Directions Direction Route Type Route Type
      description: View all routes of a particular type for a direction of travel.
      operationId: Directions_ForDirectionAndType
      x-api-path-slug: v3directionsdirection-idroute-typeroute-type-get
      parameters:
      - in: query
        name: devid
        description: Your developer id
      - in: path
        name: direction_id
        description: Identifier of direction of travel; values returned by Directions
          API - /v3/directions/route/{route_id}
      - in: path
        name: route_type
        description: Number identifying transport mode; values returned via RouteTypes
          API
      - in: query
        name: signature
        description: Authentication signature for request
      - in: query
        name: token
        description: Please ignore
      responses:
        200:
          description: OK
      tags:
      - Directions
      - Direction
      - Id
      - Route
      - Type
      - Route
      - Type
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