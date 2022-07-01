---
id: authentication
title: Autenticação
sidebar_label: Autenticação
---

Guia de [Introdução](introduction.md).

### Fields

| field | type | required | description |
|---|---|---|---|
| email | string | true | - |
| password | string | true | - |

## Request

### Route

    POST /login

### Header

    Content-Type: application/json

### Body

    {
	    "email": "comprador@jobspace.com.br",
	    "password": "admin123?"
    }

## Response

### Status

    200

### Body

    {
	"success": true,
	"user": {
		"address": [],
		"_id": "62ba0b14754ba7c06965be4a",
		"name": "Fred Comprador",
		"document": "269.498.980-29",
		"email": "comprador@jobspace.com.br",
		"phone": "(41) 9999-9999",
		"password": "$2b$10$W96kKP9/d66XM6AQtyTLYugkw3T14UcN41ShiFaafysZK1n9mWpG6",
		"uf": "SP",
		"city": "São Paulo",
		"role": "buyer",
		"status": "active",
		"createdAt": "2022-06-27T19:55:00.801Z",
		"updatedAt": "2022-06-27T19:55:00.801Z",
		"__v": 0
	},
	"token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImFkZHJlc3MiOltdLCJfaWQiOiI2MmJhMGIxNDc1NGJhN2MwNjk2NWJlNGEiLCJuYW1lIjoiRnJlZCBDb21wcmFkb3IiLCJkb2N1bWVudCI6IjI2OS40OTguOTgwLTI5IiwiZW1haWwiOiJjb21wcmFkb3JAam9ic3BhY2UuY29tLmJyIiwicGhvbmUiOiIoNDEpIDk5OTktOTk5OSIsInBhc3N3b3JkIjoiJDJiJDEwJFc5NmtLUDkvZDY2WE02QVF0eVRMWXVna3czVDE0VWNONDFTaGlGYWFmeXNaSzFuOW1XcEc2IiwidWYiOiJTUCIsImNpdHkiOiJTw6NvIFBhdWxvIiwicm9sZSI6ImJ1eWVyIiwic3RhdHVzIjoiYWN0aXZlIiwiY3JlYXRlZEF0IjoiMjAyMi0wNi0yN1QxOTo1NTowMC44MDFaIiwidXBkYXRlZEF0IjoiMjAyMi0wNi0yN1QxOTo1NTowMC44MDFaIiwiX192IjowfSwiaWF0IjoxNjU2NjgyMTc2fQ.e_rEv9pIw3MaLzZr23qwrj_jxT3FZ0ByQtPsvradVg8"
    }
