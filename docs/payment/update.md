---
id: update
title: Editar status pedido
sidebar_label: Editar status pedido
---

Guia de [Introdução](introduction.md).

Editar um status do pedido baseado no _id

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| status | string | false | `pending` `canceled` `concluded` |

## Request

### Route

    PUT /payment/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "status": "pending"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
        "payment": {
            "_id": "62bdd69336fbb6ea855fdf3b",
            "buyer": "62b9ed7df63d9bdac1b91a00",
            "establishment": "62ba0ae8754ba7c06965be47",
            "product": "62bb4bee13961a124352936e",
            "totalPrice": 120,
            "requestNumber": "137655570",
            "status": "pending",
            "quantity": 12,
            "address": "62bdd69336fbb6ea855fdf38",
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1934533:m:713bf27ac7b01803e38df47c615978e17f2e6c0c38f610fc092602063218213a",
            "createdAt": "2022-06-30T17:00:03.608Z",
            "updatedAt": "2022-06-30T17:09:57.419Z",
            "__v": 0
        },
        "message": "Pagamento atualizado com sucesso!"
    }
