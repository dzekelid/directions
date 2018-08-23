{
  "info": {
    "name": "BC Route Planner Get the directions, path, distance and travel time between a series of geographic points",
    "_postman_id": "f6402ecc-bcd9-426b-8c0d-224c2cfec433",
    "description": "Represents the turn-by-turn directions, geometry, distance, and time of the shortest path or fastest path between given start and end points",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Directions",
      "item": [
        {
          "id": "0cded133-9c59-4b19-8c15-d09627d7811e",
          "name": "represents-the-turnbyturn-directions-geometry-distance-and-time-of-the-shortest-path-or-fastest-path",
          "request": {
            "url": {
              "protocol": "http",
              "host": "router.api.gov.bc.ca",
              "path": [
                "directions.:outputFormat"
              ],
              "query": [
                {
                  "key": "criteria",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "distanceUnit",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "outputSRS",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "points",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "routeDescription",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "outputFormat",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Represents the turn-by-turn directions, geometry, distance, and time of the shortest path or fastest path between given start and end points"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5954d274-6f7b-498d-a512-6fd5a2df275d"
            }
          ]
        }
      ]
    }
  ]
}