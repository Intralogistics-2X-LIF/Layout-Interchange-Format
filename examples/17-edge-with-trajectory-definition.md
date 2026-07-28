# 17 Edge with Trajectory Definition

Two edges between node N1 and N2 with a half circle trajectory. Before entering the edge N1 to N2 the mobile robot needs to rotate on N1 to -90°. The mobile robot will maintain the -90° while moving on the edge. Before entering the edge N2 to N1 the mobile robot needs to rotate to 90°. The mobile robot will maintain the 90° while moving on the edge.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_17",
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
                        },
                        {
                            "nodeId": "N2",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 15.0,
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
                                        -1.5708
                                    ],
                                    "rotationAtStartNodeAllowed": "BOTH",
                                    "rotationAtEndNodeAllowed": "BOTH",
                                    "trajectory": {
                                        "degree": 2,
                                        "knotVector": [
                                            0,
                                            0,
                                            0,
                                            0.5,
                                            1,
                                            1,
                                            1
                                        ],
                                        "controlPoints": [
                                            {
                                                "x": 5.0,
                                                "y": 0.0
                                            },
                                            {
                                                "x": 5.0,
                                                "y": 5.0
                                            },
                                            {
                                                "x": 15.0,
                                                "y": 5.0
                                            },
                                            {
                                                "x": 15.0,
                                                "y": 0.0
                                            }
                                        ]
                                    }
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
                                        1.5708
                                    ],
                                    "rotationAtStartNodeAllowed": "BOTH",
                                    "rotationAtEndNodeAllowed": "BOTH",
                                    "trajectory": {
                                        "degree": 2,
                                        "knotVector": [
                                            0,
                                            0,
                                            0,
                                            0.5,
                                            1,
                                            1,
                                            1
                                        ],
                                        "controlPoints": [
                                            {
                                                "x": 15.0,
                                                "y": 0.0
                                            },
                                            {
                                                "x": 15.0,
                                                "y": -5.0
                                            },
                                            {
                                                "x": 5.0,
                                                "y": -5.0
                                            },
                                            {
                                                "x": 5.0,
                                                "y": 0.0
                                            }
                                        ]
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

> **Note:** The LIF 1.0 example's control points ran from (0, 0) to (3.6, 0) and therefore did not connect the actual node positions. The trajectories have been recalculated so the curves start and end at N1 (5, 0) and N2 (15, 0).
