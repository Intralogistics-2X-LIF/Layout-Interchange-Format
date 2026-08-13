# 19 Forward Edge with Two Mobile Robot Types with Differing Orientation

One edge (straight line) between two nodes, where two different mobile robot types from the same integrator must adopt different orientations.

![](assets/png/19-forward-edge-with-two-mobile-robot-types.png)

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_19",
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
                                "x": 0.0,
                                "y": 0.0
                            },
                            "mobileRobotTypeNodeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        },
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
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
                                        },
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
                                        0.0
                                    ],
                                    "rotationAtStartNodeAllowed": "NONE",
                                    "rotationAtEndNodeAllowed": "NONE"
                                },
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
                                        1.5708
                                    ],
                                    "rotationAtStartNodeAllowed": "NONE",
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

> **Note:** The node properties are identical for both types and therefore merged into one entry via the `mobileRobotTypes` array; the edge properties differ per type (differing orientation) and therefore remain separate entries.
