---
id: get-all
title: Listar todos os endereços
sidebar_label: Listar todos os endereços
---

Guia de [Introdução](introduction.md).

Lista todos os endereços cadastrados no sistema.

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /address

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
            "_id": "62be3264aaae052a132e02c3",
            "cep": "80710000",
            "address": "Rua Padre Agostinho",
            "district": "Bigorrilho",
            "number": "1221",
            "complement": "Sem complemento",
            "uf": "PR",
            "city": "Curitiba",
            "status": "active",
            "createdAt": "2022-06-30T23:31:48.632Z",
            "updatedAt": "2022-06-30T23:31:48.632Z",
            "__v": 0
        },
        {
            "_id": "62be3251c0c8730b181a4d83",
            "cep": "80710000",
            "address": "Rua Padre Agostinho",
            "district": "Bigorrilho",
            "number": "1221",
            "complement": "Sem complemento",
            "uf": "PR",
            "city": "Curitiba",
            "status": "active",
            "createdAt": "2022-06-30T23:31:29.849Z",
            "updatedAt": "2022-06-30T23:31:29.849Z",
            "__v": 0
        },
        {
            "_id": "62be3249c0c8730b181a4d7f",
            "cep": "80710000",
            "address": "Rua Padre Agostinho",
            "district": "Bigorrilho",
            "number": "1221",
            "complement": "Sem complemento",
            "uf": "PR",
            "city": "Curitiba",
            "status": "active",
            "createdAt": "2022-06-30T23:31:21.513Z",
            "updatedAt": "2022-06-30T23:31:21.513Z",
            "__v": 0
        },
    ]

## Filters

| parameters | description |
|---|---|
| paginate | `true` ou `false` |
| limit | `integer >= 0` |
| page | `integer >= 1` |
| order | `asc` ou `desc` |
| atributo | `status`|

### Request

#### Route

    GET /address?paginate=true&limit=50&status=active

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
                "_id": "62be3264aaae052a132e02c3",
                "cep": "80710000",
                "address": "Rua Padre Agostinho",
                "district": "Bigorrilho",
                "number": "1221",
                "complement": "Sem complemento",
                "uf": "PR",
                "city": "Curitiba",
                "status": "active",
                "createdAt": "2022-06-30T23:31:48.632Z",
                "updatedAt": "2022-06-30T23:31:48.632Z",
                "__v": 0
            },
            {
                "_id": "62be3251c0c8730b181a4d83",
                "cep": "80710000",
                "address": "Rua Padre Agostinho",
                "district": "Bigorrilho",
                "number": "1221",
                "complement": "Sem complemento",
                "uf": "PR",
                "city": "Curitiba",
                "status": "active",
                "createdAt": "2022-06-30T23:31:29.849Z",
                "updatedAt": "2022-06-30T23:31:29.849Z",
                "__v": 0
            },
        ],
        "total": 32,
        "limit": 10,
        "page": 1,
        "pages": 4
    }