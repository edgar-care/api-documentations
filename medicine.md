# 💊 Medicine

<mark style="color:green;">`POST`</mark> `/medicine`

{% tabs %}
{% tab title="Body" %}
```json
{
		"dci":             "String",
		"name":             "String",
		"target_diseases": ["String"],
		"treated_symptoms": ["String"],
		"side_effects":     ["String"],
	        "dosage": Int, 
	        "dosage_unit": "UnitEnum",
	        "container": "ContainerEnum",
		"dosage_form": "FormEnum"
}
```
{% endtab %}

{% tab title="UnitEnum" %}
```
	"ml"
	"mg"
	"g"
```
{% endtab %}

{% tab title="ContainerEnum" %}
```
	"FLACON"
	"TUBE"
	"BOITE"
```
{% endtab %}

{% tab title="FormEnum" %}
```
	"CREME"
	"POMMADE"
	"GELULE"
	"COMPRIME"
	"GELE"
	"SOLUTION_BUVABLE"
	"POUDRE"
	"SUPPOSITOIRE"
	"AMPOULE"
	"SUSPENSION_NASALE"
	"SPRAY"
	"COLLUTOIRE"
	"SHAMPOOING"
	"SOLUTION_INJECTABLE"
	"COMPRIMER_EFERVESCENT"
	"GRANULER_EN_SACHET"
	"PASTILLE"
	"SIROP"
```
{% endtab %}

{% tab title="Return 201" %}
```json
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/medicine`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/medicine/{id}`

{% tabs %}
{% tab title="No body" %}

{% endtab %}

{% tab title="Return 200" %}
```json
```
{% endtab %}
{% endtabs %}
