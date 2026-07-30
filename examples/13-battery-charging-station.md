# 13 Battery Charging Station

Modelling of a battery charging station.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_13",
        "creator": "VDMA",
        "exportTimestamp": "2026-09-28T10:00:00.00Z",
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
                            "nodeId": "N_CHARGER",
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
                                    ],
                                    "feasibleActions": [
                                        {
                                            "actionType": "startCharging",
                                            "blockingType": "HARD"
                                        },
                                        {
                                            "actionType": "stopCharging",
                                            "blockingType": "HARD"
                                        }
                                    ]
                                }
                            ]
                        },
                        {
                            "nodeId": "N1",
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
                            "edgeId": "N_CHARGER-N1",
                            "startNodeId": "N_CHARGER",
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
                                        3.14159
                                    ],
                                    "rotationAtStartNodeAllowed": "NONE",
                                    "rotationAtEndNodeAllowed": "BOTH",
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": false
                                    }
                                }
                            ]
                        },
                        {
                            "edgeId": "N1-N_CHARGER",
                            "startNodeId": "N1",
                            "endNodeId": "N_CHARGER",
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
                                    ],
                                    "rotationAtStartNodeAllowed": "BOTH",
                                    "rotationAtEndNodeAllowed": "NONE",
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": false
                                    }
                                }
                            ]
                        }
                    ],
                    "stations": [
                        {
                            "stationId": "N_CHARGER",
                            "interactionNodeIds": [
                                "N_CHARGER"
                            ],
                            "stationName": "Battery Charging Station",
                            "stationDescriptor": "Station to charge the battery or park the mobile robot",
                            "stationHeight": 0.0
                        }
                    ]
                }
            ]
        }
    ]
}
```
