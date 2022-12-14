# 🚀 Quick Start

{% hint style="warning" %}
**Attention:** This is a private API, which means that its url will not figure in this documentation. If you want to get access to it, please send an email to [our development team](#user-content-fn-1)[^1].
{% endhint %}

## About authentication

Your API requests are authenticated using a Bearer token associated with a valid user. Any request that doesn't include a Bearer token will return an error.

You can generate a Bearer token using the [authentication.md](reference/api-reference/authentication.md "mention") requests at any time.

## Use the API

You can interact with our API using HTTP requests. Check out [api-reference](reference/api-reference/ "mention") for a detailed list of our available routes.

## Make your first request

To make your first request, send an authenticated request to the `patient` endpoint. This will return all the information concerning the patient that is logged in.

If your token belongs to a `Doctor` instance, you can send that request to the `doctor` endpoint.

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/patient" method="get" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/patient" method="get" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

Take a look at how you might call this method using `curl`:

{% tabs %}
{% tab title="curl" %}
```bash
curl { API_URL }/patient  
    -H "Authorization: Bearer YOUR_TOKEN"
```
{% endtab %}
{% endtabs %}

[^1]: dev.edgar.care@gmail.com
