---
id: update
title: Editar tipo de produto
sidebar_label: Editar tipo de produto
---

Guia de [Introdução](introduction.md).

Editar um tipo de produto baseado no _id

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |

## Request

### Route

    PUT /types/:id

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
        "types": {
            "name": "SC",
            "status": "active",
            "_id": "62bafdb7b259708bc69dd017",
            "createdAt": "2022-06-28T13:10:15.133Z",
            "updatedAt": "2022-06-28T13:10:15.133Z",
            "__v": 0
        },
        "message": "Tipo de produto alterado com sucesso"
    }
