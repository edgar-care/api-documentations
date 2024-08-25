# 📃 Medical Folder

The "onboarding" route is a streamlined process designed to gather essential user information swiftly. This route serves as a welcome step, collecting necessary details to personalize the user experience and enhance their engagement with the platform.





<mark style="color:green;">`POST`</mark> `/dashboard/medical-info`&#x20;

#### Request Body

{% tabs %}
{% tab title="Body" %}
```json
{
  "Name": "String",
  "Firstname": "String",
  "Birthdate": Int,
  "Sex": "ENUM",
  "Weight": Int,
  "Height": Int,
  "Primary_doctor_id": "String",
  "family_members_med_info_id": []String,
  "Medical_antecedents": [
    {
      "Name": "String",
      "treatments": [
        {
          "Period": ["ENUM"],
          "Day": ["ENUM"],
          "Quantity": int,
          "Medicine_id": "String"
	  "start_date": Int,
          "end_date": Int,
        },
      ],
      "Still_relevant": Boolean
    }
  ]
}
```
{% endtab %}

{% tab title="Body with no medical antecedent" %}
```json
{
  "Name": "String",
  "Firstname": "String",
  "Birthdate": Int,
  "Sex": "ENUM",
  "Weight": Int,
  "Height": Int,
  "Primary_doctor_id": "String",
  "Medical_antecedents": []
}
```
{% endtab %}

{% tab title="Return 201" %}
```json
{
	"Medical-info": {
		"antecedent_diseases": {
			"antediseases": [
				{
					"AnteDisease": {
						"id": "String",
						"name": "String",
						"chronicity": Int,
						"surgery_ids": [
							"String"
						],
						"symptoms": [
							"String",
						],
						"treatment_ids": [
							"String",
						],
						"still_relevant": Boolean
					},
					"Treatments": [
						{
							"id": "String",
							"period": [
								"ENUM"
							],
							"day": [
								"ENUMDAY"
							],
							"quantity": Int,
							"medicine_id": "String"
							"start_date": Int,
          						"end_date": Int,
						},
					]
				},
			]
		},
		"birthdate": Int,
		"firstname": "String",
		"height": Int,
		"id": "String",
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "ENUM",
		"weight": Int
	}
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/dashboard/medical-info`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
{
	"Medical-info": {
		"antecedent_diseases": {
			"antediseases": [
				{
					"AnteDisease": {
						"id": "String",
						"name": "String",
						"chronicity": Int,
						"surgery_ids": [
							"String"
						],
						"symptoms": [
							"String",
						],
						"treatment_ids": [
							"String",
						],
						"still_relevant": Boolean
					},
					"Treatments": [
						{
							"id": "String",
							"period": [
								"ENUM"
							],
							"day": [
								"ENUMDAY"
							],
							"quantity": Int,
							"medicine_id": "String"
							"start_date": Int,
          						"end_date": Int,
						},
					]
				},
			]
		},
		"birthdate": Int,
		"firstname": "String",
		"height": Int,
		"id": "String",
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "ENUM",
		"weight": Int
	}
}
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:orange;">`PUT`</mark> `/dashboard/medical-info`

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
	"medical_antecedents": [
		{
			"antedisease_id": "string",
			"name": "string",
			"treatments": [
				{
					"treatment_id": "string",
					"name": "string",
					"period": ["ENUM"],
					"day": ["ENUM"],
					"quantity": int
					"start_date": Int,
          				"end_date": Int,
				}
			],
			"still_relevant": boolean
		}
	],
	"onboarding_status": "DONE"
}

```
{% endtab %}

{% tab title="Return 200" %}
```json
{
	"Medical-info": {
		"antecedent_diseases": {
			"antediseases": [
				{
					"AnteDisease": {
						"id": "String",
						"name": "String",
						"chronicity": Int,
						"surgery_ids": [
							"String"
						],
						"symptoms": [
							"String",
						],
						"treatment_ids": [
							"String",
						],
						"still_relevant": Boolean
					},
					"Treatments": [
						{
							"id": "String",
							"period": [
								"ENUM"
							],
							"day": [
								"ENUMDAY"
							],
							"quantity": Int,
							"medicine_id": "String"
						  	"start_date": Int,
          						"end_date": Int,
						},
					]
				},
			]
		},
		"birthdate": Int,
		"firstname": "String",
		"height": Int,
		"id": "String",
		"name": "String",
		"onboarding_status": "DONE",
		"primary_doctor_id": "String",
		"sex": "ENUM",
		"weight": Int
	}
}
```
{% endtab %}
{% endtabs %}
