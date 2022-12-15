# 🔠 Exam using NLP

The whole NLP / Exam process is based on the `ExamContextItem` type defined below :&#x20;

<details>

<summary>ExamContextItem</summary>

```json
{
    "symptom": "symptom_key",
    "present": true | false
}
```

</details>

## NLP

You can use the `nlp` endpoint to parse user input and get objects to add to your `ExamContextItem` list.

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/nlp" method="get" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}

## Exam

The `exam` endpoint will treat a single list of `ExamContextItem` by sorting and processing it, so the client will get either a new question to ask the user or a context containing all the needed information for a diagnosis.

{% swagger src="https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml" path="/exam" method="get" %}
[https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml](https://raw.githubusercontent.com/edgar-care/lambdas/dev/openapi.yaml)
{% endswagger %}
