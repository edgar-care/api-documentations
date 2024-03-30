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
  "PrimaryDoctorID": "String",
  "MedicalAntecedents": [
    {
      "Name": "String",
      "Medicines": [
        {
          "Period": ["ENUM"],
          "Day": ["ENUM"],
          "Quantity": int,
          "MedicineID": "String"
        },
      ],
      "StillRelevant": Boolean
    }
  ]
}
```
{% endtab %}

{% tab title="Return 201" %}
```json
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
// Some code
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
      "medicines": [
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
	"medifcal_folder": {
		"id": "String",
		"name": "String",
		"firstname": "String",
		"birthdate": Int,
		"sex": "ENUM",
		"height": Int,
		"weight": Int,
		"primary_doctor_id": "test",
		"onboarding_status": "DONE",
		"medical_antecedents": [
			{
				"id": "String",
				"name": "String",
				"medicines": [
					{
						"period": [
							"ENUM",
						],
						"day": [
							"ENUM"
						],
						"quantity": Int
					}
				],
				"still_relevant": Boolean
			}
		]
	}
}
```
{% endtab %}
{% endtabs %}
