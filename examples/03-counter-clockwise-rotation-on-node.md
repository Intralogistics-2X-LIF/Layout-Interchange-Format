# 3 Counter-clockwise Rotation on Node

Two edges (straight line) between two nodes. The mobile robot may only move forward oriented on both edges; rotation counter-clockwise is allowed at node N2.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_03",
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
                                        0.0
                                    ],
                                    "rotationAtStartNodeAllowed": "NONE",
                                    "rotationAtEndNodeAllowed": "CCW"
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
                                    ],
                                    "rotationAtStartNodeAllowed": "CCW",
                                    "rotationAtEndNodeAllowed": "NONE"
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

> **Note:** The LIF 1.0 prose stated the rotation node as N1, contradicting its own JSON (both edges mark N1 as NONE and N2 as CCW); the prose has been corrected to N2.
