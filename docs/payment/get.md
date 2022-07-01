---
id: get
title: Listar pedido
sidebar_label: Listar pedido
---

Guia de [Introdução](introduction.md).

Listar um pedido baseado no _id

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /payment/:id

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
        "payment": {
            "_id": "62bdd69336fbb6ea855fdf3b",
            "buyer": {
                "_id": "62b9ed7df63d9bdac1b91a00",
                "name": "Fred Chien Produtor",
                "document": "344.367.320-10",
                "email": "fredchien@jobspace.com.br",
                "phone": "(41) 9999-9999",
                "uf": "PR",
                "city": "Curitiba",
                "role": "producer",
                "status": "active",
                "createdAt": "2022-06-27T17:48:45.956Z",
                "updatedAt": "2022-06-28T16:50:25.637Z",
                "__v": 0,
                "avatar": "https://domatech-tests.s3.amazonaws.com/d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg",
                "avatarKey": "d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg",
                "address": [
                    "62bb0621305ed651bf2bf95a"
                ]
            },
            "establishment": {
                "_id": "62ba0ae8754ba7c06965be47",
                "producer": "62ba0ae7754ba7c06965be45",
                "name": "Loja teste produtor",
                "status": "active",
                "createdAt": "2022-06-27T19:54:16.152Z",
                "updatedAt": "2022-06-27T21:00:41.566Z",
                "__v": 0,
                "location": {
                    "type": "Point",
                    "coordinates": [
                        -46.6323597,
                        -23.5653314
                    ],
                    "_id": "62ba11c42db63bd80cbb8528"
                },
                "avatar": "https://domatech-tests.s3.amazonaws.com/2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg",
                "avatarKey": "2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg"
            },
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
            "address": {
                "_id": "62bdd69336fbb6ea855fdf38",
                "cep": "80710000",
                "address": "Rua Padre Agostinho",
                "district": "Bigorrilho",
                "number": "1221",
                "complement": "Sem complemento",
                "uf": "PR",
                "city": "Curitiba",
                "status": "active",
                "createdAt": "2022-06-30T17:00:03.016Z",
                "updatedAt": "2022-06-30T17:00:03.016Z",
                "__v": 0
            },
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1934533:m:713bf27ac7b01803e38df47c615978e17f2e6c0c38f610fc092602063218213a",
            "createdAt": "2022-06-30T17:00:03.608Z",
            "updatedAt": "2022-06-30T17:09:57.419Z",
            "__v": 0
        },
        "message": "Pagamento encontrado com sucesso!"
    }