---
id: get-all
title: Listar todos usuários
sidebar_label: Listar todos usuários
---

Guia de [Introdução](introduction.md).

Lista todos os usuários cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /user

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
            "address": [],
            "_id": "62ba0b14754ba7c06965be4a",
            "name": "Fred Comprador",
            "document": "269.498.980-29",
            "email": "comprador@jobspace.com.br",
            "phone": "(41) 9999-9999",
            "uf": "SP",
            "city": "São Paulo",
            "role": "buyer",
            "status": "active",
            "createdAt": "2022-06-27T19:55:00.801Z",
            "updatedAt": "2022-06-27T19:55:00.801Z",
            "__v": 0
        },
        {
            "_id": "62b9ed7df63d9bdac1b91a00",
            "name": "Fred Chien Produtor",
            "document": "344.367.320-10",
            "email": "fredchien@jobspace.com.br",
            "phone": "(41) 9999-9999",
            "uf": "PR",
            "city": "Curitiba",
            "role": "producer",
            "status": "active",
            "createdAt": "2022-06-27T17:48:45.956Z",
            "updatedAt": "2022-06-28T16:50:25.637Z",
            "__v": 0,
            "avatar": "https://domatech-tests.s3.amazonaws.com/d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg",
            "avatarKey": "d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg",
            "address": [
                {
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
                }
            ]
        }
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `role`, `status`, `uf`, `city`, `name` |

### Request

#### Route

    GET /user?paginate=true&limit=50&uf=SP

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
                "address": [],
                "_id": "62ba0b14754ba7c06965be4a",
                "name": "Fred Comprador",
                "document": "269.498.980-29",
                "email": "comprador@jobspace.com.br",
                "phone": "(41) 9999-9999",
                "uf": "SP",
                "city": "São Paulo",
                "role": "buyer",
                "status": "active",
                "createdAt": "2022-06-27T19:55:00.801Z",
                "updatedAt": "2022-06-27T19:55:00.801Z",
                "__v": 0
            },
            {
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
            {
                "address": [],
                "_id": "62b9ef75cc331388d9817b4d",
                "name": "Pedro Produtor",
                "document": "269.498.980-29",
                "email": "fred_chien@yahoo.com.br",
                "phone": "(41) 9999-9999",
                "uf": "SP",
                "city": "São Paulo",
                "role": "buyer",
                "status": "disabled",
                "createdAt": "2022-06-27T17:57:09.333Z",
                "updatedAt": "2022-06-27T19:05:47.419Z",
                "__v": 0
            }
        ],
        "total": 3,
        "limit": 10,
        "page": 1,
        "pages": 1
    }