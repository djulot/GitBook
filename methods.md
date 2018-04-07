# Defining Methods

Methods allow you to smoothly display code examples in different languages.

{% method %}
## My first method

My first method exposes how to print a message in JavaScript and Go.

{% sample lang="curl" %}
Code pour le cURL.

```cURL
-X POST 
-d '{"objet": "nouveau"}'
```

{% sample lang="fmp" %}
Code pour l'option cURL dans FileMaker.

```fmp
"-X POST " &
"-d " & citation ( "{\"objet\": \"nouveau\"}" )
```

{% common %}
Whatever language you are using, the result will be the same.

```bash
$ My first method
```
{% endmethod %}
