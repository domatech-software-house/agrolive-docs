---
id: get
title: Listar comentário comprador
sidebar_label: Listar comentário comprador
---

Guia de [Introdução](introduction.md).

Listar um comentário comprador baseado no _id

Incluir token gerado no [login](authentication)

## Request

### Route

    GET /buyer-evaluation/:id

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
            "_id": "62bde9ebddc2405187855a82",
            "buyer": "62b9ed7df63d9bdac1b91a00",
            "payment": "62bdd69336fbb6ea855fdf3b",
            "establishment": "62ba0b14754ba7c06965be4a",
            "star": 5,
            "description": "Muito bom, um ótimo comprador.",
            "status": "active",
            "createdAt": "2022-06-30T18:22:35.610Z",
            "updatedAt": "2022-06-30T18:22:35.610Z",
            "__v": 0
        },
        "message": "Avaliação encontrado com sucesso!"
    }