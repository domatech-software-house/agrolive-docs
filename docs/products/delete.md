---
id: delete
title: Remover produto
sidebar_label: Remover produto
---

Guia de [Introdução](introduction.md).

Nenhum produto é deletado do sistema, mas sim, alterado o seu status de "active" para "disabled"

Incluir token gerado no [login](authentication)

## Request

### Route

    DELETE /product/:id

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
        "product": {
            "_id": "62bb3904342bf1829a2a989d",
            "establishment": "62ba0ae8754ba7c06965be47",
            "category": "62baf4cde86239188c23f35d",
            "type": "62bafdacb259708bc69dd013",
            "address": "62bb0621305ed651bf2bf95a",
            "name": "Batata Doce",
            "criteria": [
                "Roxa"
            ],
            "description": "Uma breve descrição do produto",
            "productPhoto": [],
            "date": "2022-06-28T13:10:04.426Z",
            "shipping": [
                {
                    "distance": "fixed",
                    "price": 200
                }
            ],
            "stock": 200,
            "price": 200,
            "status": "disabled",
            "createdAt": "2022-06-28T17:23:16.518Z",
            "updatedAt": "2022-06-28T17:49:24.677Z",
            "__v": 0
        },
        "message": "Produto desativado com sucesso!"
    }
