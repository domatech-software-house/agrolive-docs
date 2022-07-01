---
id: get-all
title: Listar todos comentário venda
sidebar_label: Listar todos comentário venda
---

Guia de [Introdução](introduction.md).

Lista todos os comentário de vendas cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /request-evaluation

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {}

## Response

### Status

    200

### Body

    [
        {
            "_id": "62bdef5ab6bc7a13cd4b82cd",
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": {
                "_id": "62bdd69336fbb6ea855fdf3b",
                "buyer": "62b9ed7df63d9bdac1b91a00",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 108,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-06-30T17:00:04.039Z",
                    "__v": 1
                },
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
            "establishment": "62ba0ae8754ba7c06965be47",
            "star": 4,
            "description": "Muito bom, gostei",
            "status": "active",
            "createdAt": "2022-06-30T18:45:46.128Z",
            "updatedAt": "2022-06-30T18:45:46.128Z",
            "__v": 0
        },
        {
            "_id": "62bde969d11c42ff01559456",
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": {
                "_id": "62bdd69336fbb6ea855fdf3b",
                "buyer": "62b9ed7df63d9bdac1b91a00",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 108,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-06-30T17:00:04.039Z",
                    "__v": 1
                },
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
            "establishment": "62b9ed7df63d9bdac1b91a00",
            "star": 5,
            "description": "Muito bom, um ótimo comprador.",
            "status": "active",
            "createdAt": "2022-06-30T18:20:25.041Z",
            "updatedAt": "2022-06-30T18:20:25.041Z",
            "__v": 0
        },
        {
            "_id": "62bde471ad1bc86a3be0dc1f",
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": {
                "_id": "62bdd69336fbb6ea855fdf3b",
                "buyer": "62b9ed7df63d9bdac1b91a00",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 108,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-06-30T17:00:04.039Z",
                    "__v": 1
                },
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
            "establishment": "62ba0ae8754ba7c06965be47",
            "star": 4,
            "description": "Muito bom, gostei",
            "status": "active",
            "createdAt": "2022-06-30T17:59:13.116Z",
            "updatedAt": "2022-06-30T17:59:13.116Z",
            "__v": 0
        }
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `buyer`, `payment` |

### Request

#### Route

    GET /request-evaluation?buyer=62ba0b14754ba7c06965be4a

#### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

#### Body

    {}

### Response

#### Status

    200

#### Body

    [
        {
            "_id": "62bdf16a070ba9bd02eee0fa",
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": {
                "_id": "62bdd69336fbb6ea855fdf3b",
                "buyer": "62b9ed7df63d9bdac1b91a00",
                "establishment": "62ba0ae8754ba7c06965be47",
                "product": {
                    "_id": "62bb4bee13961a124352936e",
                    "establishment": "62ba0ae8754ba7c06965be47",
                    "category": "62baf4cde86239188c23f35d",
                    "type": "62bafdacb259708bc69dd013",
                    "address": "62bb0621305ed651bf2bf95a",
                    "name": "Produt com foto",
                    "criteria": [],
                    "productPhoto": [
                        "62bb4bef13961a1243529370",
                        "62bb4f71223b9281ce71cc90",
                        "62bf2f8f3d5a95f0f13e0125",
                        "62bf2f8f3d5a95f0f13e0129"
                    ],
                    "shipping": [
                        {}
                    ],
                    "stock": 72,
                    "price": 55,
                    "status": "active",
                    "createdAt": "2022-06-28T18:43:58.926Z",
                    "updatedAt": "2022-07-01T17:32:00.230Z",
                    "__v": 1
                },
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
            "establishment": "62ba0ae7754ba7c06965be45",
            "star": 4,
            "description": "Muito bom, gostei",
            "status": "active",
            "createdAt": "2022-06-30T18:54:34.322Z",
            "updatedAt": "2022-06-30T18:54:34.322Z",
            "__v": 0
        },
    ]