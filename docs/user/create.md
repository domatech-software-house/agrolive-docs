---
id: create
title: Criar usuário
sidebar_label: Criar usuário
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo usuário via API


### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |
| document | string | true | - |
| email | string | true | - |
| phone | string | false | - |
| password | string | true | - |
| uf | string | true | `length: 2` |
| city | string | true | - |
| address | objectId | false | [Address](../address/create) |
| role | string | true | `admin` `buyer` `producer` |



## Request

### Route

    POST /user

### Header

    Content-Type: application/json

### Body

    {
        "name": "Fred Comprador",
        "document": "26949898029",
        "email": "comprador@jobspace.com.br",
        "phone": "(41) 9999-9999",
        "password": "senha",
        "uf": "SP",
        "city": "São Paulo",
        "role": "buyer"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "user": {
            "name": "Fred Comprador",
            "document": "26949898029",
            "email": "comprador@jobspace.com.br",
            "phone": "(41) 9999-9999",
            "password": "$2b$10$W96kKP9/d66XM6AQtyTLYugkw3T14UcN41ShiFaafysZK1n9mWpG6",
            "uf": "SP",
            "city": "São Paulo",
            "role": "buyer",
            "status": "active",
            "_id": "62ba0b14754ba7c06965be4a",
            "createdAt": "2022-06-27T19:55:00.801Z",
            "updatedAt": "2022-06-27T19:55:00.801Z",
            "__v": 0
        },
        "message": "User cadastrado com sucesso"
    }

### Status

    200 - Usuário já cadastrado

### Body

    {
        "success": false,
        "error": true,
        "message": "Usuário já registrado com esse e-mail no sistema"
    }
