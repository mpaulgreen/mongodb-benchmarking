- 3 shards
  - 1st Run
  ```
    /work $ curl -X GET http://localhost:9090/benchmark/120/60
  {
    "noOfExecutions" : 1030775,
    "noOfFailures" : 0,
    "minResponseTime" : {
      "index" : 238080,
      "responseTime" : 1
    },
    "maxResponseTime" : {
      "index" : 37,
      "responseTime" : 811
    },
    "averageResponseTime" : 6,
    "percentile95" : 11,
    "percentile99" : 27,
    "totalTimeMillis" : 6635351,
    "elapsedTimeMillis" : 120004,
    "requestsPerSecond" : 8589.0
  }
  ```

  - 2nd Run
  ```
  /work $ curl -X GET http://localhost:9090/benchmark/120/60
{
  "noOfExecutions" : 981674,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 31373,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 494271,
    "responseTime" : 151
  },
  "averageResponseTime" : 6,
  "percentile95" : 11,
  "percentile99" : 41,
  "totalTimeMillis" : 6675097,
  "elapsedTimeMillis" : 120006,
  "requestsPerSecond" : 8180.0
}
  ```
