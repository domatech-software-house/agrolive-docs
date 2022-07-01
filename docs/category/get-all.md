---
id: get-all
title: Listar todos categorias de produtos
sidebar_label: Listar todos categorias de produtos
---

Guia de [Introdução](introduction.md).

Lista todos as categorias de produtos cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /category

### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

### Body

    {}

## Response

### Status

    200

### Body

    [
        {
            "_id": "62baf618f4aa97135bb422ed",
            "name": "Hortifruti",
            "status": "active",
            "createdAt": "2022-06-28T12:37:44.284Z",
            "updatedAt": "2022-06-28T12:37:44.284Z",
            "__v": 0
        },
        {
            "_id": "62baf4cde86239188c23f35d",
            "name": "Grãos",
            "status": "active",
            "createdAt": "2022-06-28T12:32:13.229Z",
            "updatedAt": "2022-06-28T12:43:20.060Z",
            "__v": 0
        }
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `status` |

### Request

#### Route

    GET /category?paginate=true&limit=50&status=active

#### Header

    Content-Type: application/json
    Authorization: Bearer <<TOKEN>>

#### Body

    {}

### Response

#### Status

    200

#### Body

    {
        "docs": [
            {
                "_id": "62baf618f4aa97135bb422ed",
                "name": "Hortifruti",
                "status": "active",
                "createdAt": "2022-06-28T12:37:44.284Z",
                "updatedAt": "2022-06-28T12:37:44.284Z",
                "__v": 0
            },
            {
                "_id": "62baf4cde86239188c23f35d",
                "name": "Grãos",
                "status": "active",
                "createdAt": "2022-06-28T12:32:13.229Z",
                "updatedAt": "2022-06-28T12:43:20.060Z",
                "__v": 0
            }
        ],
        "total": 2,
        "limit": 10,
        "page": 1,
        "pages": 1
    }