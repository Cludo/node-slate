<h2 id="authentication_basic">Basic authentication</h2>

```shell
curl -X GET \
-I https://api.cludo.com/api/v3/search \
-u {CustomerId}:{API_Key} \

#result header example:
> GET /api/v3/search HTTP/1.1
> Host: https://api.cludo.com
> Authorization: Basic Q3VzdG9tZXJJZDpDdXN0b21lcktleQ==
```

All API endpoints, except search, requires [Basic auth](http://en.wikipedia.org/wiki/Basic_access_authentication) over HTTP, where the username is your CustomerId, and the password is your API_Key. You can [contact](https://www.cludo.com/en/contact/) Cludo to get your id and key.

Most HTTP clients provide ways to automatically set your id and key upon the request header, but sometimes you may need to set it explicity. To do so, Base64-encode a string containing your id and key separated by a `:`.

`Authorization: Basic <Base64({CustomerId}:{API_Key})>`

<aside class="notice">
You must replace <code>CustomerId</code> with your customer id and the <code>API_Key</code> with your personal API key.
</aside>