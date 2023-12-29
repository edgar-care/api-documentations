# 📅 Slot

{% swagger baseUrl="/" summary="" method="post" path="doctor/slot" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="start_date" required="true" type="Timestamp" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="end_date" type="Timestamp" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="get" path="doctor/slot/{id}" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="get" path="doctor/slots" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="delete" path="doctor/slot/{id}" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}
