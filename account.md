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
/auth/{type}/missing-password
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
/auth/{type}/reset-password
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





<mark style="color:green;">`POST`</mark>` ``/auth/delete_account`

Email envoyer confirmant l'action

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return" %}
```
{
	"message": "Account deletion scheduled"
}
```
{% endtab %}
{% endtabs %}



<mark style="color:green;">`POST`</mark>` ``/auth/update_password`

Update password

{% tabs %}
{% tab title="First Tab" %}
```
{
    "old_password": "String",
    "new_password": "String"
}
```


{% endtab %}

{% tab title="Second Tab" %}
```
{
    		"password": "updated",
}
```
{% endtab %}
{% endtabs %}

