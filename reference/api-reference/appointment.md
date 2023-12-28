# 🏥 Appointment

### Patient

{% swagger method="post" path="appointments/{id} " baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="patient/appointments/{id} " baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="doctor/{id}/appointments " baseUrl="/" summary="{id} => id Doctor" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="patient/appointments " baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="delete" path="appointments/{id} " baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="appointments/{id} " baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to get health (check if you share all information) " %}

{% endswagger-response %}
{% endswagger %}

***

### Doctor

{% swagger method="post" path="doctor/appointments" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id_patient" type="String" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="start_date" required="true" type="Timestamp" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="end_date" required="true" type="Timestamp" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="doctor/appointments" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="doctor/appointments/{id}" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}

{% swagger method="put" path="doctor/appointments/{id}" baseUrl="/" summary="" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}

{% endswagger-response %}
{% endswagger %}
