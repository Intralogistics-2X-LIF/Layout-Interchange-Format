# 15 Rack Station Modelled by Three Stations

Rack station with three levels modelled by three individual stations.

![](assets/png/15-rack-station-modelled-by-three-stations.png)

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_15",
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
                        }
                    ],
                    "stations": [
                        {
                            "stationId": "S01_Level_A",
                            "interactionNodeIds": [
                                "N1"
                            ],
                            "stationName": "Shelf on Level A",
                            "stationDescriptor": "Shelf on level A",
                            "stationHeight": 0.0
                        },
                        {
                            "stationId": "S01_Level_B",
                            "interactionNodeIds": [
                                "N1"
                            ],
                            "stationName": "Shelf on Level B",
                            "stationDescriptor": "Shelf on level B",
                            "stationHeight": 2.5
                        },
                        {
                            "stationId": "S01_Level_C",
                            "interactionNodeIds": [
                                "N1"
                            ],
                            "stationName": "Shelf on Level C",
                            "stationDescriptor": "Shelf on level C",
                            "stationHeight": 5.0
                        }
                    ]
                }
            ]
        }
    ]
}
```

> **Note:** The LIF 1.0 example used the inconsistent stationId `S01_Level_2` for the level C shelf; corrected to `S01_Level_C`.
