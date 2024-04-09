# 💊 Medicine

<mark style="color:green;">`POST`</mark> `/medicine`

{% tabs %}
{% tab title="Body" %}
```json
{
		"name":             "String",
		"unit":             "String",
		"target_diseases": ["String"],
		"treated_symptoms": ["String"],
		"side_effects":     ["String"]
}
```
{% endtab %}

{% tab title="Return 201" %}
```json
{
	"medicament": {
		"id": "String",
		"name": "String",
		"unit": "piStringpi",
		"target_diseases": [
			"String",
		],
		"treated_symptoms": [
			"String",
		],
		"side_effects": [
			"String"
		]
	}
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/medicine`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"medicament": [
		{
			"id": "String",
			"name": "String",
			"unit": "String",
			"target_diseases": [
				"String"
			],
			"treated_symptoms": [
				"String"
			],
			"side_effects": [
				"String"
			]
		}
	]
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/medicine/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"medicament": {
		"id": "660876c2db5877da92d71b13",
		"name": "String",
		"unit": "String",
		"target_diseases": [
			"String"
		],
		"treated_symptoms": [
			"String"
		],
		"side_effects": [
			"String"
		]
	}
}
```
{% endtab %}
{% endtabs %}
