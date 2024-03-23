# 📅 Slot

<mark style="color:green;">`POST`</mark> `/doctor/slot`

{% tabs %}
{% tab title="Body" %}
```json
{
	"start_date": Timestamp,
	"end_date": Timestamp
}
```
{% endtab %}

{% tab title="Return 201: OK " %}
```json
{
	"rdv": {
		"id": "String",
		"doctor_id": "String",
		"id_patient": "",
		"start_date": Timestamp,
		"end_date": Timestamp,
		"cancelation_reason": "",
		"appointment_status": "OPENED",
		"session_id": "String"
	}
}
```
{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/doctor/slot/{id}`

{% tabs %}
{% tab title="Return 200: OK " %}
```json
{
	"slot": {
		"id": "String",
		"doctor_id": "String",
		"id_patient": "String",
		"start_date": Timestamp,
		"end_date": Timestamp,
		"appointment_status": "ENUM",
		"session_id": "String"
	}
}
```
{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/doctor/slots`

{% tabs %}
{% tab title="Return 200: OK " %}
```json
{
	"slot": [
		{
			"id": "String",
			"doctor_id": "String",
			"id_patient": "String",
			"start_date": Timestamp,
			"end_date": 7890,
			"cancelation_reason": "String",
			"appointment_status": "ENUM",
			"session_id": ""
		}
	]
}
```
{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:red;">`DELETE`</mark> `/doctor/slot/{id}`

{% tabs %}
{% tab title="Return 200: OK " %}
```json
{
	"deleted": true,
	"message": "Slot deleted successfully"
}
```
{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

