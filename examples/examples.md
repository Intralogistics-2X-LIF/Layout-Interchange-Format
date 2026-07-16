# 11 Examples

**Note:** The examples are kept simple, thus optional attributes (e.g. trajectory) are not defined for most.

## 11.1 Forward Edge

One Edge (straight line) between two nodes. The mobile robot may only move forward oriented on this edge.

![](assets/fig11_1-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 01",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId":"Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
            "nodes": [
                {
                    "nodeId": "N1",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N2",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 11.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.2 Bidirectional Edge

Two Edges (straight line) between two nodes. The mobile robot may only move forward oriented on one edge and backward oriented on the other edge.

![](assets/fig11_2-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 02",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId":"Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
            "nodes": [
                {
                    "nodeId": "N1",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N2",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 11.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        }
    ]
}
```
## 11.3 Counter-clockwise Rotation on Node

Two Edges (straight line) between two nodes. The mobile robot may only move forward oriented on both edge, rotation counter-clockwise allowed at node N1.

![](assets/fig11_3-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 03",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientation": 0.0,
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "CCW",
                            "rotationAtEndNodeAllowed": "NONE"
                        }
                    ]
                }
            ]
        }
    ]
}
```
## 11.4 Omnidirectional Edge

Two Edges (straight line) between two nodes. The mobile robot moves omnidirectionally to 90° on the edge from N1 to N2 and the mobile robot moves omnidirectionally back to -90° on the edge from N2 back to N1.

![](assets/fig11_4-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 04",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [1.5707963267948966],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": false,
                            "rotationAtStartNodeAllowed": "NONE",
                            "rotationAtEndNodeAllowed": "NONE"
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientation": -1.5707963267948966,
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": false,
                            "rotationAtStartNodeAllowed": "NONE",
                            "rotationAtEndNodeAllowed": "NONE"
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.5 Multiple Layouts in One LIF

Two layouts in one LIF file, representing two different levels of the facility.

![](assets/fig11_5-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 05",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutLevelId": "0",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        },
        {
            "layoutId": "Layout_Upper_Level",
            "layoutName": "Name of Layout Upper Level",
            "layoutVersion": "1",
            "layoutLevelId": "1",
            "layoutdescriptor": "Upper level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.6 Station with One Node

Two Edges (straight line) between two nodes. At one node there is a station for picking up pallets. The mobile robot may only move forward oriented on one edge and backward oriented on the other edge.

![](fig11_6-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 06",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ],
            "stations": [
                {
                    "stationId": "S01",
                    "interactionNodeIds": [
                        "N2"
                    ],
                    "stationName": "SOURCE_01",
                    "stationDescription": "Source to pick up pallet",
                    "stationHeight": "0.55"
                }
            ]
        }
    ]
}
```

## 11.7 Station with Two Nodes

Modelling a Station with two different nodes (e.g. Rotation station for a pallet).

![](assets/fig11_7-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 07",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId":"Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
            "nodes": [
                {
                    "nodeId": "N1",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.2,
                        "y": 3.4
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
                                },
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "N2",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.4,
                        "y": 3.2
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "N3",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N11",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 3.4
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N21",
                    "mapId":"Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N11-N1",
                    "startNodeId": "N11",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N3-N11",
                    "startNodeId": "N3",
                    "endNodeId": "N11",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N1-N3",
                    "startNodeId": "N1",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N3-N21",
                    "startNodeId": "N3",
                    "endNodeId": "N21",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N21-N2",
                    "startNodeId": "N21",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N3",
                    "startNodeId": "N2",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId":"Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ],
            "stations": [
                {
                    "stationId": "S01",
                    "interactionNodeIds": [
                        "N1",
                        "N2"
                    ],
                    "stationName":"SOURCE_01",
                    "stationDescription": "Pallet rotation station",
                    "stationHeight": "0.55"
                }
            ]
        }
    ]
}
```

## 11.8 Station with Two Nodes, Restricted for Different Mobile Robot Types

Station with tow Nodes but restricted for different mobile robot types.

![](assets/fig11_8-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 08",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "N3",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.6,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "N4",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 14.8,
                        "y": 3.4
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N4-N3",
                    "startNodeId": "N4",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N3-N4",
                    "startNodeId": "N3",
                    "endNodeId": "N4",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ],
            "stations": [
                {
                    "stationId": "S01",
                    "interactionNodeIds": [
                        "N2",
                        "N3"
                    ],
                    "stationName": "SOURCE_01",
                    "stationDescription": "Handover station for pallet",
                    "stationHeight": "0.0"
                }
            ]
        }
    ]
}
```

## 11.9 Rotation Station

Rotation station for pallet, on which a rectangular load can be dropped "short side leading" and then picked up "long side leading".

![](assets/fig11_9-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 09",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N11",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "N21",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "theta": -1.5707963268,
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD",
                                    "actionParameters": [
                                        {
                                            "key": "loadType",
                                            "value": "Example load type"
                                        }
                                    ]
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
                        "y": -5.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N1-N11",
                    "startNodeId": "N1",
                    "endNodeId": "N11",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N11-N21",
                    "startNodeId": "N11",
                    "endNodeId": "N21",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "CW"
                        }
                    ]
                },
                {
                    "edgeId": "N21-N2",
                    "startNodeId": "N21",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ],
            "stations": [
                {
                    "stationId": "S01",
                    "interactionNodeIds": [
                        "N11",
                        "N21"
                    ],
                    "stationName": "Rotation_01",
                    "stationDescription": "Rotation station for pallet",
                    "stationHeight": "0.75"
                }
            ]
        }
    ]
}
```

## 11.10 Station with Three Nodes, Restricted to Different Mobile Robot Types

One station with three nodes, but restricted to different mobile robot types.

Restriction on edges:

* Mobile Robot Type 1 Forward
* Mobile Robot Type 2 Backward
* Mobile Robot Type 2 & 3 Forward
* Mobile Robot Type 2 & 3 Backward

Explanation:

* NSL: Mobile Robot Type 1 pick and drop
* NSB: Mobile Robot Type 1 pick
* NSR: Mobile Robot Type 2 drop
* NSR: Mobile Robot Type 3 pick and drop

![](assets/fig11_10-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 10",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "NSL",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "NSR",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 10.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "actions": [
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                }
                            ]
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_3",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                }
                            ]
                        }
                    ]
                },
                {
                    "nodeId": "NSB",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 9.7,
                        "y": -0.5
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
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
                        "x": 9.7,
                        "y": -5.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N3",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 13.2,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2"
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_3"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N1-NSL",
                    "startNodeId": "N1",
                    "endNodeId": "NSL",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "NSL-N1",
                    "startNodeId": "NSL",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-NSB",
                    "startNodeId": "N2",
                    "endNodeId": "NSB",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "NSB-N2",
                    "startNodeId": "NSB",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N3-NSR",
                    "startNodeId": "N3",
                    "endNodeId": "NSR",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_3",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "NSR-N3",
                    "startNodeId": "NSR",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_3",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ],
            "stations": [
                {
                    "stationId": "NS",
                    "interactionNodeIds": [
                        "NSL",
                        "NSB",
                        "NSR"
                    ],
                    "stationName": "Complicated handover station",
                    "stationDescription": "Handover station for multiple mobile robot types with different allowed actions",
                    "stationHeight": "0.5"
                }
            ]
        }
    ]
}
```

## 11.11 Multiple Edges with Load Restrictions

Multiple Edges with different load restrictions applied.

![](assets/fig11_11-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 11",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
            "nodes": [
                {
                    "nodeId": "N0",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "startCharging",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "stopCharging",
                                    "requirementType": "CONDITIONAL",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N3",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 25.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N4",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 35.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N0-N1",
                    "startNodeId": "N0",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                    "edgeId": "N1-N0",
                    "startNodeId": "N1",
                    "endNodeId": "N0",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "NONE",
                            "loadRestriction": {
                                "unloaded": true,
                                "loaded": false
                            }
                        }
                    ]
                },
                {
                    "edgeId": "N1-N2",
                    "startNodeId": "N1",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH"
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH"
                        }
                    ]
                },
                {
                    "edgeId": "N2-N3",
                    "startNodeId": "N2",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH",
                            "loadRestriction": {
                                "unloaded": true,
                                "loaded": true,
                                "loadSetNames": [
                                    "Load_Type_EUR"
                                ]
                            }
                        }
                    ]
                },
                {
                    "edgeId": "N3-N2",
                    "startNodeId": "N3",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH",
                            "loadRestriction": {
                                "unloaded": true,
                                "loaded": true,
                                "loadSetNames": [
                                    "Load_Type_EUR"
                                ]
                            }
                        }
                    ]
                },
                {
                    "edgeId": "N3-N4",
                    "startNodeId": "N3",
                    "endNodeId": "N4",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH",
                            "loadRestriction": {
                                "unloaded": false,
                                "loaded": true,
                                "loadSetNames": [
                                    "Load_Type_EUR"
                                ]
                            }
                        }
                    ]
                },
                {
                    "edgeId": "N4-N3",
                    "startNodeId": "N4",
                    "endNodeId": "N3",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "BOTH",
                            "loadRestriction": {
                                "unloaded": false,
                                "loaded": true,
                                "loadSetNames": [
                                    "Load_Type_EUR"
                                ]
                            }
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.12 Multiple Edges Between Same Two Nodes for Different mobileRobotTypeEdgeProperty Constraints.

If, for example, a mobile robot would be incapable of remembering the properties of the load it is carrying, and/or the traffic controller would be asked to manage the mobile robots' maximumSpeed or other behavior, multiple overlapping edges (or in other cases nodes) can accomplish this.

![](assets/fig11_12-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 12",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
            "nodes": [
                {
                    "nodeId": "N0",
                    "mapId": "Map_Z-Level_1",
                    "nodePosition": {
                        "x": 0.0,
                        "y": 0.0
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "startCharging",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "stopCharging",
                                    "requirementType": "CONDITIONAL",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N0-N1_Unloaded",
                    "startNodeId": "N0",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                    "edgeId": "N1-N0_Stable_Load",
                    "startNodeId": "N1",
                    "endNodeId": "N0",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "NONE",
                            "maximumSpeed": 0.8,
                            "loadRestriction": {
                                "unloaded": false,
                                "loaded": true,
                                "loadSetNames": [
                                    "Stable_Load_Unit"
                                ]
                            }
                        }
                    ]
                },
                {
                    "edgeId": "N1-N0_Unstable_Load",
                    "startNodeId": "N1",
                    "endNodeId": "N0",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "BOTH",
                            "rotationAtEndNodeAllowed": "NONE",
                            "maximumSpeed": 0.3,
                            "loadRestriction": {
                                "unloaded": false,
                                "loaded": true,
                                "loadSetNames": [
                                    "Unstable_Load_Unit"
                                ]
                            }
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.13 Battery Charging Station

Modelling of a battery charging station.

![](assets/fig11_13-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 13",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "startCharging",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "stopCharging",
                                    "requirementType": "CONDITIONAL",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                    "stationDescription": "Station to charge the battery or park the mobile robot",
                    "stationHeight": "0.0"
                }
            ]
        }
    ]
}
```

