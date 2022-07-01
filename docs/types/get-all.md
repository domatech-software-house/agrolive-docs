---
id: get-all
title: Listar todos tipos de produtos
sidebar_label: Listar todos tipos de produtos
---

Guia de [Introdução](introduction.md).

Lista todos os tipos de produtos cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /types

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
            "_id": "62bafdb7b259708bc69dd017",
            "name": "SC",
            "status": "active",
            "createdAt": "2022-06-28T13:10:15.133Z",
            "updatedAt": "2022-06-28T13:10:15.133Z",
            "__v": 0
        },
        {
            "_id": "62bafdb2b259708bc69dd015",
            "name": "CX",
            "status": "active",
            "createdAt": "2022-06-28T13:10:10.435Z",
            "updatedAt": "2022-06-28T13:10:10.435Z",
            "__v": 0
        },
        {
            "_id": "62bafdacb259708bc69dd013",
            "name": "KG",
            "status": "active",
            "createdAt": "2022-06-28T13:10:04.426Z",
            "updatedAt": "2022-06-28T13:10:04.426Z",
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

    GET /types?paginate=true&limit=50&status=active

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
                "_id": "62bafdb7b259708bc69dd017",
                "name": "SC",
                "status": "active",
                "createdAt": "2022-06-28T13:10:15.133Z",
                "updatedAt": "2022-06-28T13:10:15.133Z",
                "__v": 0
            },
            {
                "_id": "62bafdb2b259708bc69dd015",
                "name": "CX",
                "status": "active",
                "createdAt": "2022-06-28T13:10:10.435Z",
                "updatedAt": "2022-06-28T13:10:10.435Z",
                "__v": 0
            },
            {
                "_id": "62bafdacb259708bc69dd013",
                "name": "KG",
                "status": "active",
                "createdAt": "2022-06-28T13:10:04.426Z",
                "updatedAt": "2022-06-28T13:10:04.426Z",
                "__v": 0
            }
        ],
        "total": 3,
        "limit": 10,
        "page": 1,
        "pages": 1
    }