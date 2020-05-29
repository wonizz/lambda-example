---
description: 도서 리스트를 가져오는 API
---

# 01.getBook

{% api-method method="get" host="https://8xk6c6vlz2.execute-api.ap-northeast-2.amazonaws.com" path="/getBook" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="token" type="string" required=true %}
login token
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "Items": [
    {
      "duedate": "2020-05-14",
      "reservationYN": "N",
      "title": "k8s2"
    },
    {
      "duedate": "",
      "reservationYN": "Y",
      "title": "쿠버네티스패턴"
    },
    {
      "reservationYN": "N",
      "duedate": "2020-06-12",
      "author": "ahn sung tae",
      "title": "쿠버네티스패턴22"
    },
    {
      "duedate": "2020-05-14",
      "reservationYN": "N",
      "title": "k8s"
    },
    {
      "duedate": "",
      "reservationYN": "Y",
      "title": "쿠버네티스 패턴"
    }
  ],
  "Count": 5,
  "ScannedCount": 5
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=401 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "message": "invalid token"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



