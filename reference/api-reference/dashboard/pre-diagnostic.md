# ✔️ Pre-Diagnostic

<mark style="color:green;">`POST`</mark> `/doctor/diagnostic/{id}`

{% tabs %}
{% tab title="Body" %}
```json
{
	"reason": "String",
	"validation": Boolean
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
	}
}
```
{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark>` ``/doctor/diagnostic/waiting`

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
		}
	]
}
```
{% endtab %}
{% endtabs %}
