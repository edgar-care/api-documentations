# 📋 Dashboard "! Maintenance !"



Recuperer un patient assiocier au dit docteur

<mark style="color:blue;">`GET`</mark> `/doctor/patient/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Body return" %}
```json
{
	"id": "String",
	"medical_folder": {
		"birthdate": Int,
		"family_members_med_info_id": ["String"],
		"firstname": "String",
		"height": Int,
		"id": "String",
		"medical_antecedents": [
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
		],
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "String",
		"weight": Int
	},
	"patient": "String"
}
```
{% endtab %}
{% endtabs %}



Récuprer tous les patients associer au dit docteur

<mark style="color:blue;">`GET`</mark> `/doctor/patients`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Body return" %}
```json
{
	"patients": [
		{
			"id": "String",
			"medical_folder": {
				"birthdate": Int,
				"family_members_med_info_id": ["String"],
				"firstname": "String",
				"height": Int,
				"id": "String",
				"medical_antecedents": [
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
				],
				"name": "String",
				"onboarding_status": "DONE",
				"primary_doctor_id": "String",
				"sex": "String",
				"weight": Int
			},
			"patient": "String"
		}
	]
}
```
{% endtab %}
{% endtabs %}



Modifier les informations du patient

<mark style="color:orange;">`PUT`</mark> `/doctor/patient/{id}`&#x20;

Attention, si la maladie ou le traitement n'est pas renseignée, elle sera supprimée en base de donnée

{% tabs %}
{% tab title="Body" %}
```json
{
	"name": "string",
	"firstname": "string",
	"birthdate": int,
	"sex": "String",
	"weight": int,
	"height": int,
	"primary_doctor_id": "string",
	"family_members_med_info_id": []"string"
}
```
{% endtab %}

{% tab title="Body return" %}
```json
{
	"medical_folder": {
		"birthdate": Int,
		"family_members_med_info_id": ["String"],
		"firstname": "String",
		"height": Int,
		"id": "String",
		"medical_antecedents": [
			"String",
		],
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "String",
		"weight": Int
	}
}
```
{% endtab %}
{% endtabs %}



Creation d'un nouveau patient depuis un docteur

<mark style="color:green;">`POST`</mark> `/doctor/patient`

Si le patient existe deja, cela edit juste le patient

{% tabs %}
{% tab title="Body" %}
```json
{
    "email": "String",
    "medical_info": {
        "name": "String",
        "firstname": "String",
        "birthdate": Int,
        "sex": "String",
        "weight": Int,
        "height": Int,
        "primary_doctor_id": "String",
          "medical_antecedents": [
						{
							"name": "String",
							"symptoms": ["String"],
							"treatments": [
								{
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
						}
					],
        "onboarding_status": "DONE",
	"family_members_med_info_id": ["String"]
    }
}
```
{% endtab %}

{% tab title="Body return" %}
```json
{
	"id": "String",
	"medical_folder": {
		"birthdate": Int,
		"family_members_med_info_id": ["String"],
		"firstname": "String",
		"height": Int,
		"id": "String",
		"medical_antecedents": [
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
		],
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "String",
		"weight": Int
	},
	"patient": "String"
}
```
{% endtab %}
{% endtabs %}



Suppression Patient Account.

<mark style="color:red;">`DELETE`</mark> `/doctor/patient/{id}`

