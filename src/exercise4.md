## Тестирование API с Postman

https://crimson-firefly-167786.postman.co/workspace/f0540550-14ca-4977-8580-57d3af75a1af/request/28044271-9dc5881f-3efb-47f3-950e-1979b2351d30

### Отчёт запросов и ответов Fake REST Api.

#### Activities

***1. GET /api/v1/Activities***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса** Отсутствует

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sat, 17 Jun 2023 16:16:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id": 1, "title": "Activity 1", "dueDate": "2023-06-17T17:16:34.0366439+00:00", "completed": false},
{"id": 2, "title": "Activity 2", "dueDate": "2023-06-17T18:16:34.036646+00:00", "completed": true},
{"id": 3, "title": "Activity 3", "dueDate": "2023-06-17T19:16:34.0366463+00:00", "completed": false},
{"id": 4, "title": "Activity 4", "dueDate": "2023-06-17T20:16:34.0366466+00:00", "completed": true},
{"id": 5, "title": "Activity 5", "dueDate": "2023-06-17T21:16:34.0366469+00:00", "completed": false}

***2. POST /api/v1/Activities***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{activity_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-18T06:44:51.020Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 06:44:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-18T06:44:51.02Z","completed":true}

***3. GET /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат** 

 - получить 
 
**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 06:51:29 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"title":"Activity 1","dueDate":"2023-06-18T06:51:29.9537052+00:00","completed":false}

***4. GET /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 06:55:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-572c0cfd8407c240ad1d58a9f91de03a-bb3eb1d2da09884e-00"}

***5. PUT /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат**

 - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T15:25:50.679Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:01:20 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-17T15:25:50.679Z","completed":true}

***6. PUT /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{body_no}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:04:17 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**

0

***7. PUT /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{body_word}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": put,
  "title": "string",
  "dueDate": "2023-06-17T14:41:11.361Z",
  "completed": true
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:10:17 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-f6ff49391c14db4f9e4ca1921e08d8e7-aa1b6f7a40f47a43-00","errors":{"id":["The value 'post put' is not valid."],"$.id":["'p' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."]}}

***8. DELETE /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{one_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:06:32 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**
0

***9. DELETE /api/v1/Activities/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{12_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:12:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
**Тело ответа**

0

***10. GET /api/v1/Activities/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{bag_id}}

**Ожидаемый результат**

- получить запрос c кодом 200 (а получаем 404)

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:03:35 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-fe4e97ed029508408f25c849b697e572-e25333a49628bb45-00"}

***11. POST /api/v1/Activities*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат** 

- получить запрос c 400 в Swagger 200 получаем, в Postman 405

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "title": "string",
  "dueDate": "2023-06-17T22:12:40.517Z",
  "completed": true
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:08:00 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0

***12. PUT /api/v1/Activities/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}
**Ожидаемый результат**

 - получить запрос 400, (получаем 200)

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
{
  "id": 0,
  "title": "string",
  "dueDate": "2023-06-17T22:17:34.092Z",
  "completed": true
}
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:13:01 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","dueDate":"2023-06-17T22:17:34.092Z ","completed":true}

***13. PUT /api/v1/Activities/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Activities/{{minus_id}}

**Ожидаемый результат**

 - получить запрос с кодом 400 (получаем 200)

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
{
  "id": -1,
  "title": "string",
  "dueDate": "2023-06-17T22:17:34.092Z",
  "completed": true
}
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:18:39 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"title":"string","dueDate":"2023-06-17T22:17:34.092Z ","completed":true}

###  Authors

*** 14. GET /api/v1/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors{{activity_id}}

**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.2
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:24:10 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"},{"id":2,"idBook":1,"firstName":"First Name 2","lastName":"Last Name 2"},{"id":3,"idBook":1,"firstName":"First Name 3","lastName":"Last Name 3"},{"id":4,"idBook":1,"firstName":"First Name 4","lastName":"Last Name 4"},

***15. POST /api/v1/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{activity_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:51:14 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}

***16. POST /api/v1/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_no}}

**Ожидаемый результат**

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:54:33 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.13","title":"Unsupported Media Type","status":415,"traceId":"00-9b303e447ec7b94887685c07a0856df9-c59a4841fc752c45-00"}

***17. POST /api/v1/Authors***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_word}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": post,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}
**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07 6:57:44 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0

