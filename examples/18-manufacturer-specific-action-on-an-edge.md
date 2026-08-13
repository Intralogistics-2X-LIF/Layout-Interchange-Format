# 18 Manufacturer Specific Action on an Edge

Manufacturer specific action on an edge.

![](assets/png/18-manufacturer-specific-action-on-an-edge.png)

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_18",
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
                                    "feasibleActions": [
                                        {
                                            "actionType": "BEEP",
                                            "actionDescriptor": "Section where the (third-party) fleet control system could instruct the mobile robot to beep",
                                            "blockingType": "SOFT"
                                        }
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
                                        3.14159
                                    ],
                                    "requiredActions": [
                                        {
                                            "actionType": "LOWER_FORK_AND_BEEP",
                                            "actionDescriptor": "Section where the (third-party) fleet control system must tell the mobile robot to lower forks and beep",
                                            "blockingType": "SOFT"
                                        }
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
