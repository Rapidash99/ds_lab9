<details>
	<summary> rs.status output </summary>
	rs0:PRIMARY> rs.status()
	{
		"set" : "rs0",
		"date" : ISODate("2019-11-01T18:18:31.788Z"),
		"myState" : 1,
		"term" : NumberLong(1),
		"syncingTo" : "",
		"syncSourceHost" : "",
		"syncSourceId" : -1,
		"heartbeatIntervalMillis" : NumberLong(2000),
		"majorityVoteCount" : 2,
		"writeMajorityCount" : 2,
		"optimes" : {
			"lastCommittedOpTime" : {
				"ts" : Timestamp(1572632303, 1),
				"t" : NumberLong(1)
			},
			"lastCommittedWallTime" : ISODate("2019-11-01T18:18:23.309Z"),
			"readConcernMajorityOpTime" : {
				"ts" : Timestamp(1572632303, 1),
				"t" : NumberLong(1)
			},
			"readConcernMajorityWallTime" : ISODate("2019-11-01T18:18:23.309Z"),
			"appliedOpTime" : {
				"ts" : Timestamp(1572632303, 1),
				"t" : NumberLong(1)
			},
			"durableOpTime" : {
				"ts" : Timestamp(1572632303, 1),
				"t" : NumberLong(1)
			},
			"lastAppliedWallTime" : ISODate("2019-11-01T18:18:23.309Z"),
			"lastDurableWallTime" : ISODate("2019-11-01T18:18:23.309Z")
		},
		"lastStableRecoveryTimestamp" : Timestamp(1572632303, 1),
		"lastStableCheckpointTimestamp" : Timestamp(1572632303, 1),
		"electionCandidateMetrics" : {
			"lastElectionReason" : "electionTimeout",
			"lastElectionDate" : ISODate("2019-11-01T17:58:22.768Z"),
			"termAtElection" : NumberLong(1),
			"lastCommittedOpTimeAtElection" : {
				"ts" : Timestamp(0, 0),
				"t" : NumberLong(-1)
			},
			"lastSeenOpTimeAtElection" : {
				"ts" : Timestamp(1572631092, 1),
				"t" : NumberLong(-1)
			},
			"numVotesNeeded" : 2,
			"priorityAtElection" : 1,
			"electionTimeoutMillis" : NumberLong(10000),
			"numCatchUpOps" : NumberLong(27017),
			"newTermStartDate" : ISODate("2019-11-01T17:58:23.276Z"),
			"wMajorityWriteAvailabilityDate" : ISODate("2019-11-01T17:58:24.134Z")
		},
		"members" : [
			{
				"_id" : 0,
				"name" : "machine1:27017",
				"ip" : "172.31.84.74",
				"health" : 1,
				"state" : 1,
				"stateStr" : "PRIMARY",
				"uptime" : 1582,
				"optime" : {
					"ts" : Timestamp(1572632303, 1),
					"t" : NumberLong(1)
				},
				"optimeDate" : ISODate("2019-11-01T18:18:23Z"),
				"syncingTo" : "",
				"syncSourceHost" : "",
				"syncSourceId" : -1,
				"infoMessage" : "",
				"electionTime" : Timestamp(1572631102, 1),
				"electionDate" : ISODate("2019-11-01T17:58:22Z"),
				"configVersion" : 1,
				"self" : true,
				"lastHeartbeatMessage" : ""
			},
			{
				"_id" : 1,
				"name" : "machine2:27017",
				"ip" : "172.31.81.3",
				"health" : 1,
				"state" : 2,
				"stateStr" : "SECONDARY",
				"uptime" : 1219,
				"optime" : {
					"ts" : Timestamp(1572632303, 1),
					"t" : NumberLong(1)
				},
				"optimeDurable" : {
					"ts" : Timestamp(1572632303, 1),
					"t" : NumberLong(1)
				},
				"optimeDate" : ISODate("2019-11-01T18:18:23Z"),
				"optimeDurableDate" : ISODate("2019-11-01T18:18:23Z"),
				"lastHeartbeat" : ISODate("2019-11-01T18:18:31.318Z"),
				"lastHeartbeatRecv" : ISODate("2019-11-01T18:18:30.335Z"),
				"pingMs" : NumberLong(0),
				"lastHeartbeatMessage" : "",
				"syncingTo" : "machine1:27017",
				"syncSourceHost" : "machine1:27017",
				"syncSourceId" : 0,
				"infoMessage" : "",
				"configVersion" : 1
			},
			{
				"_id" : 2,
				"name" : "machine3:27017",
				"ip" : "172.31.95.185",
				"health" : 1,
				"state" : 2,
				"stateStr" : "SECONDARY",
				"uptime" : 1219,
				"optime" : {
					"ts" : Timestamp(1572632303, 1),
					"t" : NumberLong(1)
				},
				"optimeDurable" : {
					"ts" : Timestamp(1572632303, 1),
					"t" : NumberLong(1)
				},
				"optimeDate" : ISODate("2019-11-01T18:18:23Z"),
				"optimeDurableDate" : ISODate("2019-11-01T18:18:23Z"),
				"lastHeartbeat" : ISODate("2019-11-01T18:18:31.318Z"),
				"lastHeartbeatRecv" : ISODate("2019-11-01T18:18:30.335Z"),
				"pingMs" : NumberLong(0),
				"lastHeartbeatMessage" : "",
				"syncingTo" : "machine1:27017",
				"syncSourceHost" : "machine1:27017",
				"syncSourceId" : 0,
				"infoMessage" : "",
				"configVersion" : 1
			}
		],
		"ok" : 1,
		"$clusterTime" : {
			"clusterTime" : Timestamp(1572632303, 1),
			"signature" : {
				"hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
				"keyId" : NumberLong(0)
			}
		},
		"operationTime" : Timestamp(1572632303, 1)
	}

</details>

<details>
	<summary> rs.config output </summary>
	rs0:PRIMARY> rs.config()
	{
		"_id" : "rs0",
		"version" : 1,
		"protocolVersion" : NumberLong(1),
		"writeConcernMajorityJournalDefault" : true,
		"members" : [
			{
				"_id" : 0,
				"host" : "machine1:27017",
				"arbiterOnly" : false,
				"buildIndexes" : true,
				"hidden" : false,
				"priority" : 1,
				"tags" : {
					
				},
				"slaveDelay" : NumberLong(0),
				"votes" : 1
			},
			{
				"_id" : 1,
				"host" : "machine2:27017",
				"arbiterOnly" : false,
				"buildIndexes" : true,
				"hidden" : false,
				"priority" : 1,
				"tags" : {
					
				},
				"slaveDelay" : NumberLong(0),
				"votes" : 1
			},
			{
				"_id" : 2,
				"host" : "machine3:27017",
				"arbiterOnly" : false,
				"buildIndexes" : true,
				"hidden" : false,
				"priority" : 1,
				"tags" : {
					
				},
				"slaveDelay" : NumberLong(0),
				"votes" : 1
			}
		],
		"settings" : {
			"chainingAllowed" : true,
			"heartbeatIntervalMillis" : 2000,
			"heartbeatTimeoutSecs" : 10,
			"electionTimeoutMillis" : 10000,
			"catchUpTimeoutMillis" : -1,
			"catchUpTakeoverDelayMillis" : 30000,
			"getLastErrorModes" : {
				
			},
			"getLastErrorDefaults" : {
				"w" : 1,
				"wtimeout" : 0
			},
			"replicaSetId" : ObjectId("5dbc7234ecd3fae5b24d45ae")
		}
	}
</details>

![alt text](https://i.imgur.com/2jQI21g.png)
