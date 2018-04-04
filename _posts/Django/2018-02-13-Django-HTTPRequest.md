---
layout: post
title: HTTP Request와 REST API
category: Django
tags: [http request, rest api]
comments: true
---



HTTP = hypertext transfer protocol

Client와 Server는 Request,Response로 소통한다.

Cosume a resource => GET

Create a resource => POST

Update a resource => PUT

Delete a resource => DELETE

Header

Body



Client : google.com/users/

Server : GET google.com/users/ => (look) => URL => View()



REST API

명사만 사용

```
GET /owners/nicolas/dogs  -> list of all

POST /owners/nicolas/dogs -> create a dog for nicolas

PUT /owners/nicolas/dogs -> update all of nicolas dogs

DELETE /owners/nicolas/dogs -> bye bye

method만 바꾸고 같은 api 사용

```