# 📃 Onboarding

The "onboarding" route is a streamlined process designed to gather essential user information swiftly. This route serves as a welcome step, collecting necessary details to personalize the user experience and enhance their engagement with the platform.





### Health

{% swagger method="post" path=" " baseUrl="/onboarding/health" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Patientallergies" type="String" %}
(optional)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Patientsillness" type="String" %}
(optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

### Infos

{% swagger method="post" path=" " baseUrl="/onboarding/infos" summary="" expanded="false" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="Name" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Surname" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Age" required="true" type="Int" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Sexe" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Weight" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="Height" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get Info Health (check if you share all information)" %}

{% endswagger-response %}
{% endswagger %}



{% swagger method="get" path="" baseUrl="" summary="" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}
