swagger: "2.0"
x-collection-name: Public Transport Victoria Timetable
x-complete: 1
info:
  title: Public Transport Victoria Timetable
  description: the-ptv-timetable-api-provides-direct-access-to-public-transport-victorias-public-transport-timetable-data--the-api-returns-scheduled-timetable-route-and-stop-data-for-all-metropolitan-and-regional-train-tram-and-bus-services-in-victoria-including-night-networknight-train-and-night-tram-data-are-included-in-metropolitan-train-and-tram-services-data-respectively-whereas-night-bus-is-a-separate-route-type--the-api-also-returns-realtime-data-for-metropolitan-train-tram-and-bus-services-where-this-data-is-made-available-to-ptv-as-well-as-disruption-information-stop-facility-information-and-access-to-myki-ticket-outlet-data-
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