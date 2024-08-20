# ⚕️ Treatment

<mark style="color:green;">`POST`</mark> `/dashboard/treatment`

{% tabs %}
{% tab title="Body" %}
```
{
  "name": "String",       # a renseigner dans le cas ou la maladie n'existe pas
  "disease_id": "String", # a renseigner lorsque l'on veut rajouter un treatement a une maladie deja existante
  "still_relevant": Boolean,
  "treatments": [
    {
      "period": ["ENUM"],
      "day": ["ENUM"],
      "quantity": Int,
      "medicine_id": "String"
      "start_date": Int,
      "end_date": Int,
      
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
				"start_date": Int,
				"end_date": Int,
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
		"start_date": Int,
		"end_date": Int,
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
[
	{
		"antedisease": {
			"id": String,
			"name": String,
			"chronicity": Int,
			"still_relevant": Boolean
		},
		"treatments": [
			{
				"id": String,
				"period": [
					ENUM
				],
				"day": [
					ENUM
				],
				"quantity": int,
				"medicine_id": String
				"start_date": Int,
				"end_date": Int,
			}
		]
	},
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:orange;">`PUT`</mark> `/dashboard/treatment`

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
      "start_date": Int,
      "end_date": Int,
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
			"start_date": Int,
			"end_date": Int,
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
