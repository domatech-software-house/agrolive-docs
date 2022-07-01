---
id: create
title: Criar produto
sidebar_label: Criar produto
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo produto via API


### Fields

| field | type | required | description |
|---|---|---|---|
| establishment | objectId | true | [Establishment](../establishment/create) |
| category | objectId | true | [Category](../category/create) |
| type | objectId | true | [Type](../type/create) |
| address | objectId | true | [Address](../address/create) |
| name | string | true | - |
| criteria | string | false | - |
| description | string | false | - |
| date | string | false | - |
| stock | number | true | - |
| price | number | true | - |
| distance | string | false | `fixed` `km` |
| shippingprice | number | false | - |

## Request

### Route

    POST /product

### Header

    Content-Type: application/json

### Body

    {
        "establishment": "62ba0ae8754ba7c06965be47",
        "category": "62baf4cde86239188c23f35d",
        "type": "62bafdacb259708bc69dd013",
        "address": "62bb0621305ed651bf2bf95a",
        "name": "Produto amarelo",
        "criteria": "10% amarelo",
        "description": "Uma breve descrição do produto",
        "date": "2022-06-28T13:10:04.426Z",
        "stock": 200,
        "price": 420
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "product": {
            "establishment": "62ba0ae8754ba7c06965be47",
            "category": "62baf4cde86239188c23f35d",
            "type": "62bafdacb259708bc69dd013",
            "address": "62bb0621305ed651bf2bf95a",
            "name": "Produto amarelo",
            "criteria": [
                "10% amarelo"
            ],
            "description": "Uma breve descrição do produto",
            "productPhoto": [],
            "date": "2022-06-28T13:10:04.426Z",
            "shipping": [
                {}
            ],
            "stock": 200,
            "price": 420,
            "status": "active",
            "_id": "62bb4cd4a9ce48dabf713ae2",
            "createdAt": "2022-06-28T18:47:48.948Z",
            "updatedAt": "2022-06-28T18:47:48.948Z",
            "__v": 0
        },
        "message": "Produto cadastrado com sucesso"
    }