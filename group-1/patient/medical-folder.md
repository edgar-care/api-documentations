# 📃 Medical Folder

The "onboarding" route is a streamlined process designed to gather essential user information swiftly. This route serves as a welcome step, collecting necessary details to personalize the user experience and enhance their engagement with the platform.



| ENUM    |
| ------- |
| JOUR    |
| SEMAINE |
| MOIS    |
| ANNEE   |





<mark style="color:green;">`POST`</mark> `/dashboard/medical-info`&#x20;

#### Request Body

{% tabs %}
{% tab title="Body" %}
```json
{
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
          "start_date": Int,
          "end_date": Int4567899,
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
  "family_members_med_info_id": ["String"]
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
  "family_members_med_info_id": ["String"],
  "Medical_antecedents": []
}
```
{% endtab %}

{% tab title="Return 201" %}
```json
{
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
	"medical_folder": {
		"birthdate": Int,
		"family_members_med_info_id": [
			""
		],
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
			},
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
}

```
{% endtab %}

{% tab title="Return 200" %}
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
