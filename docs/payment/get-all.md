---
id: get-all
title: Listar todos pedidos
sidebar_label: Listar todos pedidos
---

Guia de [Introdução](introduction.md).

Lista todos os pedidos cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /payment

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {}

## Response

### Status

    200

### Body

    [
        {
            "_id": "62bdf44c7e311532c81fbc86",
            "buyer": "62b9ed7df63d9bdac1b91a00",
            "establishment": {
                "_id": "62ba0ae8754ba7c06965be47",
                "producer": "62ba0ae7754ba7c06965be45",
                "name": "Loja teste produtor",
                "status": "active",
                "createdAt": "2022-06-27T19:54:16.152Z",
                "updatedAt": "2022-06-27T21:00:41.566Z",
                "__v": 0,
                "location": {
                    "type": "Point",
                    "coordinates": [
                        -46.6323597,
                        -23.5653314
                    ],
                    "_id": "62ba11c42db63bd80cbb8528"
                },
                "avatar": "https://domatech-tests.s3.amazonaws.com/2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg",
                "avatarKey": "2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg"
            },
            "product": {
                "_id": "62bb4bee13961a124352936e",
                "establishment": "62ba0ae8754ba7c06965be47",
                "category": "62baf4cde86239188c23f35d",
                "type": "62bafdacb259708bc69dd013",
                "address": "62bb0621305ed651bf2bf95a",
                "name": "Produt com foto",
                "criteria": [],
                "productPhoto": [
                    "62bb4bef13961a1243529370",
                    "62bb4f71223b9281ce71cc90"
                ],
                "shipping": [
                    {}
                ],
                "stock": 96,
                "price": 55,
                "status": "active",
                "createdAt": "2022-06-28T18:43:58.926Z",
                "updatedAt": "2022-06-30T19:06:52.956Z",
                "__v": 1
            },
            "totalPrice": 120,
            "requestNumber": "137656029",
            "status": "pending",
            "quantity": 12,
            "address": "62bdf44b7e311532c81fbc84",
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1934967:m:8df313a2f2715381d068686f1e5a6784550a71f164bf73e125e959db71aebb4d",
            "createdAt": "2022-06-30T19:06:52.436Z",
            "updatedAt": "2022-06-30T19:06:52.436Z",
            "__v": 0
        },
        {
            "_id": "62bdd69336fbb6ea855fdf3b",
            "buyer": "62b9ed7df63d9bdac1b91a00",
            "establishment": {
                "_id": "62ba0ae8754ba7c06965be47",
                "producer": "62ba0ae7754ba7c06965be45",
                "name": "Loja teste produtor",
                "status": "active",
                "createdAt": "2022-06-27T19:54:16.152Z",
                "updatedAt": "2022-06-27T21:00:41.566Z",
                "__v": 0,
                "location": {
                    "type": "Point",
                    "coordinates": [
                        -46.6323597,
                        -23.5653314
                    ],
                    "_id": "62ba11c42db63bd80cbb8528"
                },
                "avatar": "https://domatech-tests.s3.amazonaws.com/2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg",
                "avatarKey": "2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg"
            },
            "product": {
                "_id": "62bb4bee13961a124352936e",
                "establishment": "62ba0ae8754ba7c06965be47",
                "category": "62baf4cde86239188c23f35d",
                "type": "62bafdacb259708bc69dd013",
                "address": "62bb0621305ed651bf2bf95a",
                "name": "Produt com foto",
                "criteria": [],
                "productPhoto": [
                    "62bb4bef13961a1243529370",
                    "62bb4f71223b9281ce71cc90"
                ],
                "shipping": [
                    {}
                ],
                "stock": 96,
                "price": 55,
                "status": "active",
                "createdAt": "2022-06-28T18:43:58.926Z",
                "updatedAt": "2022-06-30T19:06:52.956Z",
                "__v": 1
            },
            "totalPrice": 120,
            "requestNumber": "137655570",
            "status": "pending",
            "quantity": 12,
            "address": "62bdd69336fbb6ea855fdf38",
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1934533:m:713bf27ac7b01803e38df47c615978e17f2e6c0c38f610fc092602063218213a",
            "createdAt": "2022-06-30T17:00:03.608Z",
            "updatedAt": "2022-06-30T17:09:57.419Z",
            "__v": 0
        },
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `buyer`, `establishment`, `status` |

### Request

#### Route

    GET /payment?establishment=62ba0ae8754ba7c06965be47&paginate=true

#### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

#### Body

    {}

### Response

#### Status

    200

#### Body

    {
        "docs": [
            {
                "_id": "62be3265aaae052a132e02c5",
                "buyer": "62ba0b14754ba7c06965be4a",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90",
                        "62bf2f8f3d5a95f0f13e0125",
                        "62bf2f8f3d5a95f0f13e0129"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 72,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-07-01T17:32:00.230Z",
                    "__v": 1
                },
                "totalPrice": 120,
                "requestNumber": "137656219",
                "status": "pending",
                "quantity": 12,
                "address": "62be3264aaae052a132e02c3",
                "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1935133:m:8c7b0a02419f67447e1037f87617aed0e5b43f33a1e887340faf2fe782872481",
                "createdAt": "2022-06-30T23:31:49.428Z",
                "updatedAt": "2022-06-30T23:31:49.428Z",
                "__v": 0
            },
            {
                "_id": "62be17255e76ce0b2d2217a7",
                "buyer": "62ba0b14754ba7c06965be4a",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90",
                        "62bf2f8f3d5a95f0f13e0125",
                        "62bf2f8f3d5a95f0f13e0129"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 72,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-07-01T17:32:00.230Z",
                    "__v": 1
                },
                "totalPrice": 120,
                "requestNumber": "137656160",
                "status": "pending",
                "quantity": 12,
                "address": "62be17245e76ce0b2d2217a5",
                "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1935083:m:dc8d4a5789ccb7120dd402f5c604212449e5c81fd1b973c58a1a2b95a08db922",
                "createdAt": "2022-06-30T21:35:33.118Z",
                "updatedAt": "2022-06-30T21:35:33.118Z",
                "__v": 0
            },
        ],
        "total": 7,
        "limit": 10,
        "page": 1,
        "pages": 1
    }