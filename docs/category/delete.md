---
id: delete
title: Remover categoria de produto
sidebar_label: Remover categoria de produto
---

Guia de [Introdução](introduction.md).

Nenhuma categoria de produto é deletado do sistema, mas sim, alterado o seu status de "active" para "disabled"

Incluir token gerado no [login](authentication)

## Request

### Route

    DELETE /category/:id

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
        "category": {
            "_id": "62baf4cde86239188c23f35d",
            "name": "Grãos",
            "status": "disabled",
            "createdAt": "2022-06-28T12:32:13.229Z",
            "updatedAt": "2022-06-28T12:43:07.559Z",
            "__v": 0
        },
        "message": "Categoria desativado com sucesso"
    }