***18. GET /api/v1/Authors/authors/books/{idBook}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{one_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:01:23 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[{"id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"}, {"id":2,"idBook":1,"firstName":"First Name 2","lastName":"Last Name 2"}]

***19. GET /api/v1/Authors/authors/books/{idBook}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/authors/books/{{12_id}}
**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:04:01 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-d3107340761be74c9925fb8056a464a1-b3e7126c672a9e48-00","errors": {"idBook": ["The value '111111111111' is not valid."]}}

***20. GET /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:06:15 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":1,"firstName":"First Name 1","lastName":"Last Name 1"}

***21. GET /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:08:43 GMT
Server: Kestrel
Transfer-Encoding: chunked
*Тело ответа**
{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-9b4048c8a40d42419e89b15472897203-4bb9fe81a8dd0e42-00","errors": {"id": ["The value '111111111111' is not valid."]}}

***22. PUT /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:11:33 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}

***23. PUT /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:16:24 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-d3ca6c3792458d45b5068b01a0155624-0f415515d1ec9c1f-00","errors":{"id":["The value '111111111111' is not valid."]}}

***24. PUT /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_no}
}
**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:18:43 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**

0

***25. PUT /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{body_word}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": put,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:20:22 GMT
Server: Kestrel
Transfer-Encoding: 

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-8d94d80bd08bce4690d5fbaf96091a8d-2f795622c5dd765a-00","errors":{"id":["The value 'post put' is not valid."],"$.id":"'p' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."}}

***26. DELETE /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:22:33 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**

0

***27. DELETE /api/v1/Authors/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{12_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 07:24:41 GMT
Server: Kestrel
Transfer-Encoding: chunked

**Тело ответа**

0

***28. POST /api/v1/Authors*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат** 

- получить запрос с ошибкой 400 (id=-1) в Swagger UI код 200 показывает, в Postman 415

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 07:26:59 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0

***29. PUT /api/v1/Authors/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат** 

- получить запрос с кодом 400, а получаем с кодом 200 вводя -1

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:31:09 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"firstName":"string","lastName":"string"}

***30. PUT /api/v1/Authors/{id}*** (BAG)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Authors/{{minus_id}}

**Ожидаемый результат**  

- получить запрос с кодом 400, а получаем - 200 (id=-1).

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
{
  "id": -1,
  "idBook": 0,
  "firstName": "string",
  "lastName": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:41:11 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"idBook":0,"firstName":"string","lastName":"string"}

### Books

***31. GET /api/v1/Books***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:46:02 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

"id":1,"title":"Book 1","description":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n","pageCount":100

***32. POST /api/v1/Books***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{activity_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T22:30:48.937Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:49:28 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-17T22:30:48.937Z"}

***33. GET /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 07:51:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0
**Тело ответа**

"id":1,"title":"Book 1","description":"Lorem lorem lorem. Lorem lorem lorem. Lorem lorem lorem.\n","pageCount":100,"excerpt"

***34. GET /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 08:10:52 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-83533691e90c354a9c0166386a73a937-ff45cc717d32f61f-00"}

***35. PUT /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T22:33:42.901Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 08:12:51 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-17T22:33:42.901Z"}


***36. PUT /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{body_no}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T22:38:42.901Z"
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 08:17:35 GMT
Server: Kestrel
Allow: GET, POST

**Тело ответа**

0

***37. PUT /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{body_word}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": ,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T22:38:42.901Z"
}

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8
Date: Sun, 18 Jun 2023 08:20:39 GMT
Server: Kestrel
Transfer-Encoding: 

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.1","title":"One or more validation errors occurred.","status":400,"traceId":"00-08dfd498d1d7aa4a88dee17e3e697ff8-7d1dea78fb93fd47-00","errors":{"id":["The value 'post put' is not valid."],"$.id":',' is an invalid start of a value. Path: $.id | LineNumber: 1 | BytePositionInLine: 8."}}

***38. DELETE /api/v1/Books/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 08:22:50 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**

0

***39. POST /api/v1/Books*** (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат** 

- получить запрос с кодом 400, а ) в Swagger UI код 200 показывает, в Postman 405

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T23:30:03.334Z"
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 08:24:34 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0

***40. PUT /api/v1/Books/{id}*** (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат**  

- получить запрос 400, а получаем 200 вводя в ID -1
**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T23:31:43.538Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 08:29:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-17T23:31:43.538Z"}

***41. PUT /api/v1/Books/{id}*** (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Books/{{minus_id}}

**Ожидаемый результат** 

- получить запрос с кодом 400, а получаем код 200 вводя в тело запроса -1

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id":-1,
  "title": "string",
  "description": "string",
  "pageCount": 0,
  "excerpt": "string",
  "publishDate": "2023-06-17T22:31:43.538Z"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 08:32:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"title":"string","description":"string","pageCount":0,"excerpt":"string","publishDate":"2023-06-17T22:31:43.538Z"}

### CoverPhotos

***42. GET /api/v1/CoverPhotos***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:05:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"},{"id":2,"idBook":2,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 2&w=250&h=350"},{"id":3,"idBook":3,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 3&w=250&h=350"},

***43. POST /api/v1/CoverPhotos***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{activity_id}}


**Ожидаемый результат**  
- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:10:31 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}

