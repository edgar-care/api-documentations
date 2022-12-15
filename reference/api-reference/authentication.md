# 🔓 Authentication

Use the following endpoints to authenticate yourself as a `Patient` or a `Doctor` .

{% hint style="info" %}
Keep in mind that you have to use one of those to be granted a <mark style="color:red;">token</mark> that will enable you to use the whole API.
{% endhint %}

<details>

<summary>Token format</summary>

#### For the doctor :

```json
"doctor": {
    "id": string,
    "password": string,
    "name": string,
    "last_name": string,
    "email": string,
    "address": string
 }
```

#### For the patient

```json
"patient": {
    "id": string,
    "password": string,
    "name": string,
    "last_name": string,
    "email": string,
    "age": int,
    "height": int,
    "weight": int,
    "sex": string"
 }
```



</details>

## Login

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/auth/d/login" method="post" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/auth/p/login" method="post" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

## Register

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/auth/d/register" method="post" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/auth/p/register" method="post" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}
