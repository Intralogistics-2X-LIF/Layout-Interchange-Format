# 21 Node with allowedDeviationXY as a Fixed Ellipse

Node N2 defines an allowedDeviationXY with different minimum and maximum values for a and b, permitting the mobile robot to deviate within an ellipse around the node position.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_21",
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
                                    ]
                                }
                            ]
                        },
                        {
                            "nodeId": "N2",
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
                                    ],
                                    "allowedDeviationXY": {
                                        "aMinimum": 0.3,
                                        "bMinimum": 0.2,
                                        "aMaximum": 0.6,
                                        "bMaximum": 0.4,
                                        "theta": 0.0
                                    }
                                }
                            ]
                        },
                        {
                            "nodeId": "N3",
                            "mapId": "Map_Z-Level_1",
                            "nodePosition": {
                                "x": 7.0,
                                "y": 3.0
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
                                    "mobileRobotOrientations": [
                                        0.0
                                    ],
                                    "orientationType": "TANGENTIAL"
                                }
                            ]
                        },
                        {
                            "edgeId": "N2-N3",
                            "startNodeId": "N2",
                            "endNodeId": "N3",
                            "mobileRobotTypeEdgeProperties": [
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_1"
                                        }
                                    ],
                                    "mobileRobotOrientations": [
                                        0.9827937232
                                    ],
                                    "orientationType": "TANGENTIAL"
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