# JavaScript Vulnerability Demo

This project demonstrates two common JavaScript security vulnerabilities and their mitigations:

1. **Cross-Site Scripting (XSS)** using `innerHTML`
2. **Dynamic Code Execution** using `eval()`

## 📁 Directory Structure

```
src/
├── vulnerable/
│   ├── xss.html          # Demonstrates XSS via innerHTML
│   └── eval.html         # Demonstrates eval() vulnerability
├── mitigated/
│   ├── xss_safe.html     # Safe version using DOMPurify
│   └── eval_safe.html    # Safe version using whitelisting
├── README.md
```

## 🛠 How to Run

You can open each HTML file in your web browser manually

### Option 1: Manual

Open each HTML file in your browser:
```bash
# macOS / Linux
open vulnerable/xss.html
open vulnerable/eval.html
open mitigated/xss_safe.html
open mitigated/eval_safe.html

# Windows (PowerShell or CMD)
start vulnerable\xss.html
start vulnerable\eval.html
start mitigated\xss_safe.html
start mitigated\eval_safe.html
```

## 📦 Dependencies

For `mitigated/xss_safe.html`, this demo uses:
- [DOMPurify CDN](https://github.com/cure53/DOMPurify)

For `mitigated/eval_safe.html`, this demo uses:
- [mathjs browser bundle via CDN] for safe arithmetic parsing/evaluation (no `eval()` required).

No installation is required. Just open the HTML files in your browser.

## ⚠️ Important warnings

- The `vulnerable/` pages intentionally show insecure coding **patterns** for educational purposes only. **Do not** deploy those pages or patterns to public-facing production servers.
- Always validate and sanitize user input and prefer safe APIs or libraries when evaluating expressions or accepting HTML.

## Resources
- OWASP XSS Prevention Cheat Sheet
- DOMPurify documentation
- mathjs documentation
