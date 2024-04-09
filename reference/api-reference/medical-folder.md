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
  "Medical_antecedents": [
    {
      "Name": "String",
      "treatments": [
        {
          "Period": ["ENUM"],
          "Day": ["ENUM"],
          "Quantity": int,
          "Medicine_id": "String"
        },
      ],
      "Still_relevant": Boolean
    }
  ]
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
  "name": "String",
  "firstname": "String",
  "birthdate": Int,
  "sex": "ENUM",
  "weight": Int,
  "height": Int,
  "primary_doctor_id": "String",
  "medical_antecedents": [
    {
      "name": "String",
      "treatments": [
        {
          "period": ["ENUM"],
          "day": ["ENUM"],
          "quantity": Int
        }
      ],
      "still_relevant": Boolean
    }
  ],
  "onboarding_status": "String"

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
