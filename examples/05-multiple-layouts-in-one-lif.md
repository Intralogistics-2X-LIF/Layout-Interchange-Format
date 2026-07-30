# 5 Multiple Layouts in One LIF

Two layouts in one LIF file, representing two different levels of the facility. Each layout references its own origin, reflecting that the levels are located on different levels of the facility.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_05",
        "creator": "VDMA",
        "exportTimestamp": "2026-09-28T10:00:00.00Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_Level_0",
            "originDescriptor": "Origin of the ground level",
            "layouts": [
                {
                    "layoutId": "Layout_Ground_Level",
                    "layoutName": "Name of Layout Ground Level",
                    "layoutVersion": "1",
                    "layoutLevelId": "0",
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
                                    ]
                                }
                            ]
                        }
                    ]
                }
            ]
        },
        {
            "originId": "Origin_Level_1",
            "originDescriptor": "Origin of the upper level",
            "layouts": [
                {
                    "layoutId": "Layout_Upper_Level",
                    "layoutName": "Name of Layout Upper Level",
                    "layoutVersion": "1",
                    "layoutLevelId": "1",
                    "layoutDescriptor": "Upper level of Customer",
                    "nodes": [
                        {
                            "nodeId": "N101",
                            "mapId": "Map_Z-Level_2",
                            "nodePosition": {
                                "x": 12.4,
                                "y": 3.4
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
                            "nodeId": "N102",
                            "mapId": "Map_Z-Level_2",
                            "nodePosition": {
                                "x": 12.0,
                                "y": 3.4
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
                            "edgeId": "N101-N102",
                            "startNodeId": "N101",
                            "endNodeId": "N102",
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
                    ]
                }
            ]
        }
    ]
}
```

> **Note:** Migration note: in LIF 1.0 all layouts implicitly shared one global origin. In LIF 2.0 each level is assigned its own origin with a distinct originId, since the two levels lie in different planes of the facility.
