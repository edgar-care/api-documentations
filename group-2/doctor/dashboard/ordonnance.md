# 💉 Ordonnance

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
      "comment": "String",                 #=> No comment ""
      "periods": [
        {
          "quantity": Int,
          "frequency": Int,
          "frequency_ratio": Int,
          "frequency_unit": "TimeUnitEnum",
          "period_length": Int,             #=> no period lenght 0
          "period_unit": "TimeUnitEnum"     #=> no period Unit ""
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

{% tab title="Return" %}
```
{
	"prescription": {
		"id": "String",
		"created_by": "String",		# ID Doctor
		"patient_id": "String",		# ID patient
		"medicines": [
			{
				"medicine_id": "String",	# ID Médicament
				"qsp": Int,
				"qsp_unit": "TimeUnitEnum",
				"comment": "String",
				"periods": [
					{
						"quantity": Int,
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "TimeUnitEnum",
						"period_length": Int,
						"period_unit": "TimeUnitEnum"
					}
				]
			}
		],
		"createdAt": Int,	#Timestamp
		"updatedAt": Int	#Timestamp
	},
	"url_prescription": "String URL"
}
```
{% endtab %}
{% endtabs %}



<mark style="color:blue;">`GET`</mark>

```
/dashboard/prescription/{id}
```

{% tabs %}
{% tab title="Return" %}
```
{
	"prescription": {
		"id": "String",
		"created_by": "String", 	# ID Doctor
		"patient_id": "String", 	# ID patient
		"medicines": [
			{
				"medicine_id": "String",	# ID Médicamen
				"qsp": Int,
				"qsp_unit": "TimeUnitEnum",
				"comment": "String
					{
						"quantity": Int;
						"frequency": Int,
						"frequency_ratio": Int,
						"frequency_unit": "TimeUnitEnum",
						"period_length": Int,
						"period_unit": "TimeUnitEnum"
					}
				]
			}
		],
		"createdAt": Int,	#Timestamp
		"updatedAt": Int	#Timestamp
	},
	"url_prescription": "String URL"
}
```
{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark>

```
/dashboard/prescriptions
```

{% tabs %}
{% tab title="Return" %}
```
{
	"prescriptions": [
		{
			"id": "String",
			"created_by": "String", 	# ID Doctor
			"patient_id": "String", 	# ID patient
			"medicines": [
				{
					"medicine_id": "String", 	# ID Medicament
					"qsp": Int,
					"qsp_unit": "TimeUnitEnum",
					"comment": "String",
					"periods": [
						{
							"quantity": Int,
							"frequency": Int,
							"frequency_ratio": Int,
							"frequency_unit": "TimeUnitEnum",
							"period_length": Int,
							"period_unit": "TimeUnitEnum"
						}
					]
				}
			],
			"createdAt": Int,	#Timestamp
			"updatedAt": Int,	#Timestamp
			"URL": "String URL"
		}
	]
}
```
{% endtab %}
{% endtabs %}
