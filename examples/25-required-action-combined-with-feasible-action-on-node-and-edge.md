# 25 Required Action Combined with Feasible Action(s) on a Node and Edge

One edge (straight line) connects two nodes. Both the node and the edge combine an action the mobile robot must take with one it may optionally take when driving through the node.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_25",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.000Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_1",
            "originDescriptor": "Ground level of Customer",
            "layouts": [
                {
                    "layoutId": "Layout_Ground_Level",
                    "layoutName": "Name of Layout Ground Level",
                    "layoutVersion": "1",
                    "nodes": [
                        {
                            "nodeId": "N1",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 0.0,
                                "y": 0.0
                            },
                            "mobileRobotTypeNodeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "nodeId": "N2",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 11.0,
                                "y": 0.0
                            },
                            "mobileRobotTypeNodeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "requiredActions": [
                                        {
                                            "actionType": "pick",
                                            "blockingType": "HARD"
                                        }
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "beep",
                                            "actionDescriptor": "Section where the fleet control system could instruct the mobile robot to beep",
                                            "blockingType": "SOFT"
                                        }
                                    ]
                                }
                            ]
                        }
                    ],
                    "edges": [
                        {
                            "edgeId": "N1-N2",
                            "startNodeId": "N1",
                            "endNodeId": "N2",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "mobileRobotOrientations": [
                                        0.0
                                    ],
                                    "orientationType": "TANGENTIAL",
                                    "requiredActions": [
                                        {
                                            "actionType": "lowerForks",
                                            "actionDescriptor": "Section where the fleet control system must tell the mobile robot to lower forks ahead of the pick at N2",
                                            "blockingType": "HARD"
                                        }
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "beep",
                                            "actionDescriptor": "Section where the fleet control system could instruct the mobile robot to beep",
                                            "blockingType": "SOFT"
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                }
            ]
        }
    ]
}
```