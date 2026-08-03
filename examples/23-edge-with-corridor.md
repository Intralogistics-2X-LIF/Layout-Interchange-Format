# 23 Edge with Corridor

An edge (straight line) between two nodes where the mobile robot is permitted to deviate sideways, within a corridor of defined width to the left and right, referenced to its kinematic center.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_23",
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
                                    ],
                                    "allowedDeviationXY": {
                                        "aMinimum": 0.4,
                                        "bMinimum": 0.25,
                                        "aMaximum": 0.4,
                                        "bMaximum": 0.25,
                                        "theta": 0.0
                                    }
                                }
                            ]
                        },
                        {
                            "nodeId": "N2",
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
                                    ],
                                    "allowedDeviationXY": {
                                        "aMinimum": 0.4,
                                        "bMinimum": 0.25,
                                        "aMaximum": 0.4,
                                        "bMaximum": 0.25,
                                        "theta": 0.0
                                    }
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
                                    "mobileRobotOrientations": [
                                        0.0
                                    ],
                                    "orientationType": "TANGENTIAL",
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