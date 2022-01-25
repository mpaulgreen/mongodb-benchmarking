- 1 shard with 500M of Memory and .5 CPU
```
{
  "noOfExecutions" : 140211,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 5117,
    "responseTime" : 2
  },
  "maxResponseTime" : {
    "index" : 117260,
    "responseTime" : 399
  },
  "averageResponseTime" : 50,
  "percentile95" : 98,
  "percentile99" : 105,
  "totalTimeMillis" : 7075488,
  "elapsedTimeMillis" : 120009,
  "requestsPerSecond" : 1168.0
```

- Data Distribution after 2 runs
```
---
Totals
{
  data: '46.76MiB',
  docs: 278619,
  chunks: 2,
  'Shard kogito-sharded-mongo-0': [
    '100 % data',
    '100 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

- 3 shards with 500M of Memory and .5 CPU
```

{
  "noOfExecutions" : 229576,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 51986,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 11,
    "responseTime" : 1981
  },
  "averageResponseTime" : 30,
  "percentile95" : 91,
  "percentile99" : 97,
  "totalTimeMillis" : 7049182,
  "elapsedTimeMillis" : 120008,
  "requestsPerSecond" : 1913.0
```
- Data Distribution after 2 runs
```
---
Totals
{
  data: '79.76MiB',
  docs: 475248,
  chunks: 6,
  'Shard kogito-sharded-mongo-1': [
    '33.27 % data',
    '33.27 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [
    '33.34 % data',
    '33.34 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-0': [
    '33.38 % data',
    '33.38 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

- 6 shards Cluster with 500m of memory and .5 CPU  
```


{
  "noOfExecutions" : 370774,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 12941,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 190545,
    "responseTime" : 191
  },
  "averageResponseTime" : 18,
  "percentile95" : 82,
  "percentile99" : 90,
  "totalTimeMillis" : 6978341,
  "elapsedTimeMillis" : 120076,
  "requestsPerSecond" : 3087.0
```

- Data distribution after 2 runs
```
---
Totals
{
  data: '123.87MiB',
  docs: 738025,
  chunks: 12,
  'Shard kogito-sharded-mongo-1': [
    '16.62 % data',
    '16.62 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-4': [
    '16.62 % data',
    '16.62 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-3': [
    '16.73 % data',
    '16.73 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-5': [
    '16.69 % data',
    '16.69 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [
    '16.69 % data',
    '16.69 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-0': [
    '16.61 % data',
    '16.61 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

- 9 shards with 500M of Memory and .5 CPU

```

{
  "noOfExecutions" : 457271,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 2705,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 312247,
    "responseTime" : 184
  },
  "averageResponseTime" : 15,
  "percentile95" : 71,
  "percentile99" : 85,
  "totalTimeMillis" : 6951246,
  "elapsedTimeMillis" : 120039,
  "requestsPerSecond" : 3809.0
}
```

- Data distribution after 2 runs
```
---
Totals
{
  data: '153.76MiB',
  docs: 916107,
  chunks: 18,
  'Shard kogito-sharded-mongo-2': [
    '11.1 % data',
    '11.1 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-4': [
    '11.16 % data',
    '11.16 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-8': [
    '11.08 % data',
    '11.08 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-3': [
    '11.04 % data',
    '11.04 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-7': [
    '11.12 % data',
    '11.12 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-1': [
    '11.17 % data',
    '11.17 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-0': [
    '11.11 % data',
    '11.11 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-5': [
    '11.11 % data',
    '11.11 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-6': [
    '11.06 % data',
    '11.06 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

- 21 shards with 500M of Memory and .5 CPU
```

{
  "noOfExecutions" : 750810,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 16786,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 223266,
    "responseTime" : 243
  },
  "averageResponseTime" : 9,
  "percentile95" : 39,
  "percentile99" : 66,
  "totalTimeMillis" : 6798934,
  "elapsedTimeMillis" : 120056,
  "requestsPerSecond" : 6253.0
```

- Data distribution after 2 runs
```
---
Totals
{
  data: '251.01MiB',
  docs: 1495521,
  chunks: 42,
  'Shard kogito-sharded-mongo-11': [
    '4.79 % data',
    '4.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-12': [
    '4.74 % data',
    '4.74 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-14': [
    '4.74 % data',
    '4.74 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-19': [
    '4.75 % data',
    '4.75 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-13': [
    '4.76 % data',
    '4.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-9': [
    '4.73 % data',
    '4.73 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-7': [
    '4.77 % data',
    '4.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-18': [
    '4.79 % data',
    '4.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-4': [
    '4.77 % data',
    '4.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-5': [
    '4.77 % data',
    '4.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-10': [
    '4.78 % data',
    '4.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-16': [
    '4.72 % data',
    '4.72 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-3': [
    '4.77 % data',
    '4.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-6': [
    '4.76 % data',
    '4.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-17': [
    '4.76 % data',
    '4.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-8': [
    '4.76 % data',
    '4.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [
    '4.75 % data',
    '4.75 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-20': [
    '4.74 % data',
    '4.74 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-15': [
    '4.74 % data',
    '4.74 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-0': [
    '4.76 % data',
    '4.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-1': [
    '4.74 % data',
    '4.74 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```


- 36 shards

```
/work $ curl -X GET http://localhost:9090/benchmark/120/60
{
  "noOfExecutions" : 903573,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 325556,
    "responseTime" : 1
  },
  "maxResponseTime" : {
    "index" : 835013,
    "responseTime" : 187
  },
  "averageResponseTime" : 7,
  "percentile95" : 24,
  "percentile99" : 59,
  "totalTimeMillis" : 6732901,
  "elapsedTimeMillis" : 120013,
  "requestsPerSecond" : 7528.0
}
```

- Data distribution after 2 runs
```
Totals
{
  data: '301.78MiB',
  docs: 1797992,
  chunks: 72,
  'Shard kogito-sharded-mongo-29': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-1': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-15': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-3': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-19': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-14': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-24': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-30': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-20': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-12': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-16': [
    '2.8 % data',
    '2.8 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-21': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-32': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-26': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-22': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-35': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-9': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-33': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-11': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-8': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-31': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-0': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-23': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-25': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-18': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-10': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-13': [
    '2.78 % data',
    '2.78 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-34': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-27': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-28': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-7': [
    '2.75 % data',
    '2.75 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-6': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-17': [
    '2.76 % data',
    '2.76 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-4': [
    '2.79 % data',
    '2.79 % docs in cluster',
    '176B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-5': [
    '2.77 % data',
    '2.77 % docs in cluster',
    '176B avg obj size on shard'
  ]
}
```

- 48 shards
```
{
  "noOfExecutions" : 1091337,
  "noOfFailures" : 0,
  "minResponseTime" : {
    "index" : 414,
    "responseTime" : 2
  },
  "maxResponseTime" : {
    "index" : 585379,
    "responseTime" : 173
  },
  "averageResponseTime" : 6,
  "percentile95" : 11,
  "percentile99" : 44,
  "totalTimeMillis" : 6637778,
  "elapsedTimeMillis" : 120021,
  "requestsPerSecond" : 9092.0
```

- Data distribution after 4 runs
```

```