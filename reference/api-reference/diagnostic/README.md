# 👨⚕ Diagnostic

{% swagger method="post" path="" baseUrl="/diagnostic/initiate" summary="Initiate a session and returns a sessionId" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="The session has been created, returns sessionId" %}

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

{% swagger-response status="200: OK" description="returns "done"=true if the prediagnostic is finished, "question"= next question" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}
