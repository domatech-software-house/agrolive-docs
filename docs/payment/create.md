---
id: create
title: Criar pedido
sidebar_label: Criar pedido
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo pedido via API

Dados para serem informados na criação do pedido via JUNO API


### Fields

| field | type | required | description |
|---|---|---|---|
| establishment | objectId | true | [Establishment](../establishment/create) |
| product | objectId | true | [Product](../product/create) |
| cep | string | true | - |
| address | string | true | - |
| district | string | true | - |
| number | string | true | - |
| complement | string | true | - |
| uf | string | true | - |
| city | string | true | - |
| totalPrice | number | true | - |
| quantity | number | true | - |
| name | string | true | - |
| document | string | true | - |

## Request

### Route

    POST /payment

### Header

    Content-Type: application/json

### Body

    {
        "cep": "80710000",
        "address": "Rua Padre Agostinho",
        "district": "Bigorrilho",
        "number": "1221",
        "complement": "Sem complemento",
        "uf": "PR",
        "city": "Curitiba",
        "totalPrice": 120,
        "establishment": "62ba0ae8754ba7c06965be47",
        "product": "62bb4bee13961a124352936e",
        "quantity": 12,
        "name": "Fred teste",
        "document": "07688043964"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "payment": {
            "buyer": "62ba0b14754ba7c06965be4a",
            "establishment": "62ba0ae8754ba7c06965be47",
            "product": "62bb4bee13961a124352936e",
            "totalPrice": 120,
            "requestNumber": "137656219",
            "status": "pending",
            "quantity": 12,
            "address": "62be3264aaae052a132e02c3",
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1935133:m:8c7b0a02419f67447e1037f87617aed0e5b43f33a1e887340faf2fe782872481",
            "_id": "62be3265aaae052a132e02c5",
            "createdAt": "2022-06-30T23:31:49.428Z",
            "updatedAt": "2022-06-30T23:31:49.428Z",
            "__v": 0
        },
        "message": "Pagamento cadastrado com sucesso"
    }