***44. GET /api/v1/CoverPhotos/books/covers/{idBook}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{one_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: b069eefa-87d7-4336-a833-344abdf6a16c
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:13:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"}]

*** 45. GET /api/v1/CoverPhotos/books/covers/{idBook}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{minus_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:15:46 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[]

***46. GET /api/v1/CoverPhotos/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{one_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:17:55 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[{"id":1,"idBook":1,"url":"https://placeholdit.imgix.net/~text?txtsize=33&txt=Book 1&w=250&h=350"}]

***47. GET /api/v1/CoverPhotos/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/books/covers/{{minus_id}}

**Ожидаемый результат**

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:19:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

[]

***48. PUT /api/v1/CoverPhotos/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{body_0}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:21:50 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}

***49. PUT/api/v1/CoverPhotos/{id}

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{one_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:24:08 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"idBook":0,"url":"string"}

***50. DELETE /api/v1/CoverPhotos/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{one_id}}

**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 11:26:21 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**

0

***51. POST /api/v1/CoverPhotos***  (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos{{minus_id}}

**Ожидаемый результат** 

- получить запрос с кодом 400, в Swagger UI код 200 показывает, в Postman 404

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 11:28:34 GMT
Server: Kestrel

**Тело ответа**

0

***52. PUT /api/v1/CoverPhotos/{id}*** (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{minus_id}}

**Ожидаемый результат**  - получить запрос с кодом 400 . а получаем с кодом 200.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:42:49 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"idBook":0,"url":"string"}

***53. PUT /api/v1/CoverPhotos/{id}*** (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/CoverPhotos/{{minus_id}}

**Ожидаемый результат** 

 - получить запрос с кодом 400, а получаем с кодом 200.
**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "idBook": 0,
  "url": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 11:36:36 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"idBook":0,"url":"string"}

### Users

***54. GET /api/v1/Users***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users{{activity_id}}

**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Thu, 15 Jun 2023 12:10:57 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"userName":"User 1","password":"Password1"},{"id":2,"userName":"User 2","password":"Password2"},

**55. *POST /api/v1/Users***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users{{activity_id}}

**Ожидаемый результат**

- получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:15:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"userName":"string","password":"string"}


***56. GET /api/v1/Users/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:17:53 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":1,"userName":"User 1","password":"Password1"}

***57. GET /api/v1/Users/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:20:07 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-27008e01c15282448a596190961b42de-7b2bed9850825c49-00"}


***58. PUT /api/v1/Users/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат** 

 - получить запрос

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**
{
  "id": 0,
  "userName": "string",
  "password": "string"
}
**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:21:58 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"userName":"string","password":"string"}

***59. DELETE /api/v1/Users/{id}***

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{one_id}}

**Ожидаемый результат** 

- получить запрос

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Postman-Token: 6f6e29aa-f58e-4ef9-b874-3456a646e1e0
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 12:24:19 GMT
Server: Kestrel
api-supported-versions: 1.0

**Тело ответа**

0

***60. GET /api/v1/Users/{id}*** (БАГ )

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{bag_id}}

**Ожидаемый результат** 

- получить запрос с кодом 200, а получаем 404 

**Заголовок запроса**

User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

0

**Заголовки ответа**

Content-Type: application/problem+json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:27:38 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"type":"https://tools.ietf.org/html/rfc7231#section-6.5.4","title":"Not Found","status":404,"traceId":"00-e138e51e5f53794ebb4009998473c7bf-ffb77fbe02e40e47-00"}


***61. POST /api/v1/Users***   (Баг)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  

- получить запрос 400, в Swagger UI код 200 показывает, в Postman 405

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Length: 0
Date: Sun, 18 Jun 2023 12:30:57 GMT
Server: Kestrel
Allow: DELETE, GET, PUT

**Тело ответа**

0

***62. PUT /api/v1/Users/{id}***   (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат** 

- получить запрос с кодом 400, а получаем с кодом 200 вводя -1 в ID запроса.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": 0,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:34:12 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":0,"userName":"string","password":"string"}

***63. PUT /api/v1/Users/{id}***    (БАГ)

**URL** https://fakerestapi.azurewebsites.net/api/v1/Users/{{minus_id}}

**Ожидаемый результат**  

- получить запрос с кодом 400 , получаем с кодом 200 вводя -1 в тело запроса.

**Заголовок запроса**

Content-Type: application/json
User-Agent: PostmanRuntime/7.32.3
Accept: */*
Cache-Control: no-cache
Host: fakerestapi.azurewebsites.net
Accept-Encoding: gzip, deflate, br
Connection: keep-alive

**Тело запроса**

{
  "id": -1,
  "userName": "string",
  "password": "string"
}

**Заголовки ответа**

Content-Type: application/json; charset=utf-8; v=1.0
Date: Sun, 18 Jun 2023 12:37:24 GMT
Server: Kestrel
Transfer-Encoding: chunked
api-supported-versions: 1.0

**Тело ответа**

{"id":-1,"userName":"string","password":"string"}
