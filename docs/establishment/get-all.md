---
id: get-all
title: Listar todos estabelecimentos
sidebar_label: Listar todos estabelecimentos
---

Guia de [Introdução](introduction.md).

Lista todos os estabelecimentos cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /establishments

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
            "_id": "62ba0ae8754ba7c06965be47",
            "producer": {
                "address": [],
                "_id": "62ba0ae7754ba7c06965be45",
                "name": "Produtor",
                "document": "269.498.980-29",
                "email": "produtor@jobspace.com.br",
                "phone": "(41) 9999-9999",
                "uf": "SP",
                "city": "São Paulo",
                "role": "producer",
                "status": "active",
                "createdAt": "2022-06-27T19:54:15.582Z",
                "updatedAt": "2022-06-30T22:29:24.620Z",
                "__v": 0
            },
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
        }
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `status`, `name` |

### Request

#### Route

    GET /establishments?paginate=true&limit=50&status=active

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
                "_id": "62ba0ae8754ba7c06965be47",
                "producer": {
                    "address": [],
                    "_id": "62ba0ae7754ba7c06965be45",
                    "name": "Produtor",
                    "document": "269.498.980-29",
                    "email": "produtor@jobspace.com.br",
                    "phone": "(41) 9999-9999",
                    "uf": "SP",
                    "city": "São Paulo",
                    "role": "producer",
                    "status": "active",
                    "createdAt": "2022-06-27T19:54:15.582Z",
                    "updatedAt": "2022-06-30T22:29:24.620Z",
                    "__v": 0
                },
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
            }
        ],
        "total": 1,
        "limit": 10,
        "page": 1,
        "pages": 1
    }