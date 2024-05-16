# 👨‍⚕️ Get information about doctor

<mark style="color:blue;">`GET`</mark>` ``/doctors`

Récupération de tous les docteur présent dans la base de donnée d'edgar

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

Récupération d'un seul docteur

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
