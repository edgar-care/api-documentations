# 📃 Document

<mark style="color:green;">`POST`</mark> `/document/upload`

Fichier autoriser : \
PDF\
DOC

DOCX\
ODT

ODTX

PNG

#### Request Body

| Name                                           | Type    | Description                            |
| ---------------------------------------------- | ------- | -------------------------------------- |
| document<mark style="color:red;">\*</mark>     | FIle    |                                        |
| isFavorite<mark style="color:red;">\*</mark>   | Boolean |                                        |
| category<mark style="color:red;">\*</mark>     | String  | GENERAL / FINANCE                      |
| documentType<mark style="color:red;">\*</mark> | String  | XRAY, PRESCRIPTION, OTHER, CERTIFICATE |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to upload file" %}

{% endtab %}
{% endtabs %}

<mark style="color:green;">`POST`</mark> `/document/favorite/{id}`

Execute the query to change the status. If true, the query will change to false and vice versa.

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/document/download/{id}`

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:blue;">`GET`</mark> `/document/download`

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:orange;">`PUT`</mark> `/document/{id}`

#### Request Body

| Name                                   | Type   | Description                    |
| -------------------------------------- | ------ | ------------------------------ |
| name<mark style="color:red;">\*</mark> | String | mettre l'extension dans le nom |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to upload file" %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/document/{id}`

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}

<mark style="color:red;">`DELETE`</mark> `/document/favorite/{id}`

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request no documents in result" %}

{% endtab %}
{% endtabs %}
