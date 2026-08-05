# 8 Station with Two Nodes, Restricted for Different Mobile Robot Types

Station with two nodes, but restricted for different mobile robot types.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_08",
        "creator": "VDMA",
        "exportTimestamp": "2026-09-28T10:00:00.000Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_1",
            "layouts": [
                {
                    "layoutId": "Layout_Ground_Level",
                    "layoutName": "Name of Layout Ground Level",
                    "layoutVersion": "1",
                    "layoutDescriptor": "Ground level of Customer",
                    "nodes": [
                        {
                            "nodeId": "N1",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 7.2,
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
                                "x": 9.2,
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
                                            "actionType": "drop",
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
                        },
                        {
                            "nodeId": "N3",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 9.6,
                                "y": 0.0
                            },
                            "mobileRobotTypeNodeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
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
                        },
                        {
                            "nodeId": "N4",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 14.8,
                                "y": 3.4
                            },
                            "mobileRobotTypeNodeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
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
                                    "orientationType": "TANGENTIAL",
                                    "reachOrientationBeforeEntering": true,
                                    "mobileRobotOrientations": [
                                        3.14159
                                    ]
                                }
                            ]
                        },
                        {
                            "edgeId": "N2-N1",
                            "startNodeId": "N2",
                            "endNodeId": "N1",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "orientationType": "TANGENTIAL",
                                    "reachOrientationBeforeEntering": true,
                                    "mobileRobotOrientations": [
                                        0.0
                                    ]
                                }
                            ]
                        },
                        {
                            "edgeId": "N4-N3",
                            "startNodeId": "N4",
                            "endNodeId": "N3",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "orientationType": "TANGENTIAL",
                                    "reachOrientationBeforeEntering": true,
                                    "mobileRobotOrientations": [
                                        3.14159
                                    ]
                                }
                            ]
                        },
                        {
                            "edgeId": "N3-N4",
                            "startNodeId": "N3",
                            "endNodeId": "N4",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "orientationType": "TANGENTIAL",
                                    "reachOrientationBeforeEntering": true,
                                    "mobileRobotOrientations": [
                                        0.0
                                    ]
                                }
                            ]
                        }
                    ],
                    "stations": [
                        {
                            "stationId": "S01",
                            "interactionNodeIds": [
                                "N2",
                                "N3"
                            ],
                            "stationName": "HANDOVER_01",
                            "stationDescriptor": "Handover station for pallet",
                            "stationHeight": 0.0
                        }
                    ]
                }
            ]
        }
    ]
}
```

> **Note:** The LIF 1.0 example named this station SOURCE_01 despite describing it as a handover station; renamed to HANDOVER_01.
