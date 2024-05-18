# 📋 Dashboard



ENUM

| DAY       | PERIOD  |
| --------- | ------- |
| MONDAY    | MORNING |
| TUESDAY   | NOON    |
| WEDNESDAY | EVENING |
| THURSDAY  | NIGHT   |
| FRIDAY    |         |
| SATURDAY  |         |
| SUNDAY    |         |



Recuperer un patient assiocier au dit docteur

<mark style="color:blue;">`GET`</mark> `/doctor/patient/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Body return" %}
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
{% endtabs %}



Modifier les informations du patient

<mark style="color:orange;">`PUT`</mark> `/doctor/patient/{id}`&#x20;

{% tabs %}
{% tab title="Body" %}
```json
{
	"name": "pierre",
	"firstname": "paul",
	"birthdate": 2874,
	"sex": "MALE",
	"weight": 56,
	"height": 12,
	"primary_doctor_id": "363636",
	"medical_antecedents": [
		{
			"name": "Parasetamole",
			"medicines": [ 	# ceci est le treatment
				{
					"period": ["MORNING"],
					"day": ["MONDAY"],
					"quantity": 2
				}
			],
			"still_relevant": true
		}
	],
	"onboarding_status": "DONE"
}
```
{% endtab %}

{% tab title="Body return" %}
```json
{
	"MedicalFolder": {
		"id": "65ef682a99bdff9429cf9884",
		"name": "pierre",
		"firstname": "paul",
		"birthdate": 2874,
		"sex": "MALE",
		"height": 12,
		"weight": 56,
		"primary_doctor_id": "363636",
		"onboarding_status": "DONE",
		"medical_antecedents": [
			{
				"id": "",
				"name": "Parasetamole",
				"medicines": [
					{
						"period": [
							"MORNING"
						],
						"day": [
							"MONDAY"
						],
						"quantity": 2
					}
				],
				"still_relevant": true
			}
		]
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
	"email": "testreturn@gmail.com",
	"medical_info": {
		"Name": "MADAME",
		"Firstname": "jean",
		"Birthdate": 12,
		"Sex": "FEMALE",
		"Weight": 1223,
		"Height": 122,
		"Primary_doctor_id": "Pierre",
		"medical_antecedents": [
			{
				"Name": "mal de Tete",
				"treatments": [
					{
						"period": ["MORNING"],
						"day": ["MONDAY"],
						"quantity": 10,
						"medicine_id": "test"
					},
					{
						"Period": ["NOON"],
						"Day": ["SUNDAY"],
						"Quantity": 10,
						"medicine_id": "test second"
					}
				],
				"still_relevant": true
			},
			{
				"Name": "Test second Medicine",
				"treatments": [
					{
						"Period": ["MORNING", "NOON"],
						"Day": ["MONDAY", "SUNDAY"],
						"Quantity": 10,
						"medicine_id": "test2"
					}
				],
				"Still_relevant": true
			}
		]
	}
}
```
{% endtab %}

{% tab title="Body return" %}
```json
{
	"medical_folder": {
		"birthdate": 12,
		"firstname": "jean",
		"height": 122,
		"id": "66295207e4669ff03d925263",
		"medical_antecedents": [
			{
				"id": "66295206e4669ff03d925260",
				"medicines": [
					{
						"day": [
							"MONDAY"
						],
						"id": "66295206e4669ff03d92525e",
						"medicine_id": "test",
						"period": [
							"MORNING"
						],
						"quantity": 10
					},
					{
						"day": [
							"SUNDAY"
						],
						"id": "66295206e4669ff03d92525f",
						"medicine_id": "test second",
						"period": [
							"NOON"
						],
						"quantity": 10
					}
				],
				"name": "mal de Tete",
				"stillRelevant": true
			},
			{
				"id": "66295206e4669ff03d925262",
				"medicines": [
					{
						"day": [
							"MONDAY",
							"SUNDAY"
						],
						"id": "66295206e4669ff03d925261",
						"medicine_id": "test2",
						"period": [
							"MORNING",
							"NOON"
						],
						"quantity": 10
					}
				],
				"name": "Test second Medicine",
				"stillRelevant": true
			}
		],
		"name": "MADAME",
		"onboarding_status": "DONE",
		"primary_doctor_id": "Pierre",
		"sex": "FEMALE",
		"weight": 1223
	},
	"patient": "testreturn@gmail.com",
	"patient_id": "66295205e4669ff03d92525d"
}
```
{% endtab %}
{% endtabs %}



Suppression Patient Account.

<mark style="color:red;">`DELETE`</mark> `/doctor/patient/{id}`

