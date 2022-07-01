---
id: create
title: Criar uma mensagem
sidebar_label: Criar uma mensagem
---

Guia de [Introdução](introduction.md).

Informações para cadastro de nova mensagem no chat via API


### Fields

| field | type | required | description |
|---|---|---|---|
| chat | objectId | true | [Establishment](../chat/create) |
| text | string | true | - |

## Request

### Route

    POST /comment

### Header

    Content-Type: application/json

### Body

    {
        "chat": "62be17255e76ce0b2d2217ad",
        "text": "Bom dia!"
    }

## Response

### Status

    200

### Body

    {
        "_id": "62be17255e76ce0b2d2217ad",
        "payment": {
            "_id": "62be17255e76ce0b2d2217a7",
            "buyer": "62ba0b14754ba7c06965be4a",
            "establishment": "62ba0ae8754ba7c06965be47",
            "product": "62bb4bee13961a124352936e",
            "totalPrice": 120,
            "requestNumber": "137656160",
            "status": "pending",
            "quantity": 12,
            "address": "62be17245e76ce0b2d2217a5",
            "billet": "https://pay-sandbox.juno.com.br/charge/boleto.pdf?token=1935083:m:dc8d4a5789ccb7120dd402f5c604212449e5c81fd1b973c58a1a2b95a08db922",
            "createdAt": "2022-06-30T21:35:33.118Z",
            "updatedAt": "2022-06-30T21:35:33.118Z",
            "__v": 0
        },
        "comments": [
            "62be2b4a96829aa881f22fb9",
            "62be2b9b96829aa881f22fc0"
        ],
        "createdAt": "2022-06-30T21:35:33.830Z",
        "updatedAt": "2022-06-30T23:02:51.494Z",
        "__v": 2
    }