- Document that is been written
```
  {
    id: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf',  # hashed - Chosen for shard key
    name: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf',
    description: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf'
  }
```

- Commands to shard
```
sh.enableSharding("fruits")
db.demo.fruit.ensureIndex({_id: "hashed"})
sh.shardCollection("fruits.demo.fruit",{"_id":"hashed"})


```
- Sharding output
```
    collections: {
      'fruit.fruit': {
        shardKey: { id: 'hashed' },
        unique: false,
        balancing: true,
        chunkMetadata: [
          { shard: 'kogito-sharded-mongo-0', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-1', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-2', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-3', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-4', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-5', nChunks: 2 }
        ],
        chunks: [
          { min: { id: MinKey() }, max: { id: Long("-7686143364045646500") }, 'on shard': 'kogito-sharded-mongo-0', 'last modified': Timestamp({ t: 1, i: 0 }) },
          { min: { id: Long("-7686143364045646500") }, max: { id: Long("-6148914691236517200") }, 'on shard': 'kogito-sharded-mongo-0', 'last modified': Timestamp({ t: 1, i: 1 }) },
          { min: { id: Long("-6148914691236517200") }, max: { id: Long("-4611686018427387900") }, 'on shard': 'kogito-sharded-mongo-1', 'last modified': Timestamp({ t: 1, i: 2 }) },
          { min: { id: Long("-4611686018427387900") }, max: { id: Long("-3074457345618258600") }, 'on shard': 'kogito-sharded-mongo-1', 'last modified': Timestamp({ t: 1, i: 3 }) },
          { min: { id: Long("-3074457345618258600") }, max: { id: Long("-1537228672809129300") }, 'on shard': 'kogito-sharded-mongo-2', 'last modified': Timestamp({ t: 1, i: 4 }) },
          { min: { id: Long("-1537228672809129300") }, max: { id: Long("0") }, 'on shard': 'kogito-sharded-mongo-2', 'last modified': Timestamp({ t: 1, i: 5 }) },
          { min: { id: Long("0") }, max: { id: Long("1537228672809129300") }, 'on shard': 'kogito-sharded-mongo-3', 'last modified': Timestamp({ t: 1, i: 6 }) },
          { min: { id: Long("1537228672809129300") }, max: { id: Long("3074457345618258600") }, 'on shard': 'kogito-sharded-mongo-3', 'last modified': Timestamp({ t: 1, i: 7 }) },
          { min: { id: Long("3074457345618258600") }, max: { id: Long("4611686018427387900") }, 'on shard': 'kogito-sharded-mongo-4', 'last modified': Timestamp({ t: 1, i: 8 }) },
          { min: { id: Long("4611686018427387900") }, max: { id: Long("6148914691236517200") }, 'on shard': 'kogito-sharded-mongo-4', 'last modified': Timestamp({ t: 1, i: 9 }) },
          { min: { id: Long("6148914691236517200") }, max: { id: Long("7686143364045646500") }, 'on shard': 'kogito-sharded-mongo-5', 'last modified': Timestamp({ t: 1, i: 10 }) },
          { min: { id: Long("7686143364045646500") }, max: { id: MaxKey() }, 'on shard': 'kogito-sharded-mongo-5', 'last modified': Timestamp({ t: 1, i: 11 }) }
        ],
        tags: []
      }
    }
  }
```

- Further configs
```
sh.shardCollection('fruit.fruit',{'id':'hashed'}, {numInitialChunks: 1000}) //with 6 shards

```

```
db.demo.fruit.getShardDistribution()
```

```
Shard kogito-sharded-mongo-1 at kogito-sharded-mongo-1/kogito-sharded-mongo-1-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-1-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '0B',
  docs: 0,
  chunks: 2,
  'estimated data per chunk': '0B',
  'estimated docs per chunk': 0
}
---
Shard kogito-sharded-mongo-0 at kogito-sharded-mongo-0/kogito-sharded-mongo-0-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-0-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '0B',
  docs: 0,
  chunks: 2,
  'estimated data per chunk': '0B',
  'estimated docs per chunk': 0
}
---
Shard kogito-sharded-mongo-3 at kogito-sharded-mongo-3/kogito-sharded-mongo-3-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-3-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '0B',
  docs: 0,
  chunks: 2,
  'estimated data per chunk': '0B',
  'estimated docs per chunk': 0
}
---
Shard kogito-sharded-mongo-2 at kogito-sharded-mongo-2/kogito-sharded-mongo-2-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-2-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '256.2MiB',
  docs: 1767476,
  chunks: 2,
  'estimated data per chunk': '128.1MiB',
  'estimated docs per chunk': 883738
}
---
Totals
{
  data: '256.2MiB',
  docs: 1767476,
  chunks: 8,
  'Shard kogito-sharded-mongo-1': [ '0 % data', '0 % docs in cluster', '0B avg obj size on shard' ],
  'Shard kogito-sharded-mongo-0': [ '0 % data', '0 % docs in cluster', '0B avg obj size on shard' ],
  'Shard kogito-sharded-mongo-3': [ '0 % data', '0 % docs in cluster', '0B avg obj size on shard' ],
  'Shard kogito-sharded-mongo-2': [
    '100 % data',
    '100 % docs in cluster',
    '152B avg obj size on shard'
  ]
}
```