<details>
	<summary> rs.status output before (from 1st machine that is primary) </summary>
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
	<summary> rs.config output before  (from 1st machine that is primary) </summary>
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

<details>
	<summary> rs.status output after (from 2nd machine that became primary) </summary>
	rs0:PRIMARY> rs.status()
	{
		"set" : "rs0",
		"date" : ISODate("2019-11-01T19:08:04.224Z"),
		"myState" : 1,
		"term" : NumberLong(2),
		"syncingTo" : "",
		"syncSourceHost" : "",
		"syncSourceId" : -1,
		"heartbeatIntervalMillis" : NumberLong(2000),
		"majorityVoteCount" : 2,
		"writeMajorityCount" : 2,
		"optimes" : {
			"lastCommittedOpTime" : {
				"ts" : Timestamp(1572635278, 4),
				"t" : NumberLong(2)
			},
			"lastCommittedWallTime" : ISODate("2019-11-01T19:07:58.652Z"),
			"readConcernMajorityOpTime" : {
				"ts" : Timestamp(1572635278, 4),
				"t" : NumberLong(2)
			},
			"readConcernMajorityWallTime" : ISODate("2019-11-01T19:07:58.652Z"),
			"appliedOpTime" : {
				"ts" : Timestamp(1572635278, 4),
				"t" : NumberLong(2)
			},
			"durableOpTime" : {
				"ts" : Timestamp(1572635278, 4),
				"t" : NumberLong(2)
			},
			"lastAppliedWallTime" : ISODate("2019-11-01T19:07:58.652Z"),
			"lastDurableWallTime" : ISODate("2019-11-01T19:07:58.652Z")
		},
		"lastStableRecoveryTimestamp" : Timestamp(1572635238, 1),
		"lastStableCheckpointTimestamp" : Timestamp(1572635238, 1),
		"electionCandidateMetrics" : {
			"lastElectionReason" : "stepUpRequestSkipDryRun",
			"lastElectionDate" : ISODate("2019-11-01T19:01:57.438Z"),
			"termAtElection" : NumberLong(2),
			"lastCommittedOpTimeAtElection" : {
				"ts" : Timestamp(1572634913, 1),
				"t" : NumberLong(1)
			},
			"lastSeenOpTimeAtElection" : {
				"ts" : Timestamp(1572634913, 1),
				"t" : NumberLong(1)
			},
			"numVotesNeeded" : 2,
			"priorityAtElection" : 1,
			"electionTimeoutMillis" : NumberLong(10000),
			"priorPrimaryMemberId" : 0,
			"numCatchUpOps" : NumberLong(-2059649328),
			"newTermStartDate" : ISODate("2019-11-01T19:01:58.382Z"),
			"wMajorityWriteAvailabilityDate" : ISODate("2019-11-01T19:01:59.871Z")
		},
		"members" : [
			{
				"_id" : 0,
				"name" : "machine1:27017",
				"ip" : "172.31.84.74",
				"health" : 0,
				"state" : 8,
				"stateStr" : "(not reachable/healthy)",
				"uptime" : 0,
				"optime" : {
					"ts" : Timestamp(0, 0),
					"t" : NumberLong(-1)
				},
				"optimeDurable" : {
					"ts" : Timestamp(0, 0),
					"t" : NumberLong(-1)
				},
				"optimeDate" : ISODate("1970-01-01T00:00:00Z"),
				"optimeDurableDate" : ISODate("1970-01-01T00:00:00Z"),
				"lastHeartbeat" : ISODate("2019-11-01T19:08:00.832Z"),
				"lastHeartbeatRecv" : ISODate("2019-11-01T19:01:56.496Z"),
				"pingMs" : NumberLong(0),
				"lastHeartbeatMessage" : "Error connecting to machine1:27017 (172.31.84.74:27017) :: caused by :: No route to host",
				"syncingTo" : "",
				"syncSourceHost" : "",
				"syncSourceId" : -1,
				"infoMessage" : "",
				"configVersion" : -1
			},
			{
				"_id" : 1,
				"name" : "machine2:27017",
				"ip" : "172.31.81.3",
				"health" : 1,
				"state" : 1,
				"stateStr" : "PRIMARY",
				"uptime" : 4507,
				"optime" : {
					"ts" : Timestamp(1572635278, 4),
					"t" : NumberLong(2)
				},
				"optimeDate" : ISODate("2019-11-01T19:07:58Z"),
				"syncingTo" : "",
				"syncSourceHost" : "",
				"syncSourceId" : -1,
				"infoMessage" : "",
				"electionTime" : Timestamp(1572634917, 1),
				"electionDate" : ISODate("2019-11-01T19:01:57Z"),
				"configVersion" : 1,
				"self" : true,
				"lastHeartbeatMessage" : ""
			},
			{
				"_id" : 2,
				"name" : "machine3:27017",
				"ip" : "172.31.95.185",
				"health" : 1,
				"state" : 2,
				"stateStr" : "SECONDARY",
				"uptime" : 4191,
				"optime" : {
					"ts" : Timestamp(1572635278, 4),
					"t" : NumberLong(2)
				},
				"optimeDurable" : {
					"ts" : Timestamp(1572635278, 4),
					"t" : NumberLong(2)
				},
				"optimeDate" : ISODate("2019-11-01T19:07:58Z"),
				"optimeDurableDate" : ISODate("2019-11-01T19:07:58Z"),
				"lastHeartbeat" : ISODate("2019-11-01T19:08:03.568Z"),
				"lastHeartbeatRecv" : ISODate("2019-11-01T19:08:04.006Z"),
				"pingMs" : NumberLong(0),
				"lastHeartbeatMessage" : "",
				"syncingTo" : "machine2:27017",
				"syncSourceHost" : "machine2:27017",
				"syncSourceId" : 1,
				"infoMessage" : "",
				"configVersion" : 1
			}
		],
		"ok" : 1,
		"$clusterTime" : {
			"clusterTime" : Timestamp(1572635278, 4),
			"signature" : {
				"hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
				"keyId" : NumberLong(0)
			}
		},
		"operationTime" : Timestamp(1572635278, 4)
	}
	
</details>

<details>
	<summary> rs.config output after (from 2nd machine that became primary) </summary>
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
Screenshot of chat before shutdown 1st machine:

![alt text](https://i.imgur.com/2jQI21g.png)

After:

![alt_text](https://i.imgur.com/Uu337gr.png)
