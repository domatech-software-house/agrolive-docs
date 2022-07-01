---
id: get
title: Listar notificações
sidebar_label: Listar notificações
---

Guia de [Introdução](introduction.md).

Lista todas as notificações de um determinado usuário logado

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /notification

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
            "_id": "62be17255e76ce0b2d2217af",
            "title": "Novo pedido",
            "description": "Você recebeu um novo pedido de Fred teste",
            "user": "62ba0ae7754ba7c06965be45",
            "reading": false,
            "createdAt": "2022-06-30T21:35:34.001Z",
            "updatedAt": "2022-06-30T21:35:34.001Z",
            "__v": 0
        },
        {
            "_id": "62bdf44d7e311532c81fbc8c",
            "title": "Novo pedido",
            "description": "Você recebeu um novo pedido de Fred teste",
            "user": "62ba0ae7754ba7c06965be45",
            "reading": false,
            "createdAt": "2022-06-30T19:06:53.207Z",
            "updatedAt": "2022-06-30T19:06:53.207Z",
            "__v": 0
        },
        {
            "_id": "62bdf16c070ba9bd02eee100",
            "title": "Novo comentário",
            "description": "Você recebeu um novo comentário de Fred Comprador",
            "user": "62ba0ae7754ba7c06965be45",
            "reading": false,
            "createdAt": "2022-06-30T18:54:36.867Z",
            "updatedAt": "2022-06-30T18:54:36.867Z",
            "__v": 0
        },
        {
            "_id": "62bdf1440045496bc1e9ee86",
            "title": "Novo comentário",
            "user": "62ba0ae7754ba7c06965be45",
            "reading": false,
            "createdAt": "2022-06-30T18:53:56.962Z",
            "updatedAt": "2022-06-30T18:53:56.962Z",
            "__v": 0
        }
    ]