# 🗃️ Follow up treatment

Cocher un treatment qui a été pris

<mark style="color:green;">`POST`</mark> `/dashboard/treatment/follow-up`

{% tabs %}
{% tab title="Body" %}
```json
{
	"treatment_id": String,
	"date": int,
	"period": ["ENUM"]
}
```
{% endtab %}

{% tab title="Return 201" %}
```json
{
	"id": "String",
	"treatment_id": "String",
	"date": Int,
	"period": [
		"ENUM"
	]
}
```
{% endtab %}
{% endtabs %}

Récupérer un traitment qui a été pris (cocher)

<mark style="color:blue;">`GET`</mark> `/dashboard/treatment/follow-up/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"id": "String",
	"treatment_id": "String",
	"date": Int,
	"period": [
		"ENUM"
	]
}
```
{% endtab %}
{% endtabs %}

Récupérer tous les tratitements qui on été pris (cocher)

<mark style="color:blue;">`GET`</mark> `/dashboard/treatment/follow-up`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"id": "String",
	"treatment_id": "String",
	"date": Int,
	"period": [
		"ENUM"
	]
},
```
{% endtab %}
{% endtabs %}

Décocher un traitement qui a été pris\ <mark style="color:red;">`DELETE`</mark> `/dashboard/treatment/follow-up/{id}`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"delete": true
}
```
{% endtab %}
{% endtabs %}
