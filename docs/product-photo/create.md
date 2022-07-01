---
id: create
title: Criar foto do produto
sidebar_label: Criar foto do produto
---

Guia de [Introdução](introduction.md).

### Fields

| field | type | required | description |
|---|---|---|---|
| _id | string | true | [Product](../product/create) |
| file | File | true | `Image` |

## Request

### Route

    POST /product-new-image

### Header

    Content-Type: multipart/form-data
    Authorization: Bearer <<TOKEN>>

### Body

    {
        "_id": "62bb4bee13961a124352936e",
        "file": File
    }


## Response

### Status

    200

### Body

    {},
