---
id: delete
title: Remover estabelecimento
sidebar_label: Remover estabelecimento
---

Guia de [Introdução](introduction.md).

Nenhum estabelecimento é deletado do sistema, mas sim, alterado o seu status de "active" para "disabled"

Incluir token gerado no [login](authentication)

## Request

### Route

    DELETE /establishments/:id

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
            "producer": "62ba0ae7754ba7c06965be45",
            "name": "Loja teste produtor",
            "status": "disabled",
            "createdAt": "2022-06-27T19:54:16.152Z",
            "updatedAt": "2022-06-27T20:23:13.283Z",
            "__v": 0,
            "location": {
                "type": "Point",
                "coordinates": [
                    -46.6323597,
                    -23.5653314
                ],
                "_id": "62ba110d023d6e124806cdda"
            }
        },
        "message": "Estabelecimento desativado com sucesso!"
    }
