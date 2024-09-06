# Ordonnance

<mark style="color:green;">`POST`</mark>&#x20;

```
/dashboard/prescription
```

{% tabs %}
{% tab title="Body" %}
```
{
  "patient_id": "", # ID Patient
  "medicines": [
    {
      "medicine_id": "", # ID medicament
      "qsp": Int,
      "qsp_unit": "UnitEnum",
      "comment": "String",
      "periods": [
        {
          "quantity": Int,
          "frequency": Int,
          "frequency_ratio": Int,
          "frequency_unit": "TimeUnitEnum",
          "period_length": Int,
          "period_unit": "TimeUnitEnum"
        },
        {
          "quantity": Int,
          "frequency": Int,
          "frequency_ratio": Int,
          "frequency_unit": "TimeUnitEnum",
          "period_length": Int,
          "period_unit": "TimeUnitEnum"
        }
      ]
    },
    {
      "medicine_id": "", # Id medicament
      "qsp": Int,
      "qsp_unit": "UnitEnum",
      "comment": "String",
      "periods": [
        {
          "quantity": Int,
          "frequency": Int,
          "frequency_ratio": Int
          "frequency_unit": "TimeUnitEnum",
          "period_length": Int,
          "period_unit": "TimeUnitEnum"
        }
      ]
    }
  ]
}
```
{% endtab %}

{% tab title="TimeUnitEnum " %}
```
        JOUR
        SEMAINE
        MOIS
        ANNEE
```
{% endtab %}

{% tab title="UnitEnum" %}
```
        ml
        mg
        g
```
{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark>

```
/dashboard/prescription/{id}
```

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark>

```
/dashboard/prescriptions
```

{% tabs %}
{% tab title="First Tab" %}

{% endtab %}

{% tab title="Second Tab" %}

{% endtab %}
{% endtabs %}
