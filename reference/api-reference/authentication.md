# 🔓 Authentication

Use the following endpoints to authenticate yourself as a `Patient` or a `Doctor` .

{% hint style="info" %}
Keep in mind that you have to use one of those to be granted a <mark style="color:red;">token</mark> that will enable you to use the whole API. We are using [JsonWebToken](https://jwt.io) for managing those.
{% endhint %}

<details>

<summary>Token Payload</summary>

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



Case 2FA activate

{% tabs %}
{% tab title="BODY RETURN" %}
```
{
	"Methods": [
		"ENUM",
	],
	"DeviceInfo": {
		"os": "String",
		"browser": "String",
		"location": "String"
	}
}
```
{% endtab %}

{% tab title="Status code 200" %}

{% endtab %}
{% endtabs %}

##

## Register

<mark style="color:green;">`POST`</mark> `/auth/d/register`

{% tabs %}
{% tab title="Body" %}
```json
{
	"email": "string", 
	"password": "string",
	"name": "string",
	"firstname": "string",
	"address": {
		"street": "string", 
		"zip_code": "string", 
		"country": "string",
		"city": "string"
	}
}
```
{% endtab %}

{% tab title="Return body" %}
```json
{
    "token": "string"
}
```
{% endtab %}
{% endtabs %}

<mark style="color:green;">`POST`</mark> `/auth/p/register`

{% tabs %}
{% tab title="Body" %}
```
{
    "email": "string",
    "password": "string"
}
```
{% endtab %}

{% tab title="Return body" %}
```
{
    "token": "string"
}
```
{% endtab %}
{% endtabs %}
