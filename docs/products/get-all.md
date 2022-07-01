---
id: get-all
title: Listar todos produtos
sidebar_label: Listar todos produtos
---

Guia de [Introdução](introduction.md).

Lista todos os produtos cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /product

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
            "_id": "62bb4bee13961a124352936e",
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
            "category": {
                "_id": "62baf4cde86239188c23f35d",
                "name": "Grãos",
                "status": "active",
                "createdAt": "2022-06-28T12:32:13.229Z",
                "updatedAt": "2022-06-28T12:43:20.060Z",
                "__v": 0
            },
            "type": {
                "_id": "62bafdacb259708bc69dd013",
                "name": "KG",
                "status": "active",
                "createdAt": "2022-06-28T13:10:04.426Z",
                "updatedAt": "2022-06-28T13:10:04.426Z",
                "__v": 0
            },
            "address": {
                "_id": "62bb0621305ed651bf2bf95a",
                "cep": "80710-000",
                "location": {
                    "type": "Point",
                    "coordinates": [
                        -49.300245,
                        -25.4320295
                    ],
                    "_id": "62bb0621305ed651bf2bf95b"
                },
                "address": "Rua Padre Agostinho",
                "district": "Bigorrilho",
                "number": "1221",
                "complement": "Sem complemento",
                "uf": "PR",
                "city": "Curitiba",
                "status": "active",
                "createdAt": "2022-06-28T13:46:09.108Z",
                "updatedAt": "2022-06-28T14:12:45.322Z",
                "__v": 0
            },
            "name": "Produt com foto",
            "criteria": [],
            "productPhoto": [
                {
                    "_id": "62bb4bef13961a1243529370",
                    "product": "62bb4bee13961a124352936e",
                    "url": "https://domatech-tests.s3.amazonaws.com/388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                    "key": "388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                    "createdAt": "2022-06-28T18:43:59.240Z",
                    "updatedAt": "2022-06-28T18:43:59.240Z",
                    "__v": 0
                },
                {
                    "_id": "62bb4f71223b9281ce71cc90",
                    "product": "62bb4bee13961a124352936e",
                    "url": "https://domatech-tests.s3.amazonaws.com/8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                    "key": "8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                    "createdAt": "2022-06-28T18:58:57.383Z",
                    "updatedAt": "2022-06-28T18:58:57.383Z",
                    "__v": 0
                }
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
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `status`, `establishment` |

### Request

#### Route

    GET /product?establishment=62ba0ae8754ba7c06965be47&paginate=true

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
                "_id": "62bb4bee13961a124352936e",
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
                "category": {
                    "_id": "62baf4cde86239188c23f35d",
                    "name": "Grãos",
                    "status": "active",
                    "createdAt": "2022-06-28T12:32:13.229Z",
                    "updatedAt": "2022-06-28T12:43:20.060Z",
                    "__v": 0
                },
                "type": {
                    "_id": "62bafdacb259708bc69dd013",
                    "name": "KG",
                    "status": "active",
                    "createdAt": "2022-06-28T13:10:04.426Z",
                    "updatedAt": "2022-06-28T13:10:04.426Z",
                    "__v": 0
                },
                "address": {
                    "_id": "62bb0621305ed651bf2bf95a",
                    "cep": "80710-000",
                    "location": {
                        "type": "Point",
                        "coordinates": [
                            -49.300245,
                            -25.4320295
                        ],
                        "_id": "62bb0621305ed651bf2bf95b"
                    },
                    "address": "Rua Padre Agostinho",
                    "district": "Bigorrilho",
                    "number": "1221",
                    "complement": "Sem complemento",
                    "uf": "PR",
                    "city": "Curitiba",
                    "status": "active",
                    "createdAt": "2022-06-28T13:46:09.108Z",
                    "updatedAt": "2022-06-28T14:12:45.322Z",
                    "__v": 0
                },
                "name": "Produt com foto",
                "criteria": [],
                "productPhoto": [
                    {
                        "_id": "62bb4bef13961a1243529370",
                        "product": "62bb4bee13961a124352936e",
                        "url": "https://domatech-tests.s3.amazonaws.com/388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                        "key": "388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                        "createdAt": "2022-06-28T18:43:59.240Z",
                        "updatedAt": "2022-06-28T18:43:59.240Z",
                        "__v": 0
                    },
                    {
                        "_id": "62bb4f71223b9281ce71cc90",
                        "product": "62bb4bee13961a124352936e",
                        "url": "https://domatech-tests.s3.amazonaws.com/8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                        "key": "8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                        "createdAt": "2022-06-28T18:58:57.383Z",
                        "updatedAt": "2022-06-28T18:58:57.383Z",
                        "__v": 0
                    }
                ],
                "shipping": [
                    {}
                ],
                "stock": 72,
                "price": 55,
                "status": "active",
                "createdAt": "2022-06-28T18:43:58.926Z",
                "updatedAt": "2022-06-30T23:31:49.973Z",
                "__v": 1
            },
            {
                "_id": "62bb3871342bf1829a2a9897",
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
                "category": {
                    "_id": "62baf4cde86239188c23f35d",
                    "name": "Grãos",
                    "status": "active",
                    "createdAt": "2022-06-28T12:32:13.229Z",
                    "updatedAt": "2022-06-28T12:43:20.060Z",
                    "__v": 0
                },
                "type": {
                    "_id": "62bafdacb259708bc69dd013",
                    "name": "KG",
                    "status": "active",
                    "createdAt": "2022-06-28T13:10:04.426Z",
                    "updatedAt": "2022-06-28T13:10:04.426Z",
                    "__v": 0
                },
                "address": {
                    "_id": "62bb0621305ed651bf2bf95a",
                    "cep": "80710-000",
                    "location": {
                        "type": "Point",
                        "coordinates": [
                            -49.300245,
                            -25.4320295
                        ],
                        "_id": "62bb0621305ed651bf2bf95b"
                    },
                    "address": "Rua Padre Agostinho",
                    "district": "Bigorrilho",
                    "number": "1221",
                    "complement": "Sem complemento",
                    "uf": "PR",
                    "city": "Curitiba",
                    "status": "active",
                    "createdAt": "2022-06-28T13:46:09.108Z",
                    "updatedAt": "2022-06-28T14:12:45.322Z",
                    "__v": 0
                },
                "name": "Produto teste",
                "criteria": [
                    "10% verde"
                ],
                "description": "Uma breve descrição do produto",
                "productPhoto": [],
                "date": "2022-06-28T13:10:04.426Z",
                "shipping": [
                    {
                        "distance": "km",
                        "price": 20
                    }
                ],
                "stock": 100,
                "price": 120,
                "status": "active",
                "createdAt": "2022-06-28T17:20:49.424Z",
                "updatedAt": "2022-06-28T17:20:49.424Z",
                "__v": 0
            }
        ],
        "total": 2,
        "limit": 10,
        "page": 1,
        "pages": 1
    }