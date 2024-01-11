# 📃 Document

{% swagger baseUrl="/" summary="" method="post" path="document/upload" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="document" required="true" type="FIle" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="isFavorite" type="Boolean" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="category" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="documentType" type="String" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Unable to upload file" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="post" path="document/favorite/{id}" %}
{% swagger-description %}
Execute the query to change the status. If true, the query will change to false and vice versa.
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="no documents in result" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="get" path="document/download/{id}" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="no documents in result" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="delete" path="document/{id}" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="no documents in result" %}

{% endswagger-response %}
{% endswagger %}

{% swagger baseUrl="/" summary="" method="delete" path="document/favorite/{id}" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}

{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="no documents in result" %}

{% endswagger-response %}
{% endswagger %}
