# 🎛️ Dashboard

<mark style="color:blue;">`GET`</mark> `/doctor/patient/{id}`

{% tabs %}
{% tab title="200: OK " %}
{% tabs %}
{% tab title="example" %}
```json
{
	"onboarding_health": {
		"id": "string",
		"patients_allergies": ["string", "string"],
		"patients_illness": ["string"],
		"patients_treatments": ["string"],
		"patients_primary_doctor": "string"
	},
	"onboarding_info": {
		"id": "string",
		"name": "string",
		"surname": "string",
		"birthdate": "string",
		"sex": "MALE",
		"weight": int,
		"height": int
	},
	"patient": {
		"id": "string",
		"onboarding_info_id": "string",
		"onboarding_health_id": "string",
		"email": "string"
	}
}
```
{% endtab %}
{% endtabs %}
{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/doctor/patients`

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:orange;">`PUT`</mark> `/doctor/patient/{id}`

#### Request Body

| Name                      | Type      | Description |
| ------------------------- | --------- | ----------- |
| onboarding\_info          | {}        |             |
| name                      | String    |             |
| surname                   | String    |             |
| birthdate                 | String    |             |
| sex                       | String    |             |
| weight                    | String    |             |
| height                    | String    |             |
| onboarding\_health        | {}        |             |
| patients\_allergies       | \[String] |             |
| patients\_illness         | \[String] |             |
| patients\_treatments      | \[String] |             |
| patients\_primary\_doctor | String    |             |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:green;">`POST`</mark> `/doctor/patient`

#### Request Body

| Name                                    | Type      | Description |
| --------------------------------------- | --------- | ----------- |
| onboarding\_info                        | {}        |             |
| name                                    | String    |             |
| surname                                 | String    |             |
| birthdate                               | String    |             |
| sex                                     | String    |             |
| weight                                  | String    |             |
| height                                  | String    |             |
| onboarding\_health                      | {}        |             |
| patients\_allergies                     | \[String] |             |
| patients\_illness                       | \[String] |             |
| patients\_treatments                    | \[String] |             |
| patients\_primary\_doctor               | String    |             |
| patient\_input                          | {}        |             |
| email<mark style="color:red;">\*</mark> | String    |             |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/doctor/patient/{id}`

Suppression Patient Account.

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}
