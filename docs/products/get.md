---
id: get
title: Listar produto
sidebar_label: Listar produto
---

Guia de [Introdução](introduction.md).

Listar um produto baseado no _id

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /product/:id

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
        "product": {
            "_id": "62bb4bee13961a124352936e",
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
            "category": {
                "_id": "62baf4cde86239188c23f35d",
                "name": "Grãos",
                "status": "active",
                "createdAt": "2022-06-28T12:32:13.229Z",
                "updatedAt": "2022-06-28T12:43:20.060Z",
                "__v": 0
            },
            "type": {
                "_id": "62bafdacb259708bc69dd013",
                "name": "KG",
                "status": "active",
                "createdAt": "2022-06-28T13:10:04.426Z",
                "updatedAt": "2022-06-28T13:10:04.426Z",
                "__v": 0
            },
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
            "name": "Produt com foto",
            "criteria": [],
            "productPhoto": [
                {
                    "_id": "62bb4bef13961a1243529370",
                    "product": "62bb4bee13961a124352936e",
                    "url": "https://domatech-tests.s3.amazonaws.com/388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                    "key": "388fc7e201d969732135ff1a3cabb6be-1649170157827.jpeg",
                    "createdAt": "2022-06-28T18:43:59.240Z",
                    "updatedAt": "2022-06-28T18:43:59.240Z",
                    "__v": 0
                },
                {
                    "_id": "62bb4f71223b9281ce71cc90",
                    "product": "62bb4bee13961a124352936e",
                    "url": "https://domatech-tests.s3.amazonaws.com/8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                    "key": "8de388b0f4fa95fbf20886bcaaee5054-stp_card_visa.png",
                    "createdAt": "2022-06-28T18:58:57.383Z",
                    "updatedAt": "2022-06-28T18:58:57.383Z",
                    "__v": 0
                }
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
        "message": "Produto encontrado com sucesso!"
    }