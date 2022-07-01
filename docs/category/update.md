---
id: update
title: Editar categoria de produto
sidebar_label: Editar categoria de produto
---

Guia de [Introdução](introduction.md).

Editar uma categoria de produto baseado no _id

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |

## Request

### Route

    PUT /category/:id

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "name": "Novo nome",
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "error": false,
        "category": {
            "_id": "62baf4cde86239188c23f35d",
            "name": "Grãos",
            "status": "active",
            "createdAt": "2022-06-28T12:32:13.229Z",
            "updatedAt": "2022-06-28T12:43:20.060Z",
            "__v": 0
        },
        "message": "Dados alterados com sucesso"
    }
