# 20 One Origin with Two Layouts

Two layouts share the same origin and overlap in space. A single station connects them, with one interaction node in each layout, so the mobile robot can approach it from either side.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_20",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.000Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_1",
            "originDescriptor": "Ground-level origin shared by both layouts.",
            "layouts": [
                {
                    "layoutId": "Layout_A",
                    "layoutName": "Approach from the West",
                    "layoutVersion": "1",
                    "layoutDescriptor": "Ground level of Customer",
                    "nodes": [
                        {
                            "nodeId": "N1_A",
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
                            "nodeId": "N2_A",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 5.0,
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
                        }
                    ],
                    "edges": [
                        {
                            "edgeId": "N1_A-N2_A",
                            "startNodeId": "N1_A",
                            "endNodeId": "N2_A",
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
                                    "reachOrientationBeforeEntering": true
                                }
                            ]
                        }
                    ]
                },
                {
                    "layoutId": "Layout_B",
                    "layoutName": "Approach from the East",
                    "layoutVersion": "1",
                    "layoutDescriptor": "Ground level of Customer",
                    "nodes": [
                        {
                            "nodeId": "N1_B",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 10.0,
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
                            "nodeId": "N2_B",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 7.0,
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
                                    "feasibleActions": [
                                        {
                                            "actionType": "pick",
                                            "blockingType": "HARD",
                                            "actionParameters": [
                                                {
                                                    "key": "loadType",
                                                    "value": "Example load type"
                                                }
                                            ]
                                        }
                                    ]
                                }
                            ]
                        }
                    ],
                    "edges": [
                        {
                            "edgeId": "N1_B-N2_B",
                            "startNodeId": "N1_B",
                            "endNodeId": "N2_B",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "mobileRobotOrientations": [
                                        3.141592653589793
                                    ],
                                    "orientationType": "TANGENTIAL"
                                }
                            ]
                        },
                        {
                            "edgeId": "N2_B-N2_A",
                            "startNodeId": "N2_B",
                            "endNodeId": "N2_A",
                            "edgeDescriptor": "Connects the station's two interaction nodes.",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "mobileRobotOrientations": [
                                        3.141592653589793
                                    ],
                                    "orientationType": "TANGENTIAL"
                                }
                            ]
                        }
                    ],
                    "stations": [
                        {
                            "stationId": "S01",
                            "interactionNodeIds": [
                                "N2_A",
                                "N2_B"
                            ],
                            "stationName": "SOURCE_01",
                            "stationDescriptor": "Lane Drop-Off",
                            "stationHeight": 0.55
                        }
                    ]
                }
            ]
        }
    ]
}
```