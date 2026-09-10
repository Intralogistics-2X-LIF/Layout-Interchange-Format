# 28 Base LIF for Order Examples

A base layout reused by the following order examples: one edge between two nodes permitting travel in either direction with a corridor, and a node where charging is optional.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_29",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.000Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_1",
            "layouts": [
                {
                    "layoutId": "Layout_Ground_Level",
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
                                    "feasibleActions": [
                                        {
                                            "actionType": "startCharging",
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
                                    "orientationType": "TANGENTIAL",
                                    "mobileRobotOrientations": [
                                        0.0,
                                        3.141592653589793
                                    ],
                                    "reachOrientationBeforeEntering": true,
                                    "corridor": {
                                        "maximumLeftWidth": 0.5,
                                        "maximumRightWidth": 0.5,
                                        "corridorReferencePoint": "KINEMATIC_CENTER"
                                    }
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

The following order examples are all valid against this Base LIF.