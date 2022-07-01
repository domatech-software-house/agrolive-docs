---
id: create
title: Criar tipo de produto
sidebar_label: Criar tipo de produto
---

Guia de [Introdução](introduction.md).

Informações para cadastro de novo tipo de produto via API

Somente usuário admin consegue cadastrar


### Fields

| field | type | required | description |
|---|---|---|---|
| name | string | true | - |



## Request

### Route

    POST /types

### Header

    Content-Type: application/json

### Body

    {
        "name": "SC"
    }

## Response

### Status

    200

### Body

    {
        "success": true,
        "types": {
            "name": "SC",
            "status": "active",
            "_id": "62bafdb7b259708bc69dd017",
            "createdAt": "2022-06-28T13:10:15.133Z",
            "updatedAt": "2022-06-28T13:10:15.133Z",
            "__v": 0
        },
        "message": "Tipo de produto cadastrado com sucesso"
    }