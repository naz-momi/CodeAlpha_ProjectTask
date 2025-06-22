# Task 3: Secure Coding Review – OWASP Juice Shop (CodeAlpha Internship)

This project is part of my internship at **CodeAlpha** under the **Cybersecurity Intern** role.  
I performed a security analysis of the intentionally vulnerable web application **OWASP Juice Shop**, discovering and exploiting real-world flaws including Broken Authentication, Improper Input Validation, and Cross-Site Scripting (XSS).

---

##  Objective

- Analyze a vulnerable web app for insecure coding patterns.
- Identify critical web vulnerabilities.
- Provide remediation suggestions based on OWASP Top 10.

---

##  Tools & Technologies

- [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- Burp Suite 
- Firefox Developer Tools
- Manual testing techniques



##  Challenges Solved

###  Broken Authentication
- **Basket Manipulation:**  
  Used **Burp Suite** to intercept and modify basket item quantities and prices. This allowed manipulation of order totals — a classic example of trusting client-side logic.

- **Product Tampering:**  
  Intercepted product details in a request and modified the product ID and price. This bypassed integrity checks and revealed how insecure session handling can be abused.

###  Improper Input Validation
- **Upload Type Challenge:**  
  Uploaded a file with a disguised extension using Burp. Bypassed front-end checks by altering headers/payload and uploaded unauthorized files, revealing a lack of server-side file validation.

###  Cross-Site Scripting (XSS)
- **Reflected XSS Challenge:**  
  Injected the payload `<script>alert("XSS")</script>` into a vulnerable input field. It executed successfully due to lack of output sanitization, confirming reflected XSS.



## 🧹 Remediation Suggestions

| Vulnerability | Fix Recommendation |
|---------------|--------------------|
| Broken Authentication | Validate session tokens on server-side, avoid price manipulation from the client. |
| Input Validation | Enforce strict MIME and extension checks server-side. |
| XSS | Sanitize and escape user inputs; use CSP headers. |


## Learning Outcomes

Learned manual web app testing methodology.

Understood exploitation of broken auth, input validation flaws, and XSS.

Gained experience using Burp Suite for real-world bug identification.

## Author

Momal Naz Cybersecurity Intern @ CodeAlpha 📧 momalnaz1234@gmail.com


