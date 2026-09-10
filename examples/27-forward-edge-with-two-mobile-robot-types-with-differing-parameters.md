# 27 Forward Edge with Two Mobile Robot Types with Differing Parameters

One edge (straight line) between two nodes, where each mobile robot type has different parameters on the node and on the edge.
LIF-File:

```json
{
    "metaInformation": {
        "lifId": "LIF_Example_27",
        "creator": "VDMA",
        "exportTimestamp": "2023-09-28T10:00:00.000Z",
        "lifVersion": "2.0.0"
    },
    "origins": [
        {
            "originId": "Origin_1",
            "originDescriptor": "Ground level of Customer",
            "layouts": [
                {
                    "layoutId": "Layout_Ground_Level",
                    "layoutName": "Name of Layout Ground Level",
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
                                    ],
                                    "theta": 0.0,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": false
                                    }
                                },
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "theta": 1.5707963267948966,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": true,
                                        "loadSetNames": [
                                            "EUR_Pallet"
                                        ]
                                    }
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
                                    "theta": 0.0,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": false
                                    }
                                },
                                {
                                    "mobileRobotTypes": [
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "theta": 1.5707963267948966,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": true,
                                        "loadSetNames": [
                                            "EUR_Pallet"
                                        ]
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
                                    "orientationType": "TANGENTIAL",
                                    "reachOrientationBeforeEntering": false,
                                    "mobileRobotOrientations": [
                                        0.0
                                    ],
                                    "rotationAtStartNodeAllowed": "BOTH",
                                    "rotationAtEndNodeAllowed": "BOTH",
                                    "maximumSpeed": 2.0,
                                    "maximumRotationSpeed": 1.5,
                                    "minimumLoadHandlingDeviceHeight": 0.0,
                                    "maximumMobileRobotHeight": 2.5,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": false
                                    },
                                    "reentryAllowed": true
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
                                        0.0
                                    ],
                                    "rotationAtStartNodeAllowed": "NONE",
                                    "rotationAtEndNodeAllowed": "NONE",
                                    "maximumSpeed": 1.0,
                                    "maximumRotationSpeed": 0.5,
                                    "minimumLoadHandlingDeviceHeight": 0.0,
                                    "maximumMobileRobotHeight": 1.8,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": true,
                                        "loadSetNames": [
                                            "EUR_Pallet"
                                        ]
                                    },
                                    "reentryAllowed": false
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