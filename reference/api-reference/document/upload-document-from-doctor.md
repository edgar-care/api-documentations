# 📃 Upload Document from doctor

<mark style="color:green;">`POST`</mark> `/doctor/document/upload`

{% tabs %}
{% tab title="Body" %}


| Name                                           | Type    | Description                            |
| ---------------------------------------------- | ------- | -------------------------------------- |
| document<mark style="color:red;">\*</mark>     | FIle    |                                        |
| isFavorite<mark style="color:red;">\*</mark>   | Boolean |                                        |
| category<mark style="color:red;">\*</mark>     | String  | GENERAL / FINANCE                      |
| documentType<mark style="color:red;">\*</mark> | String  | XRAY, PRESCRIPTION, OTHER, CERTIFICATE |
| patient\_id                                    | String  |                                        |
{% endtab %}

{% tab title="return 201" %}
```json

{
    "message":
        "Document created successfully",
        "upload":
        {
                "id":"6608522b7bc5a13c2b5cf495",
                "owner_id":"660048d41955d2a3c7141138",
                "name":"2025_PLD_edgarcare_202306KO.pdf",
                "document_type":"GENERAL",
                "category":"GENERAL",
                "is_favorite":false,
                "download_url":"https://document-patient.s3.amazonaws.com/2025_PLD_edgarcare_202306KO.pdf"
        }
}

```
{% endtab %}
{% endtabs %}



\=========================================================================

<mark style="color:blue;">`GET`</mark> `/doctor/document/download/{id}`

{% tabs %}
{% tab title="No Body" %}

{% endtab %}

{% tab title="return 200" %}
```json

{
    "download":{
        "id":"String",
        "owner_id":"String",
        "name":"String",
        "document_type":"ENUM",
        "category":"ENUM"
        "is_favorite":Boolean,
        "download_url":"String"
    },"message":"Document get succesfuly"
}

```
{% endtab %}
{% endtabs %}
