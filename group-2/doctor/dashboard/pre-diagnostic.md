# ✔️ Pre-Diagnostic

<mark style="color:green;">`POST`</mark> `/doctor/diagnostic/{id}`

Validation ou non du pre diagnostic du patient depuis le docteur

{% tabs %}
{% tab title="Body" %}
```json
{
	"reason": "String",
	"validation": Boolean
	"health_methode": "String"
}
```
{% endtab %}

{% tab title="Return 200" %}
```json
{
	"review": {
		"id": "String",
		"doctor_id": "String",
		"id_patient": "String",
		"start_date": Timestamp,
		"end_date": Timestamp,
		"cancelation_reason": "REASON String",
		"appointment_status": "ENUM", 
// ENUM : CANCELED_DUE_TO_REVIEW OR ACCEPTED_DUE_TO_REVIEW //
		"session_id": "String"
		"health_method": "String"
	}
}
```
{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark>`/doctor/diagnostic/waiting`

Récuperation de tous les diagnostic en attende de validation ou non

{% tabs %}
{% tab title="Body" %}
no body
{% endtab %}

{% tab title="Return 200" %}
```json
{
	"review": [
		{
			"id": "String",
			"doctor_id": "String",
			"id_patient": "String",
			"start_date": Timestamp,
			"end_date": Timestamp,
			"cancelation_reason": "String",
			"appointment_status": "WAITING_FOR_REVIEW",
			"session_id": "String"
			"diseases": null,
			"fiability": 0.42,
			"symptoms": [
			{
				"name": "String",
				"presence": Boolean,
				"duration": int
			},
			],
			"logs":[
			{
				"question": "describe symptoms",
				"answer": "gorge et éternuements et fatigue"
			}
			],
			"alerts":[
			{
				"id": "String",
				"name": "string",
				"sex": "string",
				"height": int,
				"weight": int,
				"symptoms": [
					"string"
				],
				"comment": "string"
			}
		]
		}
	]
}
```
{% endtab %}
{% endtabs %}
