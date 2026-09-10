# 26 Forward Edge with Two Mobile Robot Types Sharing One Combined Property

One edge (straight line) between two nodes, where two mobile robot types share identical properties.

LIF-File:
```json
{
    "metaInformation": {
        "lifId": "LIF_Example_26",
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
                                        },
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "theta": 0.0,
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
                                        },
                                        {
                                            "manufacturer": "Manufacturer_A",
                                            "seriesName": "Series_2"
                                        }
                                    ],
                                    "theta": 0.0,
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
                                        },
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
                                    "maximumSpeed": 1.5,
                                    "maximumRotationSpeed": 1.0,
                                    "minimumLoadHandlingDeviceHeight": 0.0,
                                    "maximumMobileRobotHeight": 2.0,
                                    "loadRestriction": {
                                        "unloaded": true,
                                        "loaded": true,
                                        "loadSetNames": [
                                            "EUR_Pallet"
                                        ]
                                    },
                                    "reentryAllowed": true
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