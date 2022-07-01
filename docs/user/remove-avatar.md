---
id: remove-avatar
title: Remover Avatar
sidebar_label: Remover Avatar
---

Guia de [Introdução](introduction.md).

Excluir avatar de usuário

Incluir token gerado no [login](authentication)


## Request

### Route

    delete /user-avatar

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
            "updatedAt": "2022-06-27T19:06:29.021Z",
            "__v": 0,
            "avatar": "",
            "avatarKey": ""
        },
        "message": "Foto deletada com sucesso"
    }
