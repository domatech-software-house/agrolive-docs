---
id: get
title: Listar comentário venda
sidebar_label: Listar comentário venda
---

Guia de [Introdução](introduction.md).

Listar um comentário venda baseado no _id

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /request-evaluation/:id

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
        "request": {
            "_id": "62bde471ad1bc86a3be0dc1f",
            "buyer": "62ba0b14754ba7c06965be4a",
            "payment": "62bdd69336fbb6ea855fdf3b",
            "establishment": "62ba0ae8754ba7c06965be47",
            "star": 4,
            "description": "Muito bom, gostei",
            "status": "active",
            "createdAt": "2022-06-30T17:59:13.116Z",
            "updatedAt": "2022-06-30T17:59:13.116Z",
            "__v": 0
        },
        "message": "Avaliação encontrado com sucesso!"
    }