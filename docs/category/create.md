---
id: create
title: Criar categoria de produto
sidebar_label: Criar categoria de produto
---

Guia de [Introdução](introduction.md).

Informações para cadastro de nova categoria de produto via API

Somente usuário admin consegue cadastrar


### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |



## Request

### Route

    POST /category

### Header

    Content-Type: application/json

### Body

    {
        "name": "Hortifruit"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "category": {
            "name": "Hortifruti",
            "status": "active",
            "_id": "62baf618f4aa97135bb422ed",
            "createdAt": "2022-06-28T12:37:44.284Z",
            "updatedAt": "2022-06-28T12:37:44.284Z",
            "__v": 0
        },
        "message": "Categoria cadastrada com sucesso"
    }