# ➿ Double Auth

### Méthods Enable

|                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------- |
| <p><mark style="color:green;"><code>POST</code></mark> </p><pre><code>/2fa/method/email
</code></pre>               |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/2fa/method/third_party/generate
</code></pre> |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/2fa/method/mobile
</code></pre>               |



{% tabs %}
{% tab title="ENUM" %}
| ENUM            |
| --------------- |
| MOBILE          |
| AUTHENTIFICATOR |
| EMAIL           |
| BACKUPCODE      |
{% endtab %}

{% tab title="Body EMAIL" %}
```
{
	"method_2fa": "EMAIL",
}
```
{% endtab %}

{% tab title="Body MOBILE" %}
```
{
	"method_2fa": "MOBILE",
	"trusted_device_id": "string"	#id device connect you want to put on Trustdevice
}
```
{% endtab %}

{% tab title="body AUTHENTIFICATOR" %}
```
No Body
```


{% endtab %}
{% endtabs %}



Activate 2fa third party

<mark style="color:green;">`POST`</mark> /2fa/method/third\_party

{% tabs %}
{% tab title="First Tab" %}
```
{
	"token": "String"
}
```
{% endtab %}

{% tab title="Return" %}
```
{
    true
}
```
{% endtab %}
{% endtabs %}



Get 2fa method

<mark style="color:blue;">`GET`</mark>&#x20;

```
/dashboard/2fa
```



{% tabs %}
{% tab title="Body return" %}
```
{
	"double_auth": {
		"id": "string",
		"methods": [
			"ENUM"
		],
		"secret": "string",
		"url": "string",
		"trust_device_id": "string"
	}
}
```
{% endtab %}
{% endtabs %}

\
\
<mark style="color:red;">`DELETE`</mark>&#x20;

```
/dashboard/2fa/{ENUM}
```

{% tabs %}
{% tab title="ENUM" %}


| ENUM            |
| --------------- |
| MOBILE          |
| AUTHENTIFICATOR |
| EMAIL           |
| BACKUPCODE      |
{% endtab %}

{% tab title="Body Return" %}
```
{
	"message": "Double auth deleted successfully"
}
```
{% endtab %}
{% endtabs %}













\===================================================================

### Trust Device



<mark style="color:green;">`POST`</mark> `/dashboard/2fa/device/{id}`\
Ajout appareil de confiance

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Body Return " %}


```
{
	"trusted_device": "string"
}
```
{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark> `/dashboard/2fa/device/{id}`

{% tabs %}
{% tab title="Body Return" %}
```
{
	"double_auth": {
		"id": "Srting",
		"device_type": "Srting",
		"browser": "String",
		"ip_address": "Srting",
		"latitude": float,
		"longitude": float,
		"date": 1719217730,
		"trust_device": true
	}
}
```
{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/dashboard/2fa/devices`

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

\
<mark style="color:red;">`DELETE`</mark>`/dashboard/2fa/device/{id}`

{% tabs %}
{% tab title="Body Retrun" %}
```
{
	"double_auth": {
		"id": "",
		"email": "",
		"password": "",
		"status": false
	}
}
```
{% endtab %}
{% endtabs %}



<mark style="color:green;">`POST`</mark> `/auth/creation_backup_code`

Creation code de sauvegarde

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Body Return" %}
```
{
	"double_auth": {
		"id": "",
		"code": [
			"String",
			"String",
			"String",
			"String",
			"String",
			"String",
			"String",
			"String",
			"String",
			"String"
		]
	}
}
```
{% endtab %}
{% endtabs %}
