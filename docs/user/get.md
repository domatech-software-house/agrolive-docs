---
id: get
title: Listar usuário
sidebar_label: Listar usuário
---

Guia de [Introdução](introduction.md).

Listar um usuário baseado no _id

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /user/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {}

## Response

### Status

    200

### Body

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