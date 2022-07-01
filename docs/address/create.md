---
id: create
title: Criar endereço
sidebar_label: Criar endereço
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo endereço via API

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| cep | string | true | - |
| latitude | string | true | - |
| longitude | string | true | - |
| address | string | true | - |
| district | string | true | - |
| number | string | true | - |
| complement | string | true | - |
| uf | string | true | `length: 2` |
| city | string | true | - |



## Request

### Route

    POST /address

### Header

    Content-Type: application/json

### Body

    {
        "cep": "80710-000",
        "latitude": "-25.4320295",
        "longitude": "-49.300245",
        "address": "Rua Padre Agostinho",
        "district": "Bigorrilho",
        "number": "1221",
        "complement": "Sem complemento",
        "uf": "PR",
        "city": "Curitiba"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "address": {
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
            "_id": "62bb0621305ed651bf2bf95a",
            "createdAt": "2022-06-28T13:46:09.108Z",
            "updatedAt": "2022-06-28T13:46:09.108Z",
            "__v": 0
        },
        "message": "Endereço cadastrado com sucesso"
    }
