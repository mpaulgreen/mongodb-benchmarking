- Document that is been written
```
  {
    id: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf',  UUID # hashed - Chosen for shard key
    name: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf',
    description: 'c9b2c8e6-fd7f-4153-bb2e-3a724f0597cf'
  }
```

- Commands to shard
```
sh.enableSharding("fruits")
db.demo.fruit.ensureIndex({id: "hashed"})
sh.shardCollection("fruits.demo.fruit",{"id":"hashed"})
```
- sh.status()
```
shardingVersion
{
  _id: 1,
  minCompatibleVersion: 5,
  currentVersion: 6,
  clusterId: ObjectId("61e968ba821d210257a808ab")
}
---
shards
[
  {
    _id: 'kogito-sharded-mongo-0',
    host: 'kogito-sharded-mongo-0/kogito-sharded-mongo-0-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-0-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-0-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017',
    state: 1
  },
  {
    _id: 'kogito-sharded-mongo-1',
    host: 'kogito-sharded-mongo-1/kogito-sharded-mongo-1-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-1-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-1-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017',
    state: 1
  },
  {
    _id: 'kogito-sharded-mongo-2',
    host: 'kogito-sharded-mongo-2/kogito-sharded-mongo-2-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-2-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-2-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017',
    state: 1
  }
]
---
active mongoses
[ { '4.4.0': 2 } ]
---
autosplit
{ 'Currently enabled': 'yes' }
---
balancer
{
  'Currently enabled': 'yes',
  'Currently running': 'no',
  'Failed balancer rounds in last 5 attempts': 0,
  'Migration Results for the last 24 hours': { '513': 'Success' }
}
---
databases
[
  {
    database: { _id: 'config', primary: 'config', partitioned: true },
    collections: {
      'config.system.sessions': {
        shardKey: { _id: 1 },
        unique: false,
        balancing: true,
        chunkMetadata: [
          { shard: 'kogito-sharded-mongo-0', nChunks: 511 },
          { shard: 'kogito-sharded-mongo-1', nChunks: 256 },
          { shard: 'kogito-sharded-mongo-2', nChunks: 257 }
        ],
        chunks: [
          'too many chunks to print, use verbose if you want to force print'
        ],
        tags: []
      }
    }
  },
  {
    database: {
      _id: 'fruits',
      primary: 'kogito-sharded-mongo-1',
      partitioned: true,
      version: {
        uuid: UUID("fa23b514-cb0e-4547-bc51-77b24beecc88"),
        lastMod: 1
      }
    },
    collections: {
      'fruits.demo.fruit': {
        shardKey: { id: 'hashed' },
        unique: false,
        balancing: true,
        chunkMetadata: [
          { shard: 'kogito-sharded-mongo-0', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-1', nChunks: 2 },
          { shard: 'kogito-sharded-mongo-2', nChunks: 2 }
        ],
        chunks: [
          { min: { id: MinKey() }, max: { id: Long("-6148914691236517204") }, 'on shard': 'kogito-sharded-mongo-0', 'last modified': Timestamp({ t: 1, i: 0 }) },
          { min: { id: Long("-6148914691236517204") }, max: { id: Long("-3074457345618258602") }, 'on shard': 'kogito-sharded-mongo-0', 'last modified': Timestamp({ t: 1, i: 1 }) },
          { min: { id: Long("-3074457345618258602") }, max: { id: Long("0") }, 'on shard': 'kogito-sharded-mongo-1', 'last modified': Timestamp({ t: 1, i: 2 }) },
          { min: { id: Long("0") }, max: { id: Long("3074457345618258602") }, 'on shard': 'kogito-sharded-mongo-1', 'last modified': Timestamp({ t: 1, i: 3 }) },
          { min: { id: Long("3074457345618258602") }, max: { id: Long("6148914691236517204") }, 'on shard': 'kogito-sharded-mongo-2', 'last modified': Timestamp({ t: 1, i: 4 }) },
          { min: { id: Long("6148914691236517204") }, max: { id: MaxKey() }, 'on shard': 'kogito-sharded-mongo-2', 'last modified': Timestamp({ t: 1, i: 5 }) }
        ],
        tags: []
      }
    }
  }
]
```

- Data distribution after 2 runs (All the data landed in kogito-sharded-mongo-1)
```
Shard kogito-sharded-mongo-0 at kogito-sharded-mongo-0/kogito-sharded-mongo-0-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-0-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-0-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '0B',
  docs: 0,
  chunks: 2,
  'estimated data per chunk': '0B',
  'estimated docs per chunk': 0
}
---
Shard kogito-sharded-mongo-1 at kogito-sharded-mongo-1/kogito-sharded-mongo-1-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-1-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-1-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '292.26MiB',
  docs: 2016188,
  chunks: 2,
  'estimated data per chunk': '146.13MiB',
  'estimated docs per chunk': 1008094
}
---
Shard kogito-sharded-mongo-2 at kogito-sharded-mongo-2/kogito-sharded-mongo-2-0.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-2-1.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017,kogito-sharded-mongo-2-2.kogito-sharded-mongo-sh.mongodb.svc.cluster.local:27017
{
  data: '0B',
  docs: 0,
  chunks: 2,
  'estimated data per chunk': '0B',
  'estimated docs per chunk': 0
}
---
Totals
{
  data: '292.26MiB',
  docs: 2016188,
  chunks: 6,
  'Shard kogito-sharded-mongo-0': [ '0 % data', '0 % docs in cluster', '0B avg obj size on shard' ],
  'Shard kogito-sharded-mongo-1': [
    '100 % data',
    '100 % docs in cluster',
    '152B avg obj size on shard'
  ],
  'Shard kogito-sharded-mongo-2': [ '0 % data', '0 % docs in cluster', '0B avg obj size on shard' ]
}
```
