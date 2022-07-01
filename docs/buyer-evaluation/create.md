---
id: create
title: Criar comentário comprador
sidebar_label: Criar comentário comprador
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo comentário de produtor para comprador via API


### Fields

| field | type | required | description |
|---|---|---|---|
| payment | objectId | true | [Payment](../payment/create) |
| buyer | objectId | true | [User](../user/create) |
| star | number | true | - |
| description | string | true | - |

## Request

### Route

    POST /buyer-evaluation

### Header

    Content-Type: application/json

### Body

    {
        "payment": "62bdd69336fbb6ea855fdf3b",
        "buyer": "62b9ed7df63d9bdac1b91a00",
        "star": 5,
        "description": "Muito bom, um ótimo comprador."
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "request": {
            "buyer": "62b9ed7df63d9bdac1b91a00",
            "payment": "62bdd69336fbb6ea855fdf3b",
            "establishment": "62ba0b14754ba7c06965be4a",
            "star": 5,
            "description": "Muito bom, um ótimo comprador.",
            "status": "active",
            "_id": "62bdf1daef920b948c8a5e42",
            "createdAt": "2022-06-30T18:56:26.426Z",
            "updatedAt": "2022-06-30T18:56:26.426Z",
            "__v": 0
        },
        "message": "Comentário cadastrado com sucesso"
    }