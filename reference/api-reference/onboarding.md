# 📃 Onboarding

The "onboarding" route is a streamlined process designed to gather essential user information swiftly. This route serves as a welcome step, collecting necessary details to personalize the user experience and enhance their engagement with the platform.





### Health (In working)

{% swagger method="post" path=" " baseUrl="/onboarding/health" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="patients_allergies" type="String" %}
(optional)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_illness" type="String" %}
(optional)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_primary_doctor" type="String" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="patients_treatments" type="[String]" %}
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

{% swagger-parameter in="body" name="name" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="surname" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="birthdate" required="true" type="Int" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="sexe" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="weight" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-parameter in="body" name="height" required="true" type="String" %}
(required)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get Info Health (check if you share all information)" %}

{% endswagger-response %}
{% endswagger %}

