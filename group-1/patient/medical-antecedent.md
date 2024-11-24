# 💊 Medical Antecedent





| ENUM    |
| ------- |
| JOUR    |
| SEMAINE |
| MOIS    |
| ANNEE   |





<mark style="color:green;">`POST`</mark> `/dashboard/medical-antecedent`&#x20;

#### Request Body

{% tabs %}
{% tab title="Body" %}
```
{
	"name": "String",
	"symptoms": ["String"],
	"treatments": [
		{
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
}
```


{% endtab %}

{% tab title="Return" %}
```
[
	{
		"id": "String",
		"name": "String",
		"symptoms": [
			"String"
		],
		"treatments": [
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
		],
		"createdAt": Int,
		"updatedAt": Int
	}
]
```


{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark> `/dashboard/medical-antecedent`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return" %}
```
[
	{
		"id": "String",
		"name": "String",
		"symptoms": [
			"String"
		],
		"treatments": [
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
		],
		"createdAt": Int,
		"updatedAt": Int
	}
]
```


{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark> `/dashboard/medical-antecedent/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return" %}
```
{
	"id": "String",
	"name": "String",
	"symptoms": [
		"String"
	],
	"treatments": [
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
	],
	"createdAt": Int,
	"updatedAt": Int
}
```
{% endtab %}
{% endtabs %}



<mark style="color:orange;">`PUT`</mark> `/dashboard/medical-antecedent/{id}`

{% tabs %}
{% tab title="Body" %}
```
{
	"medical_antecedent": {
			"name": "String",
			"symptoms": ["String"]
	}
}
```


{% endtab %}

{% tab title="Return" %}
```
{
	"id": "String",
	"name": "String",
	"symptoms": [
		"String"
	],
	"treatments": [
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
	],
	"createdAt": Int,
	"updatedAt": Int
}
```


{% endtab %}
{% endtabs %}



<mark style="color:red;">`DELETE`</mark> `/dashboard/medical-antecedent/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return" %}
```
{
	"delete": true
}
```


{% endtab %}
{% endtabs %}

