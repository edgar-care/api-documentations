# 🔐 Login 2fa





Envoie email pour login 2fa email

<mark style="color:green;">`POST`</mark>` ``/auth/sending_emai`l

{% tabs %}
{% tab title="Body" %}
```
{
    "email": "string"
}
```
{% endtab %}
{% endtabs %}

| type |         |
| ---- | ------- |
| p    | patient |
| d    | doctor  |
| a    | admin   |



| Route Login 2fa                                                                                                 |
| --------------------------------------------------------------------------------------------------------------- |
| <p><mark style="color:green;"><code>POST</code></mark> </p><pre><code>/auth/{type}/email_2fa
</code></pre>      |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/auth/{type}/backup_code_2fa
</code></pre> |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/auth/{type}/third_party_2fa
</code></pre> |

{% tabs %}
{% tab title="Body 2fa " %}
```
{
	"email": "String",
	"password": "String",
	"token_2fa": "String"
}
```
{% endtab %}

{% tab title="Body login Backupcode" %}
```
{
	"email": "String",
	"password": "String",
	"backup_code": "String" #Non hasher
}
```
{% endtab %}
{% endtabs %}

Login 2FA Mobile (websocket)

{% tabs %}
{% tab title="Body Web" %}
```
{
    "action": "readyLogin",
    "os": "string",
    "browser": "string",
    "location": "string"
}
```
{% endtab %}

{% tab title="Return Web" %}
```
{
    "message": "Connection ready",
    "uuid": "String"
}
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Body Mobile Ask" %}
```
{
    "action": "askMobileConnection",
    "uuid": "String",
    "type": "type",    #type : p = Patient / d = Doctor
    "email": "string",
    "password": "string"
}
```
{% endtab %}

{% tab title="Return Web Ask" %}
```
{
    "message": "String"
}
```
{% endtab %}

{% tab title="Return Mobile Ask" %}
```
{
    "action": "ask_mobile_connection",
    "browser": "String",
    "location": "String",
    "os": "String",
    "uuid": "String"
}
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Body Mobile response" %}
```
{
    "action": "responseMobileConnection",
    "authToken": "{{patientAuthTokenWS}}",
    "uuid": "",
    "response": true
}
```
{% endtab %}

{% tab title="Return Mobile" %}
```
{
	"message": "Message sent"
}
```
{% endtab %}

{% tab title="Return Web" %}
```
{		
    "action":   "response_mobile_connection",
    "code":     "String",
    "response": Boolean,
}
```
{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="Body Login Mobile" %}
```
{
    "email": "String",
    "password": "String",
    "token_2fa": "String"
}
```
{% endtab %}

{% tab title="Return Login" %}
```
{
    "token": "String"
}
```
{% endtab %}
{% endtabs %}
