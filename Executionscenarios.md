- With data distribution 3 shards (4 GB 4 CPU)
```
/work $ curl -X GET http://localhost:9090/benchmark/120/60

{
  "noOfExecutions" : 1223072,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 10522,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 693178,
    "responseTime" : 171
  },
  "averageResponseTime" : 5,
  "percentile95" : 9,
  "percentile99" : 19,
  "totalTimeMillis" : 6541209,
  "elapsedTimeMillis" : 120006,
  "requestsPerSecond" : 10191.0
}
```

-  With data distribution across 6 shards (4 GB 4 CPU)
```
/work $ curl -X GET http://localhost:9090/benchmark/120/60
{
  "noOfExecutions" : 1243126,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 216368,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 34,
    "responseTime" : 774
  },
  "averageResponseTime" : 5,
  "percentile95" : 13,
  "percentile99" : 26,
  "totalTimeMillis" : 6551768,
  "elapsedTimeMillis" : 120014,
  "requestsPerSecond" : 10358.0
}
```


- Sharding output

```
Totals
{
  data: '208.94MiB',
  docs: 1244860,
  chunks: 12,
  'Shard kogito-sharded-mongo-0': [
    '16.71 % data',
    '16.71 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-3': [
    '16.64 % data',
    '16.64 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [
    '16.66 % data',
    '16.66 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-4': [
    '16.69 % data',
    '16.69 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-5': [
    '16.64 % data',
    '16.64 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-1': [
    '16.63 % data',
    '16.63 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

