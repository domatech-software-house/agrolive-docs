---
id: update
title: Ler notificação
sidebar_label: Ler notificação
---

Guia de [Introdução](introduction.md).

Ler uma notificação baseado no _id

Incluir token gerado no [login](authentication)


## Request

### Route

    PUT /notification/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
        "notification": {
            "_id": "62bdf1daef920b948c8a5e44",
            "title": "Novo comentário",
            "description": "Você recebeu um novo comentário de Fred Comprador",
            "user": "62b9ed7df63d9bdac1b91a00",
            "reading": true,
            "createdAt": "2022-06-30T18:56:26.770Z",
            "updatedAt": "2022-06-30T18:59:30.800Z",
            "__v": 0
        },
        "message": "Notificação alterada para lida!"
    }
