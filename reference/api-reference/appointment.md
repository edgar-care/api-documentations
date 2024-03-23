# 🏥 Appointment

### Patient

<mark style="color:green;">`POST`</mark> `/appointments/{id}`&#x20;

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/patient/appointments/{id}`&#x20;

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

## {id} => id Doctor

<mark style="color:blue;">`GET`</mark> `/doctor/{id}/appointments`&#x20;

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/patient/appointments`&#x20;

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/appointments/{id}`&#x20;

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

<mark style="color:orange;">`PUT`</mark> `/appointments/{id}`&#x20;

#### Request Body

| Name                                 | Type   | Description |
| ------------------------------------ | ------ | ----------- |
| id<mark style="color:red;">\*</mark> | String |             |

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

***

### Doctor

<mark style="color:green;">`POST`</mark> `/doctor/appointments`

#### Request Body

| Name                                          | Type      | Description |
| --------------------------------------------- | --------- | ----------- |
| id\_patient                                   | String    |             |
| start\_date<mark style="color:red;">\*</mark> | Timestamp |             |
| end\_date<mark style="color:red;">\*</mark>   | Timestamp |             |

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/doctor/appointments`

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/doctor/appointments/{id}`

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

<mark style="color:orange;">`PUT`</mark> `/doctor/appointments/{id}`

#### Request Body

| Name                                 | Type   | Description |
| ------------------------------------ | ------ | ----------- |
| id<mark style="color:red;">\*</mark> | String |             |

{% tabs %}
{% tab title="201: Created " %}

{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}

## Cancel an appointment

<mark style="color:red;">`DELETE`</mark> `/doctor/appointments/{id}`

#### Request Body

| Name                                     | Type   | Description        |
| ---------------------------------------- | ------ | ------------------ |
| reason<mark style="color:red;">\*</mark> | String | Cancelation reason |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request " %}

{% endtab %}
{% endtabs %}
