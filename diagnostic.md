# 👨‍⚕️ Diagnostic



## Initiate a session and returns a sessionId

<mark style="color:green;">`POST`</mark> `/diagnostic/initiate`

{% tabs %}
{% tab title="200: OK The session has been created" %}
```json
{
    "sessionId": "string"
}
```
{% endtab %}
{% endtabs %}

## Takes what the patient said and returns the next question

<mark style="color:green;">`POST`</mark> `/diagnostic/diagnose`

#### Request Body

| Name                                       | Type   | Description                      |
| ------------------------------------------ | ------ | -------------------------------- |
| id<mark style="color:red;">\*</mark>       | String | session's Id from /initiate      |
| sentence<mark style="color:red;">\*</mark> | String | Patient's sentence wrote in chat |

{% tabs %}
{% tab title="200: OK The diagnostic step has succeeded" %}
```json
{
    "done": bool, // true if simulation is finished
    "question": "string" // next question to ask to the patient
}
```
{% endtab %}

{% tab title="400: Bad Request The diagnostic step has failed" %}
```
{
    "message": "string"
}
```
{% endtab %}
{% endtabs %}

## Retrieve the summary of a session

<mark style="color:blue;">`GET`</mark> `/diagnostic/summary/{id}`

#### Path Parameters

| Name                                 | Type   | Description |
| ------------------------------------ | ------ | ----------- |
| id<mark style="color:red;">\*</mark> | String | Session Id  |

{% tabs %}
{% tab title="200: OK The session's summary has been retrieved" %}
```
{
    "session_id": "string",
    "diseases": [{"name": "string", "presence": float}]
    "fiability": float,
    "symptoms": [{"symptom": "string", "present": boolean|null, "duration": int|null, "treated": ["string"]}],
    "alert": [{
        "id": "string",
        "name": "string",
        "sex": "string"|null,
        "height": int|null,
        "weight": int|null,
        "symptoms": ["string"],
        "comment": "string"
    }]
    "logs": [{"question": "string", "answer": "string"}]
}
```
{% endtab %}

{% tab title="400: Bad Request The session's summary could not be retrieved" %}
```
{
    "message": "string"
}
```
{% endtab %}
{% endtabs %}



## Get NLP Status

<mark style="color:blue;">`GET`</mark> `/nlp/status`

{% tabs %}
{% tab title="200: " %}
{

"status": "running"

}
{% endtab %}
{% endtabs %}

