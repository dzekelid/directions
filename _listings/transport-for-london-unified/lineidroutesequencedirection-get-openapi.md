---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 0
info:
  title: Transport for London Unified Line  Route  Sequence direction
  description: Gets all valid routes for given line id, including the sequence of
    stops on each route..
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Line/{id}/Route/Sequence/{direction}:
    get:
      summary: Line  Route  Sequence direction
      description: Gets all valid routes for given line id, including the sequence
        of stops on each route..
      operationId: Line_RouteSequence
      x-api-path-slug: lineidroutesequencedirection-get
      parameters:
      - in: path
        name: direction
        description: The direction of travel
      - in: query
        name: excludeCrowding
        description: That excludes crowding from line disruptions
      - in: path
        name: id
        description: A single line id e
      - in: query
        name: serviceTypes
        description: A comma seperated list of service types to filter on
      responses:
        200:
          description: OK
      tags:
      - Line
      - ""
      - Route
      - ""
      - Sequence
      - Direction
  /StopPoint/{id}/DirectionTo/{toStopPointId}:
    get:
      summary: Stop Point  Direction To to Stop Point Id
      description: Returns the canonical direction, "inbound" or "outbound", for a
        given pair of stop point ids in the direction from -&gt; to..
      operationId: StopPoint_Direction
      x-api-path-slug: stoppointiddirectiontotostoppointid-get
      parameters:
      - in: path
        name: id
        description: Originating stop id (station naptan code e
      - in: query
        name: lineId
        description: Optional line id filter e
      - in: path
        name: toStopPointId
        description: Destination stop id (station naptan code e
      responses:
        200:
          description: OK
      tags:
      - Stop
      - Point
      - ""
      - Direction
      - To
      - Stop
      - Point
      - Id
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