# Definition
```python
- attribute of a cookie where the web server can set the cookie to send if the request is originated from their web server or domain.
- rules of cookie if it will sent to requested domain depends if it is strict, lax or none.
- used to prevent Cross-Site Request Forgery(CSRF) and Cross-Site Scripting(XSS).
-  


```


# SameSite Strict
```python
- cannot load files that are requested from another domain
- cookie will not send if the request is from another domain including all HTTP request


@Portswigger`
 If a cookie is set with the SameSite=Strict attribute, browsers will not send it in any cross-site requests. In simple terms, this means that if the target site for the request does not match the site currently shown in the browser's address bar, it will not include the cookie.

This is recommended when setting cookies that enable the bearer to modify data or perform other sensitive actions, such as accessing specific pages that are only available to authenticated users.

Although this is the most secure option, it can negatively impact the user experience in cases where cross-site functionality is desirable. 

```




# SameSite Lax
```python
- cannot load files that are requested from another domain
- cookie will send from another domain if the request is GET and reject POST request
- onyl GET HTTP Request Method is allowed.


@Portswigger`
Lax SameSite restrictions mean that browsers will send the cookie in cross-site requests, but only if both of the following conditions are met:

- The request uses the GET method.
- The request resulted from a top-level navigation by the user, such as clicking on a link.
    

This means that the cookie is not included in cross-site `POST` requests, for example. As `POST` requests are generally used to perform actions that modify data or state (at least according to best practice), they are much more likely to be the target of CSRF attacks.

Likewise, the cookie is not included in background requests, such as those initiated by scripts, iframes, or references to images and other resources.

```




# SameSite None
```python
- can load files that are requested from another domain
- cookie will send if the request is from another domain
- all HTTP Request Method is allowed.




@Portswigger`
If a cookie is set with the `SameSite=None` attribute, this effectively disables SameSite restrictions altogether, regardless of the browser. As a result, browsers will send this cookie in all requests to the site that issued it, even those that were triggered by completely unrelated third-party sites.

With the exception of Chrome, this is the default behavior used by major browsers if no `SameSite` attribute is provided when setting the cookie.

There are legitimate reasons for disabling SameSite, such as when the cookie is intended to be used from a third-party context and doesn't grant the bearer access to any sensitive data or functionality. Tracking cookies are a typical example.

```


























