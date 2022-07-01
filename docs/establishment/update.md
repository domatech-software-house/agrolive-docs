---
id: update
title: Editar estabelecimento
sidebar_label: Editar estabelecimento
---

Guia de [Introdução](introduction.md).

Editar um estabelecimento baseado no _id

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

    PUT /establishments/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "name": "Loja teste produtor",
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
        "establishment": {
            "_id": "62ba0ae8754ba7c06965be47",
            "producer": "62ba0ae7754ba7c06965be45",
            "name": "Loja teste produtor",
            "status": "active",
            "createdAt": "2022-06-27T19:54:16.152Z",
            "updatedAt": "2022-06-27T20:23:32.937Z",
            "__v": 0,
            "location": {
                "type": "Point",
                "coordinates": [
                    -46.6323597,
                    -23.5653314
                ],
                "_id": "62ba11c42db63bd80cbb8528"
            }
        },
        "message": "Estabelecimento atualizado com sucesso!"
    }
