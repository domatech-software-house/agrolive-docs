---
id: get
title: Listar um estabelecimentos
sidebar_label: Listar um estabelecimentos
---

Guia de [Introdução](introduction.md).

Lista um estabelecimento cadastrado no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /establishments/:id

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
        "establishment": {
            "_id": "62ba0ae8754ba7c06965be47",
            "producer": {
                "_id": "62ba0ae7754ba7c06965be45",
                "name": "Fred Produtor",
                "document": "269.498.980-29",
                "email": "produtor@jobspace.com.br",
                "phone": "(41) 9999-9999",
                "uf": "SP",
                "city": "São Paulo",
                "role": "producer",
                "status": "active",
                "createdAt": "2022-06-27T19:54:15.582Z",
                "updatedAt": "2022-06-27T19:54:15.582Z",
                "__v": 0
            },
            "name": "Nome da Loja",
            "status": "active",
            "createdAt": "2022-06-27T19:54:16.152Z",
            "updatedAt": "2022-06-27T19:54:16.152Z",
            "__v": 0
        },
        "message": "Estabelecimento encontrado com sucesso!"
    }