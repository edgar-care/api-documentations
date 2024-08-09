# Account

<mark style="color:orange;">`PUT`</mark> /`auth/enable_account`&#x20;

Activation du compte

{% tabs %}
{% tab title="Body" %}
```
{
	"enable_account": true
}
```
{% endtab %}

{% tab title="Body Return" %}
```
{
	"account_status": true
}
```
{% endtab %}
{% endtabs %}



<mark style="color:orange;">`PUT`</mark>` ``/auth/disable_account`&#x20;

désactivation du compte

{% tabs %}
{% tab title="Body" %}
```
{
	"enable_account": false
}
```
{% endtab %}

{% tab title="Body Return" %}
```
{
	"account_status": false
}
```
{% endtab %}
{% endtabs %}
