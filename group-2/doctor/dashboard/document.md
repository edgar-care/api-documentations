---
description: >-
  Permettre au doctor d'upload des documents dans la base du patient, mais aussi
  de récupérer des documents.
---

# 📄 Document

<mark style="color:green;">`POST`</mark> `/doctor/document/upload`

{% tabs %}
{% tab title="Body" %}
|              |         |   |
| ------------ | ------- | - |
| document     | File    |   |
| isFavorite   | Boolean |   |
| category     | ENUM    |   |
| documentType | ENUM    |   |
| patient\_id  | String  |   |
{% endtab %}

{% tab title="Return" %}
```json

{
    "message":"Document created successfully",
    "upload":{
        "id":"String",
        "owner_id":"String",
        "name":"String",
        "document_type":"ENUM",
        "category":"ENUM",
        "is_favorite":Boolean,
        "download_url":"String Url"
}

```
{% endtab %}
{% endtabs %}

\=========================================================================

<mark style="color:blue;">`GET`</mark> `/doctor/document/{id}`

{% tabs %}
{% tab title="Body" %}
No Body
{% endtab %}

{% tab title="Return" %}
```json

{
    "download":{
        "id":"String",
        "owner_id":"String",
        "name":"String",
        "document_type":"ENUM",
        "category":"ENUM",
        "is_favorite":Boolean,
        "download_url":"String Url"
    },
    "message":"Document get succesfuly"
}

```
{% endtab %}
{% endtabs %}
