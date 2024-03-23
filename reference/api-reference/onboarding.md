# 📃 Onboarding

The "onboarding" route is a streamlined process designed to gather essential user information swiftly. This route serves as a welcome step, collecting necessary details to personalize the user experience and enhance their engagement with the platform.





### Health (In working)

<mark style="color:green;">`POST`</mark> `/onboarding/health`&#x20;

#### Request Body

| Name                                                        | Type      | Description |
| ----------------------------------------------------------- | --------- | ----------- |
| patients\_allergies                                         | String    | (optional)  |
| patients\_illness                                           | String    | (optional)  |
| patients\_primary\_doctor<mark style="color:red;">\*</mark> | String    |             |
| patients\_treatments                                        | \[String] | (optional)  |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get health (check if you share all information) " %}

{% endtab %}
{% endtabs %}

### Infos

<mark style="color:green;">`POST`</mark> `/onboarding/infos`&#x20;

#### Request Body

| Name                                        | Type   | Description |
| ------------------------------------------- | ------ | ----------- |
| name<mark style="color:red;">\*</mark>      | String | (required)  |
| surname<mark style="color:red;">\*</mark>   | String | (required)  |
| birthdate<mark style="color:red;">\*</mark> | String | (required)  |
| sex<mark style="color:red;">\*</mark>       | String | (required)  |
| weight<mark style="color:red;">\*</mark>    | String | (required)  |
| height<mark style="color:red;">\*</mark>    | String | (required)  |

{% tabs %}
{% tab title="200: OK " %}

{% endtab %}

{% tab title="400: Bad Request Unable to get Info Health (check if you share all information)" %}

{% endtab %}
{% endtabs %}

