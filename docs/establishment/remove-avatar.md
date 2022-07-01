---
id: remove-avatar
title: Remover Avatar
sidebar_label: Remover Avatar
---

Guia de [Introdução](introduction.md).

Excluir avatar de estabelecimento

Incluir token gerado no [login](authentication)


## Request

### Route

    delete /establishments-avatar/:id-establishment

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
            "status": "active",
            "createdAt": "2022-06-27T19:54:16.152Z",
            "updatedAt": "2022-06-27T21:00:35.120Z",
            "__v": 0,
            "location": {
                "type": "Point",
                "coordinates": [
                    -46.6323597,
                    -23.5653314
                ],
                "_id": "62ba11c42db63bd80cbb8528"
            },
            "avatar": "",
            "avatarKey": ""
        },
        "message": "Foto deletada com sucesso"
    }
