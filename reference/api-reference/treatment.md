# ⚕️ Treatment

<mark style="color:green;">`POST`</mark> `/dashboard/treatment`

{% tabs %}
{% tab title="Body" %}
```
{
  "name": "String",
  "disease_id": "String", #Not necessary
  "still_relevant": Boolean,
  "treatments": [
    {
      "period": ["ENUM"],
      "day": ["ENUM"],
      "quantity": Int,
      "medicine_id": "String"
    }
  ]
}
```
{% endtab %}

{% tab title="return 201" %}
```json
{
	"treatment": {
		"name": "String",
		"still_relevant": Boolean,
		"treatment": [
			{
				"id": "String",
				"period": [
					"ENUM",
					
				],
				"day": [
					"ENUM"
				],
				"quantity": Int,
				"medicine_id": "String"
			}
		]
	}
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/dashboard/treatment/{id}`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"treatment": {
		"id": "String",
		"period": [
			"ENUM"
		],
		"day": [
			"ENUM",
		],
		"quantity": Int,
		"medicine_id": "String"
	}
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark>` ``/dashboard/treatments`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"treatments": [
		{
			"id": "String",
			"period": [
				"ENUM"
			],
			"day": [
				"ENUM"
			],
			"quantity": Int,
			"medicine_id": "String"
		},
	]
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:orange;">`PUT`</mark> `/dashboard/treatment/{id}`

{% tabs %}
{% tab title="Body" %}
```json
{
  "Treatments": [
    {
      "ID": "String",
      "medicine_id": "String",
      "Period": ["ENUM"],
      "Day": ["ENUM"],
      "Quantity": Int
    },
  ]
}
```
{% endtab %}

{% tab title="Return 200 " %}
```json
{
	"treatment": [
		{
			"id": "String",
			"period": [
				"ENUM"
			],
			"day": [
				"ENUM"
			],
			"quantity": Int,
			"medicine_id": "String"
		},
	]
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:red;">`DELETE`</mark> `/dashboard/treatment/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"delete": true
}
```
{% endtab %}
{% endtabs %}
