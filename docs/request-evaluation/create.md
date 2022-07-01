---
id: create
title: Criar comentário venda
sidebar_label: Criar comentário venda
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo comentário de comprador para pedido via API


### Fields

| field | type | required | description |
|---|---|---|---|
| payment | objectId | true | [Payment](../payment/create) |
| establishment | objectId | true | [Establishment](../establishment/create) |
| star | number | true | - |
| description | string | true | - |

## Request

### Route

    POST /request-evaluation

### Header

    Content-Type: application/json

### Body

    {
        "payment": "62bdd69336fbb6ea855fdf3b",
        "establishment": "62ba0ae7754ba7c06965be45",
        "star": 4,
        "description": "Muito bom, gostei"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "request": {
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": "62bdd69336fbb6ea855fdf3b",
            "establishment": "62ba0ae7754ba7c06965be45",
            "star": 4,
            "description": "Muito bom, gostei",
            "status": "active",
            "_id": "62bdf16a070ba9bd02eee0fa",
            "createdAt": "2022-06-30T18:54:34.322Z",
            "updatedAt": "2022-06-30T18:54:34.322Z",
            "__v": 0
        },
        "message": "Comentário cadastrado com sucesso"
    }