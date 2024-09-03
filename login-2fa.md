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



| Route Login 2fa                                                                                          |
| -------------------------------------------------------------------------------------------------------- |
| <p><mark style="color:green;"><code>POST</code></mark> </p><pre><code>/auth/email_2fa
</code></pre>      |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/auth/backup_code_2fa
</code></pre> |
| <p><mark style="color:green;"><code>POST</code></mark></p><pre><code>/auth/third_party_2fa
</code></pre> |

{% tabs %}
{% tab title="Body 2fa email" %}
```
{
	"email": "String",
	"password": "String",
	"token_2fa": "String"
}
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

Login 2FA Mobile (websocket)

{% tabs %}
{% tab title="Body Web" %}
```
{
    "action": "ready",
    "authToken": "{{patientAuthTokenWS}}"
}
```
{% endtab %}

{% tab title="Body Mobile Ask" %}
```
{
    "action": "askMobileConnection",
    "uuid": "67f128d9-bc94-4de0-a32a-5f083a646d49",
    "type": "patient",
    "email": "test+lucasws@gmail.com",
    "password": "testtest"
}
```
{% endtab %}

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
{% endtabs %}
