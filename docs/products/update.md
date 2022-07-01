---
id: update
title: Editar produto
sidebar_label: Editar produto
---

Guia de [Introdução](introduction.md).

Editar um produto baseado no _id

Incluir token gerado no [login](authentication)

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

    PUT /product/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "name": "Batata Doce",
        "criteria": "Roxa",
        "distance": "fixed",
        "shippingprice": 200
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
        "product": {
            "_id": "62bb3904342bf1829a2a989d",
            "establishment": "62ba0ae8754ba7c06965be47",
            "category": "62baf4cde86239188c23f35d",
            "type": "62bafdacb259708bc69dd013",
            "address": "62bb0621305ed651bf2bf95a",
            "name": "Batata Doce",
            "criteria": [
                "Roxa"
            ],
            "description": "Uma breve descrição do produto",
            "productPhoto": [],
            "date": "2022-06-28T13:10:04.426Z",
            "shipping": [
                {
                    "distance": "fixed",
                    "price": 200
                }
            ],
            "stock": 200,
            "price": 200,
            "status": "active",
            "createdAt": "2022-06-28T17:23:16.518Z",
            "updatedAt": "2022-06-28T17:46:31.807Z",
            "__v": 0
        },
        "message": "Produto atualizado com sucesso!"
    }
