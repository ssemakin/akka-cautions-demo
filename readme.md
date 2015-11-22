

## WIP: Getting memory corruption while updating state in different actors

Integrity failure (object corrupted):

    18:05:33.911 [stateful-demo-akka.actor.default-dispatcher-3] ERROR akkasharedstate.CheckingActor - all must be the same, actual --
    [ SharedImmutable(8740495492422823386,8740495492422823386,8740495492422823386,-3204019457423353804,-3204019457423353804,-3204019457423353804,-3204019457423353804,-3204019457423353804,-3204019457423353804,-3204019457423353804) ]
    [ List(8740495492422823386, 8740495492422823386, 8740495492422823386, -3204019457423353804, -3204019457423353804, -3204019457423353804, -3204019457423353804, -3204019457423353804, -3204019457423353804, -3204019457423353804) ]

Content check failure (entire object changed):

    scala> 17:58:13.412 [stateful-demo-akka.actor.default-dispatcher-21] ERROR akkasharedstate.CheckingActor - all must be [ -7705714603026718025 ], actual --
    [ SharedImmutable(8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937,8985176291945559937) ]
    [ List(8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937, 8985176291945559937) ]

--
