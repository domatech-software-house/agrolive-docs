---
id: update
title: Editar usuário
sidebar_label: Editar usuário
---

Guia de [Introdução](introduction.md).

Editar um usuário baseado no _id

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |
| document | string | true | - |
| email | string | true | - |
| phone | string | false | - |
| password | string | true | - |
| uf | string | true | `length: 2` |
| city | string | true | - |

## Request

### Route

    PUT /user/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "name": "Fred Comprador",
        "document": "26949898029",
        "email": "comprador@jobspace.com.br",
        "phone": "(41) 9999-9999",
        "password": "senha",
        "uf": "SP",
        "city": "São Paulo"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
        "user": {
            "address": [],
            "_id": "62ba0ae7754ba7c06965be45",
            "name": "Produtor",
            "document": "269.498.980-29",
            "email": "produtor@jobspace.com.br",
            "phone": "(41) 9999-9999",
            "uf": "SP",
            "city": "São Paulo",
            "role": "producer",
            "status": "active",
            "createdAt": "2022-06-27T19:54:15.582Z",
            "updatedAt": "2022-06-30T22:29:24.620Z",
            "__v": 0
        },
        "message": "Dados alterados com sucesso"
    }
