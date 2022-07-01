---
id: avatar
title: Avatar
sidebar_label: Avatar
---

Guia de [Introdução](introduction.md).

Inclui uma nova imagem no cadastro de estabelecimento

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| file | file | true  | `mime-type image/*` |

## Request

### Route

    PUT /establishments-avatar/:id-establishment

### Header

    Content-Type: multipart/form-data
    Authorization: Bearer <<TOKEN>>

### Body

    {
        file: File
    }

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
            "updatedAt": "2022-06-27T21:00:41.566Z",
            "__v": 0,
            "location": {
                "type": "Point",
                "coordinates": [
                    -46.6323597,
                    -23.5653314
                ],
                "_id": "62ba11c42db63bd80cbb8528"
            },
            "avatar": "https://domatech-tests.s3.amazonaws.com/2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg",
            "avatarKey": "2bf74486e599bba9318905a82e0926eb-1649170157827.jpeg"
        },
        "message": "Foto cadastrada com sucesso"
    }
