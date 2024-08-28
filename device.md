# 💻 Device

<mark style="color:blue;">`GET`</mark>` ``/dashboard/device/{id}`\
Récupération appareil connecté

{% tabs %}
{% tab title="Body Return" %}
```
{
	"devices": {
		"id": "Srting",
		"device_type": "Srting",
		"browser": "String",
		"ip_address": "Srting",
		"latitude": float,
		"longitude": float,
		"date": int,
		"trust_device": boolean
	}
}
```
{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark>` ``/dashboard/devices`\
Récupération de tous les appareils connectés

{% tabs %}
{% tab title="Body Return" %}
```
{
	"devices": [
		{
			"id": "Srting",
			"device_type": "Srting",
			"browser": "String",
			"ip_address": "Srting",
			"latitude": float,
			"longitude": float,
			"date": 1719217730,
			"trust_device": true
		},
		{
			"id": "Srting",
			"device_type": "Srting",
			"browser": "String",
			"ip_address": "Srting",
			"latitude": float,
			"longitude": float,
			"date": 1719217730,
			"trust_device": true
		}
	]
}
```
{% endtab %}
{% endtabs %}
