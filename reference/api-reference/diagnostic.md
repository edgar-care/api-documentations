# 👨⚕ Diagnostic



{% swagger method="post" path="" baseUrl="/diagnostic/initiate" summary="Initiate a session and returns a sessionId" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="The session has been created" %}
```json
{
    "sessionId": "string"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="" baseUrl="/diagnostic/diagnose" summary="Takes what the patient said and returns the next question" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" required="true" %}
session's Id from /initiate
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sentence" required="true" %}
Patient's sentence wrote in chat
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The diagnostic step has succeeded" %}
```json
{
    "done": bool, // true if simulation is finished
    "question": "string" // next question to ask to the patient
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The diagnostic step has failed" %}
```
{
    "message": "string"
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="" baseUrl="/diagnostic/summary/{id}" summary="Retrieve the summary of a session" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}
Session Id
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="The session's summary has been retrieved" %}
```
{
    "sessionId": "string",
    "symptoms": [{"symptom": "string", "present": boolean|null}],
    "age": int,
    "height": int,
    "weight": int,
    "sex": "MALE"|"FEMALE"|"OTHER",
    "logs": [{"question": "string", "answer": "string"}]
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="The session's summary could not be retrieved" %}
```
{
    "message": "string"
}
```
{% endswagger-response %}
{% endswagger %}
