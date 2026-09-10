# 16 Rack Station Modelled by Three Nodes

Rack station with three levels modelled by three different nodes:

* Node NA is only for picking a load.
* Node NB is only for dropping a load.
* Node NC is for picking and dropping a load.

![](assets/png/16-rack-station-modelled-by-three-nodes.png)

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_16",
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
                            "nodeId": "NA",
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
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "pick",
                                            "blockingType": "HARD"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "nodeId": "NB",
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
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "drop",
                                            "blockingType": "HARD"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "nodeId": "NC",
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
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "pick",
                                            "blockingType": "HARD"
                                        },
                                        {
                                            "actionType": "drop",
                                            "blockingType": "HARD"
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
                                    ]
                                }
                            ]
                        }
                    ],
                    "edges": [
                        {
                            "edgeId": "NA-N2",
                            "startNodeId": "NA",
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
                            "edgeId": "N2-NA",
                            "startNodeId": "N2",
                            "endNodeId": "NA",
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
                            "edgeId": "NB-N2",
                            "startNodeId": "NB",
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
                            "edgeId": "N2-NB",
                            "startNodeId": "N2",
                            "endNodeId": "NB",
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
                            "edgeId": "NC-N2",
                            "startNodeId": "NC",
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
                            "edgeId": "N2-NC",
                            "startNodeId": "N2",
                            "endNodeId": "NC",
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
                        }
                    ],
                    "stations": [
                        {
                            "stationId": "S01_Level_A",
                            "interactionNodeIds": [
                                "NA"
                            ],
                            "stationName": "Shelf on Level A",
                            "stationDescriptor": "Handover shelf from manual trucks. Inbound toward mobile robot system only.",
                            "stationHeight": 0.0
                        },
                        {
                            "stationId": "S01_Level_B",
                            "interactionNodeIds": [
                                "NB"
                            ],
                            "stationName": "Shelf on Level B",
                            "stationDescriptor": "Handover shelf toward manual trucks. Outbound away from mobile robot system only.",
                            "stationHeight": 2.5
                        },
                        {
                            "stationId": "S01_Level_C",
                            "interactionNodeIds": [
                                "NC"
                            ],
                            "stationName": "Shelf on Level C",
                            "stationDescriptor": "Special bi-directional handover shelf.",
                            "stationHeight": 5.0
                        }
                    ]
                }
            ]
        }
    ]
}
```

> **Note:** The LIF 1.0 example contained a copy-paste error (edge `NB-N2` with `startNodeId` `NA`); corrected to `NB`.
