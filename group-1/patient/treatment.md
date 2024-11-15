# ⚕️ Treatment

| ENUM    |
| ------- |
| JOUR    |
| SEMAINE |
| MOIS    |
| ANNEE   |







<mark style="color:green;">`POST`</mark> `/dashboard/treatment`

{% tabs %}
{% tab title="Body" %}
```
{
		"medical_antecedent_id": "String", => ID du medical Antecedent au quelle vous voulez rattacher ce treatment
		"created_by": "String",
		"start_date": Int,
		"end_date": Int,
		"medicines": [
			{
				"medicine_id": "String",
				"comment": "String",
				"period": [
					{
						"quantity": Int,
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "ENUM",
						"period_length": Int,
						"period_unit": "ENUM"
					}
				]
			}
		]
}
```
{% endtab %}

{% tab title="return 201" %}
```json
[
	{
		"id": "String",
		"created_by": "String",
		"start_date": Int,
		"end_date": Int,
		"medicines": [
			{
				"medicine_id": "String",
				"comment": "String",
				"period": [
					{
						"quantity": Int,
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "ENUM",
						"period_length": Int,
						"period_unit": "ENUM"
					}
				]
			}
		]
	}
]
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
	"id": "String",
	"created_by": "String",
	"start_date": Int,
	"end_date": Int,
	"medicines": [
		{
			"medicine_id": "String",
			"comment": "String",
			"period": [
				{
					"quantity": Int,
					"frequency": Int,
					"frequency_ratio": Int,
					"frequency_unit": "ENUM",
					"period_length": Int,
					"period_unit": "ENUM"
				}
			]
		}
	]
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
		"id": "String",
		"created_by": "String",
		"start_date": Int,
		"end_date": Int,
		"medicines": [
			{
				"medicine_id": "String",
				"comment": "String",
				"period": [
					{
						"quantity": Int,
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "ENUM",
						"period_length": Int,
						"period_unit": "ENUM"
					}
				]
			}
		]
	}
]
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:orange;">`PUT`</mark> `/dashboard/treatment/{id} => ID du medical Antecedent`

{% tabs %}
{% tab title="Body" %}
```json
{
	"id": "String", => ID du treatment
	"created_by": "String",
	"start_date": Int,
	"end_date": Int,
	"medicines": [
		{
			"medicine_id": "String",
			"comment": "String",
			"period": [
				{
					"quantity": Int,
					"frequency": Int,
					"frequency_ratio": Int,
					"frequency_unit": "ENUM",
					"period_length": Int,
					"period_unit": "ENUM"
				}
			]
		}
	]
}
```
{% endtab %}

{% tab title="Return 200 " %}
```json
[
	{
		"id": "String",
		"created_by": "String",
		"start_date": Int,
		"end_date": Int,
		"medicines": [
			{
				"medicine_id": "String",
				"comment": "String",
				"period": [
					{
						"quantity": Int,
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "ENUM",
						"period_length": Int,
						"period_unit": "ENUM"
					}
				]
			}
		]
	}
]
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
