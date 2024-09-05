# 🧑‍🤝‍🧑 Account

<mark style="color:orange;">`PUT`</mark> /`auth/enable_account`&#x20;

Activation du compte

{% tabs %}
{% tab title="NO Body" %}
```
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

désactivation du compt

{% tabs %}
{% tab title="NO Body" %}
```
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



<mark style="color:green;">`POST`</mark>&#x20;

```
/auth/p/missing-password
```

{% tabs %}
{% tab title="Body" %}
```
{
    "email": "String"
}    
```
{% endtab %}
{% endtabs %}



<mark style="color:green;">`POST`</mark>

```
/auth/p/reset-password
```

{% tabs %}
{% tab title="Body" %}
```
{
    "new_password": "String"
}
```
{% endtab %}

{% tab title="Untitled" %}
Query params uuid
{% endtab %}
{% endtabs %}
