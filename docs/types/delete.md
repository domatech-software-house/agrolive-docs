---
id: delete
title: Remover tipo de produto
sidebar_label: Remover tipo de produto
---

Guia de [Introdução](introduction.md).

Nenhum tipo de produto é deletado do sistema, mas sim, alterado o seu status de "active" para "disabled"

Incluir token gerado no [login](authentication)

## Request

### Route

    DELETE /types/:id

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
        "types": {
            "name": "SC",
            "status": "disabled",
            "_id": "62bafdb7b259708bc69dd017",
            "createdAt": "2022-06-28T13:10:15.133Z",
            "updatedAt": "2022-06-28T13:10:15.133Z",
            "__v": 0
        },
        "message": "Tipo de produto desativado com sucesso"
    }
