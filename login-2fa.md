# Login 2fa





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
	"token_2fa": "String" 	#NOTE IMPORTANT mettre \n a la fin du code
}
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}
