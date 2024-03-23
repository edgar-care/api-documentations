# 👨‍⚕️ Get information about doctor

<mark style="color:blue;">`GET`</mark>` ``/doctors`

{% tabs %}
{% tab title="Body" %}
No Body
{% endtab %}

{% tab title="Return" %}
```json
{
	"Doctors": [
		{
			"id": "String",
			"email": "String",
			"name": "String",
			"firstname": "String",
			"address": {
				"street": "String",
				"zip_code": "String",
				"country": "String",
				"city": "String"
			}
		}
	]
}
```
{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark>` ``/doctor/{id}`

{% tabs %}
{% tab title="Body" %}
No body
{% endtab %}

{% tab title="Return" %}
```json
{
	"Doctors": {
		"id": "String",
		"email": "Stringm",
		"name": "String",
		"firstname": "String",
		"address": {
			"street": "String",
			"zip_code": "String",
			"country": "String",
			"city": "String"
		}
	}
}
```
{% endtab %}
{% endtabs %}
