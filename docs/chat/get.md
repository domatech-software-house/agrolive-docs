---
id: get
title: Listar um chat
sidebar_label: Listar um chat
---

Guia de [Introdução](introduction.md).

Lista um chat de pedido cadastrado no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /chat/:id

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
        "_id": "62be17255e76ce0b2d2217ad",
        "payment": "62be17255e76ce0b2d2217a7",
        "comments": [
            {
                "_id": "62be2b4a96829aa881f22fb9",
                "user": {
                    "_id": "62ba0ae7754ba7c06965be45",
                    "name": "Produtor"
                },
                "chat": "62be17255e76ce0b2d2217ad",
                "text": "Testando Mensagem",
                "createdAt": "2022-06-30T23:01:30.519Z",
                "updatedAt": "2022-06-30T23:01:30.519Z",
                "__v": 0
            },
            {
                "_id": "62be2b9b96829aa881f22fc0",
                "user": {
                    "_id": "62ba0b14754ba7c06965be4a",
                    "name": "Fred Comprador"
                },
                "chat": "62be17255e76ce0b2d2217ad",
                "text": "Bom dia!",
                "createdAt": "2022-06-30T23:02:51.330Z",
                "updatedAt": "2022-06-30T23:02:51.330Z",
                "__v": 0
            }
        ],
        "createdAt": "2022-06-30T21:35:33.830Z",
        "updatedAt": "2022-06-30T23:02:51.494Z",
        "__v": 2
    }