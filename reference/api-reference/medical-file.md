# 📂 Medical File

{% swagger method="get" path="dashboard/medical-info" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="dashboard/medical-info" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="onboarding_info" type="{}" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="String" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="surname" type="String" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="birthdate" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="sex" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="weight" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="height" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="onboarding_health" type="{}" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_allergies" type="[String]" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_illness" type="[String]" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_treatments" type="[String]" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_primary_doctor" type="String" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}
