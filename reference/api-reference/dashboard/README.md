# 🎛️ Dashboard

<mark style="color:blue;">`GET`</mark> `/doctor/patient/{id}`

{% tabs %}
{% tab title="200: OK " %}
```json
{
	"document_ids": null,
	"email": String,
	"id": String,
	"medical_folder": {
		"birthdate": Int,
		"firstname": String,
		"height": Int,
		"id": String,
		"medical_antecedents": [
			{
				"id": String,
				"medicines": [
					{
						"day": [
							ENUM
						],
						"id": String,
						"medicine_id": String,
						"period": [
							ENUM
						],
						"quantity": Int
					},
					{
						"day": [
							ENUM
						],
						"id": String,
						"medicine_id": String,
						"period": [
							ENUM
						],
						"quantity": Int
					}
				],
				"name": String,
				"still_relevant": Boolean
			},
			{
				"id": String,
				"medicines": [
					{
						"day": [
							ENUM						"SUNDAY"
						],
						"id": String,
						"medicine_id": String,
						"period": [
							ENUM							"NOON"
						],
						"quantity": Int
					}
				],
				"name": String,
				"still_relevant": Boolean
			}
		],
		"name": String,
		"onboarding_status": String,
		"primary_doctor_id": String,
		"sex": String,
		"weight": Int
	},
	"rendez_vous_ids": null,
	"treatment_follow_up_ids": null
}
```
{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/doctor/patients`

{% tabs %}
{% tab title="200: OK " %}
```json
{
	"patients": [
		{
			"document_ids": null,
			"email": String,
			"id": String,
			"medical_folder": {
				"birthdate": Int,
				"firstname": String,
				"height": Int,
				"id": String,
				"medical_antecedents": [
					{
						"id": String,
						"medicines": [
							{
								"day": [
									ENUM
								],
								"id": String,
								"medicine_id": String,
								"period": [
									ENUM
								],
								"quantity": Int
							},
							{
								"day": [
									ENUM
								],
								"id": String,
								"medicine_id": String,
								"period": [
									ENUM
								],
								"quantity": Int
							}
						],
						"name": String,
						"still_relevant": Boolean
					},
				],
				"name": String,
				"onboarding_status": String,
				"primary_doctor_id": String,
				"sex": String,
				"weight": Int
			},
			"rendez_vous_ids": null,
			"treatment_follow_up_ids": null
		},
		{
			"document_ids": null,
			"email": String,
			"id": String,
			"medical_folder": {
				"birthdate": Int,
				"firstname": String,
				"height": Int,
				"id": String,
				"medical_antecedents": [
					{
						"id": String,
						"medicines": [
							{
								"day": [
									ENUM
								],
								"id": String,
								"medicine_id": String,
								"period": [
									ENUM
								],
								"quantity": Int
							},
							{
								"day": [
									ENUM
								],
								"id": String,
								"medicine_id": String,
								"period": [
									ENUM
								],
								"quantity": Int
							}
						],
						"name": String,
						"still_relevant": Boolean
					},
				],
				"name": String,
				"onboarding_status": String,
				"primary_doctor_id": String,
				"sex": String,
				"weight": Int
			},
			"rendez_vous_ids": null,
			"treatment_follow_up_ids": null
		},
	]
}
```
{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:orange;">`PUT`</mark> `/doctor/patient/{id}`

#### Request Body

| Name                      | Type      | Description |
| ------------------------- | --------- | ----------- |
| onboarding\_info          | {}        |             |
| name                      | String    |             |
| surname                   | String    |             |
| birthdate                 | String    |             |
| sex                       | String    |             |
| weight                    | String    |             |
| height                    | String    |             |
| onboarding\_health        | {}        |             |
| patients\_allergies       | \[String] |             |
| patients\_illness         | \[String] |             |
| patients\_treatments      | \[String] |             |
| patients\_primary\_doctor | String    |             |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:green;">`POST`</mark> `/doctor/patient`

#### Request Body

| Name                                    | Type      | Description |
| --------------------------------------- | --------- | ----------- |
| onboarding\_info                        | {}        |             |
| name                                    | String    |             |
| surname                                 | String    |             |
| birthdate                               | String    |             |
| sex                                     | String    |             |
| weight                                  | String    |             |
| height                                  | String    |             |
| onboarding\_health                      | {}        |             |
| patients\_allergies                     | \[String] |             |
| patients\_illness                       | \[String] |             |
| patients\_treatments                    | \[String] |             |
| patients\_primary\_doctor               | String    |             |
| patient\_input                          | {}        |             |
| email<mark style="color:red;">\*</mark> | String    |             |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/doctor/patient/{id}`

Suppression Patient Account.

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}
