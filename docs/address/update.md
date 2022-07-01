---
id: update
title: Editar endereço
sidebar_label: Editar endereço
---

Guia de [Introdução](introduction.md).

Editar um endereço baseado no _id

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |
| description | string | false | - |
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

    PUT /address/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "address": "Loja teste produtor",
        "latitude": "-23.5653314",
        "longitude": "-46.6323597",
        "description": "Descrição da loja",
        "cep": "81110070",
        "address": "Rua teste",
        "district": "Bairro",
        "number": "1221",
        "complement": "Complemento",
        "uf": "UF",
        "city": "Cidade"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
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
        "message": "Endereço atualizado com sucesso!"
    }
