---
id: delete
title: Remover usuário
sidebar_label: Remover usuário
---

Guia de [Introdução](introduction.md).

Nenhum usuário é deletado do sistema, mas sim, alterado o seu status de "active" para "disabled"

Incluir token gerado no [login](authentication)

## Request

### Route

    DELETE /user/:id

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
        "user": {
            "_id": "62b9ef75cc331388d9817b4d",
            "name": "Pedro Produtor",
            "document": "269.498.980-29",
            "email": "fred_chien@yahoo.com.br",
            "phone": "(41) 9999-9999",
            "uf": "SP",
            "city": "São Paulo",
            "role": "buyer",
            "status": "disabled",
            "createdAt": "2022-06-27T17:57:09.333Z",
            "updatedAt": "2022-06-27T19:05:47.419Z",
            "__v": 0
        },
        "message": "Usuário desativado com sucesso"
    }
