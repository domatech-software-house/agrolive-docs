---
id: delete
title: Remover foto do produto
sidebar_label: Remover foto do produto
---

Guia de [Introdução](introduction.md).

## Request

### Route

    DELETE /product-delete-photo/:id

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
        "message": "Foto deletada com sucesso"
    }
