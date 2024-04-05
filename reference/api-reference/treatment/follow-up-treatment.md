# 🗃️ Follow up treatment

<mark style="color:green;">`POST`</mark> `/dashboard/treatment/follow-up`

{% tabs %}
{% tab title="Body" %}
```json
{
	"treatment_id": String,
	"date": int,
	"period": ["ENUM"]
}
```
{% endtab %}

{% tab title="Return 201" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/dashboard/treatment/follow-up/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/dashboard/treatment/follow-up`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/dashboard/treatment/follow-up/{id}`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}

{% endtab %}
{% endtabs %}
