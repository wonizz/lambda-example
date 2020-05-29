---
description: 도서 대출 관련 API
---

# 03.checkoutbook

{% api-method method="post" host="https://8xk6c6vlz2.execute-api.ap-northeast-2.amazonaws.com" path="/checkoutBook" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="booktitle" type="string" required=true %}
 도서 제목
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
 예약자 이메일
{% endapi-method-parameter %}

{% api-method-parameter name="rsrvdate" type="string" required=true %}
 예약 날
{% endapi-method-parameter %}

{% api-method-parameter name="duedate" type="string" required=true %}
 반납 예정
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
Authentication token to track down who is emptying our stocks.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
   "Items":[
      {
         "duedate":"2020-05-14",
         "reservationYN":"N",
         "title":"k8s2"
      },
      {
         "duedate":"2020-06-12",
         "reservationYN":"N",
         "title":"쿠버네티스패턴"
      },
      {
         "reservationYN":"N",
         "duedate":"2020-06-12",
         "author":"ahn sung tae",
         "title":"쿠버네티스패턴22"
      },
      {
         "duedate":"2020-05-14",
         "reservationYN":"N",
         "title":"k8s"
      },
      {
         "duedate":"",
         "reservationYN":"Y",
         "title":"쿠버네티스 패턴"
      }
   ],
   "Count":5,
   "ScannedCount":5
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "bad request"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{
    "message": "invalid token"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "message": "Not Found"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "internal server error"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