## 11.14 Two Levels of a Facility in One LIF File

Two layouts in one LIF file, representing two different levels of the facility. Modelling of a transition between two levels.

![](assets/fig11_14-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 14",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutLevelId": "0",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N102",
                    "startNodeId": "N2",
                    "endNodeId": "N102",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        },
        {
            "layoutId": "Layout_Upper_Level",
            "layoutName": "Name of Layout Upper Level",
            "layoutVersion": "1",
            "layoutLevelId": "1",
            "layoutdescriptor": "Upper level of Customer",
            "nodes": [
                {
                    "nodeId": "N102",
                    "mapId": "Map_Z-Level_2",
                    "nodePosition": {
                        "x": 12.4,
                        "y": 3.4
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                },
                {
                    "nodeId": "N101",
                    "mapId": "Map_Z-Level_2",
                    "nodePosition": {
                        "x": 12.0,
                        "y": 3.4
                    },
                    "mobileRobotTypeNodeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        }
                    ]
                }
            ],
            "edges": [
                {
                    "edgeId": "N102-N101",
                    "startNodeId": "N102",
                    "endNodeId": "N101",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N101-N102",
                    "startNodeId": "N101",
                    "endNodeId": "N102",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N102-N2",
                    "startNodeId": "N102",
                    "endNodeId": "N2",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 11.15 Rack Station Modelled by Three Stations

Rack station with three levels modelled by three individual stations.

![](assets/fig11_15-1.png)

LIF-File:
```json 
{
    "metaInformation": {
        "projectIdentification": "LIF Example 15",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "actions": [
                                {
                                    "actionType": "pick",
                                    "requirementType": "CONDITIONAL",
                                    "blockingType": "HARD"
                                },
                                {
                                    "actionType": "drop",
                                    "requirementType": "CONDITIONAL",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
                        }
                    ]
                },
                {
                    "edgeId": "N2-N1",
                    "startNodeId": "N2",
                    "endNodeId": "N1",
                    "mobileRobotTypeEdgeProperties": [
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true
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
                    "stationDescription": "Shelf on level A",
                    "stationHeight": "0.0"
                },
                {
                    "stationId": "S01_Level_B",
                    "interactionNodeIds": [
                        "N1"
                    ],
                    "stationName": "Shelf on Level B",
                    "stationDescription": "Shelf on level B",
                    "stationHeight": "2.5"
                },
                {
                    "stationId": "S01_Level_2",
                    "interactionNodeIds": [
                        "N1"
                    ],
                    "stationName": "Shelf on Level C",
                    "stationDescription": "Shelf on level C",
                    "stationHeight": "5.0"
                }
            ]
        }
    ]
}
```
## 11.16 Rack Station Modelled by Three Nodes

Rack station with three levels modelled by three different nodes:

* Node NA is only for picking a load.
* Node NB is only for dropping a load.
* Node NC is for picking and dropping a load.

![](assets/fig11_16-1.png)

LIF-File:
```json
{
  "metaInformation": {
      "projectIdentification": "LIF Example 16",
      "creator": "VDMA",
      "exportTimestamp": "2023-09-28T10:00:00.00Z",
      "lifVersion": "0.11.0"
  },
  "layouts": [
      {
          "layoutId": "Layout_Ground_Level",
          "layoutName": "Name of Layout Ground Level",
          "layoutVersion": "1",
          "layoutdescriptor": "Ground level of Customer",
          "nodes": [
              {
                  "nodeId": "NA",
                  "mapId": "Map_Z-Level_1",
                  "nodePosition": {
                      "x": 7.2,
                      "y": 0.0
                  },
                  "mobileRobotTypeNodeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "actions": [
                              {
                                  "actionType": "pick",
                                  "requirementType": "CONDITIONAL",
                                  "blockingType": "HARD"
                              }
                          ]
                      }
                  ]
              },
              {
                  "nodeId": "NB",
                  "mapId": "Map_Z-Level_1",
                  "nodePosition": {
                      "x": 7.2,
                      "y": 0.0
                  },
                  "mobileRobotTypeNodeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "actions": [
                              {
                                  "actionType": "drop",
                                  "requirementType": "CONDITIONAL",
                                  "blockingType": "HARD"
                              }
                          ]
                      }
                  ]
              },
              {
                  "nodeId": "NC",
                  "mapId": "Map_Z-Level_1",
                  "nodePosition": {
                      "x": 7.2,
                      "y": 0.0
                  },
                  "mobileRobotTypeNodeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "actions": [
                              {
                                  "actionType": "pick",
                                  "requirementType": "CONDITIONAL",
                                  "blockingType": "HARD"
                              },
                              {
                                  "actionType": "drop",
                                  "requirementType": "CONDITIONAL",
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
                          "mobileRobotTypeId": "Mobile_Robot_Type_1"
                      }
                  ]
              }
          ],
          "edges": [
              {
                  "edgeId": "NA-N2",
                  "startNodeId": "NA",
                  "endNodeId": "N2",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [3.1415926535897931],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              },
              {
                  "edgeId": "N2-NA",
                  "startNodeId": "N2",
                  "endNodeId": "NA",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [0.0],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              },
              {
                  "edgeId": "NB-N2",
                  "startNodeId": "NA",
                  "endNodeId": "N2",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [3.1415926535897931],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              },
              {
                  "edgeId": "N2-NB",
                  "startNodeId": "N2",
                  "endNodeId": "NB",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [0.0],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              },
              {
                  "edgeId": "NC-N2",
                  "startNodeId": "NC",
                  "endNodeId": "N2",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [3.1415926535897931],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              },
              {
                  "edgeId": "N2-NC",
                  "startNodeId": "N2",
                  "endNodeId": "NC",
                  "mobileRobotTypeEdgeProperties": [
                      {
                          "mobileRobotTypeId": "Mobile_Robot_Type_1",
                          "mobileRobotOrientations": [0.0],
                          "orientationType": "TANGENTIAL",
                          "reachOrientationBeforeEntering": true
                      }
                  ]
              }
          ],
          "stations": [
              {
                  "stationId": "S01_Level_A",
                  "interactionNodeIds": [
                      "NA"
                  ],
                  "stationName": "Shelf on Level A",
                  "stationDescription": "Handover shelf from manual trucks (inbound).",
                  "stationHeight": "0.0"
              },
              {
                  "stationId": "S01_Level_B",
                  "interactionNodeIds": [
                      "NB"
                  ],
                  "stationName": "Shelf on Level B",
                  "stationDescription": "Handover shelf toward manual trucks (outbound).",
                  "stationHeight": "2.5"
              },
              {
                  "stationId": "S01_Level_C",
                  "interactionNodeIds": [
                      "NC"
                  ],
                  "stationName": "Shelf on Level C",
                  "stationDescription": "Special bi-directional handover shelf.",
                  "stationHeight": "5.0"
              }
          ]
      }
  ]
}
```
## 11.17 Edge with Trajectory Definition

Two edges between node N1 and N2 with a half circle trajectory. Before entering the edge N1 to N2 the mobile robot needs to rotate on N1 to -90°. The mobile robot will maintain the -90° while moving on the edge. Before entering the edge N2 to N1 the mobile robot needs to rotate to 90°. The mobile robot will maintain the 90° while moving on the edge.

![](assets/fig11_17-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 17",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [-1.5707963267948966],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                                        "x": 0,
                                        "y": 0
                                    },
                                    {
                                        "x": 0,
                                        "y": 1.8
                                    },
                                    {
                                        "x": 3.6,
                                        "y": 1.8
                                    },
                                    {
                                        "x": 3.6,
                                        "y": 0
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [1.5707963267948966],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
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
                                        "x": 3.6,
                                        "y": 0
                                    },
                                    {
                                        "x": 3.6,
                                        "y": -1.8
                                    },
                                    {
                                        "x": 0,
                                        "y": -1.8
                                    },
                                    {
                                        "x": 0,
                                        "y": 0
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
```

## 11.18 Manufacturer Specific Action on an Edge

Manufacturer specific action on an edge.

![](assets/fig11_18-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 18",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "actions": [
                                {
                                    "actionType": "BEEP",
                                    "actionDescriptor": "Section where the (third-party) fleet control system could instruct the mobile robot to beep",
                                    "requirementType": "OPTIONAL",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [3.1415926535897931],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "actions": [
                                {
                                    "actionType": "LOWER_FORK_AND_BEEP",
                                    "actionDescriptor": "Section where the (third-party) fleet control system must tell the mobile robot to lower forks and beep",
                                    "requirementType": "REQUIRED",
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
```

## 11.19 Forward Edge with Two Mobile Robot Types with Differing Orientation

One edge (straight line) between two nodes, where two different mobile robot types from the same mobile robot integrator must adopt different orientations.

![](assets/fig11_19-1.png)

LIF-File:
```json
{
    "metaInformation": {
        "projectIdentification": "LIF Example 19",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.00Z",
        "lifVersion": "0.11.0"
    },
    "layouts": [
        {
            "layoutId": "Layout_Ground_Level",
            "layoutName": "Name of Layout Ground Level",
            "layoutVersion": "1",
            "layoutdescriptor": "Ground level of Customer",
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1"
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2"
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
                            "mobileRobotTypeId": "Mobile_Robot_Type_1",
                            "mobileRobotOrientations": [0.0],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "NONE",
                            "rotationAtEndNodeAllowed": "NONE"
                        },
                        {
                            "mobileRobotTypeId": "Mobile_Robot_Type_2",
                            "mobileRobotOrientations": [1.5707963267948966],
                            "orientationType": "TANGENTIAL",
                            "reachOrientationBeforeEntering": true,
                            "rotationAtStartNodeAllowed": "NONE",
                            "rotationAtEndNodeAllowed": "NONE"
                        }
                    ]
                }
            ]
        }
    ]
}```
