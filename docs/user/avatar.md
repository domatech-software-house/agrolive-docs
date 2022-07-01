---
id: avatar
title: Avatar
sidebar_label: Avatar
---

Guia de [Introdução](introduction.md).

Inclui uma nova imagem no cadastro de usuário

Incluir token gerado no [login](authentication)

### Fields

| field | type | required | description |
|---|---|---|---|
| file | file | true  | `mime-type image/*` |

## Request

### Route

    PUT /user-avatar

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
        "user": {
            "_id": "62b9ed7df63d9bdac1b91a00",
            "name": "Fred Chien Produtor",
            "document": "344.367.320-10",
            "email": "fredchien@jobspace.com.br",
            "phone": "(41) 9999-9999",
            "uf": "PR",
            "city": "Curitiba",
            "role": "producer",
            "status": "active",
            "createdAt": "2022-06-27T17:48:45.956Z",
            "updatedAt": "2022-06-27T19:06:45.671Z",
            "__v": 0,
            "avatar": "https://domatech-tests.s3.amazonaws.com/d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg",
            "avatarKey": "d9429480185cb9dd05066dac53ce0b2f-1649170157827.jpeg"
        },
        "message": "Foto cadastrada com sucesso"
    }
