---
id: get
title: Listar um endereço
sidebar_label: Listar um endereço
---

Guia de [Introdução](introduction.md).

Lista um endereço cadastrado no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /address/:id

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
            "updatedAt": "2022-06-28T13:46:09.108Z",
            "__v": 0
        },
        "message": "Endereço encontrado com sucesso!"
    }