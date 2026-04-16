# Security Policy

## 🔒 Our Commitment to Security

Security is a top priority for RecipesGalore. As an open source project, we believe in transparency and responsible disclosure. We appreciate the security community's efforts to help keep our users safe.

## 🛡️ Security Practices

### GitHub Advanced Security (GHAS)

This repository uses **GitHub Advanced Security** to:
- 🔍 Scan for known vulnerabilities in dependencies (Dependabot)
- 🔎 Detect security vulnerabilities in code (CodeQL)
- 🚨 Alert maintainers of potential security issues
- 🔄 Automatically create PRs for dependency updates

### Code Review & Branch Protection

All code changes:
- ✅ Must go through pull request review
- ✅ Cannot be pushed directly to main branch
- ✅ Are automatically scanned for security issues
- ✅ Require approval from maintainers

### Secrets Management

We **never** commit secrets to the repository:
- ❌ No API keys, passwords, or credentials in code
- ✅ Use GitHub Secrets for sensitive data
- ✅ Firebase service accounts stored securely
- ✅ Regular secret rotation practices

## 🐛 Supported Versions

We provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| Latest  | ✅ Yes             |
| < Latest| ⚠️ Best effort     |

**Recommendation:** Always use the latest version deployed at [recipesgalore-web.web.app](https://recipesgalore-web.web.app)

## 🚨 Reporting a Vulnerability

### Please Report Security Vulnerabilities Responsibly

If you discover a security vulnerability, **please do NOT open a public issue**. We appreciate responsible disclosure to protect our users.

### How to Report

**Email:** [kencrismon@crismonicwave.com](mailto:kencrismon@crismonicwave.com)

**Subject Line:** `[SECURITY] RecipesGalore Web - [Brief Description]`

**Include in Your Report:**
1. **Description** - Clear explanation of the vulnerability
2. **Impact** - What could an attacker do with this?
3. **Steps to Reproduce** - Detailed steps to demonstrate the issue
4. **Proof of Concept** - Code, screenshots, or video (if applicable)
5. **Suggested Fix** - If you have ideas for remediation
6. **Your Contact Info** - So we can follow up with questions

**Example Report:**
```
Subject: [SECURITY] RecipesGalore Web - XSS in Search Feature

Description:
The recipe search feature does not properly sanitize user input, 
allowing injection of malicious scripts.

Impact:
An attacker could inject JavaScript that executes in other users' 
browsers, potentially stealing session tokens or performing actions 
on behalf of users.

Steps to Reproduce:
1. Go to search box on homepage
2. Enter: <script>alert('XSS')</script>
3. Submit search
4. Script executes in browser

Proof of Concept:
[Screenshot attached showing alert dialog]

Suggested Fix:
Use Angular's built-in sanitization or DOMPurify library to 
sanitize all user input before rendering.

Contact: security-researcher@example.com
```

### What Happens Next?

1. **Acknowledgment** - We'll respond within **48 hours** to confirm receipt
2. **Investigation** - We'll investigate and validate the issue
3. **Updates** - We'll keep you informed of progress
4. **Fix & Release** - We'll develop and deploy a fix
5. **Disclosure** - We'll coordinate public disclosure with you
6. **Credit** - We'll acknowledge your contribution (if you wish)

### Response Timeline

- **48 hours** - Initial response acknowledging receipt
- **7 days** - Preliminary assessment and severity rating
- **30 days** - Fix developed and deployed (for high severity)
- **90 days** - Maximum time before public disclosure

We aim to be faster than these timelines for critical vulnerabilities.

## 🏆 Security Researchers

We deeply appreciate security researchers who help make RecipesGalore safer. While we don't currently offer a bug bounty program, we will:

- ✅ Credit you in our security acknowledgments (unless you prefer to remain anonymous)
- ✅ Keep you informed throughout the remediation process
- ✅ Coordinate disclosure timing with you
- ✅ Share what we learned and how we fixed it

## ⚠️ Out of Scope

Please **do not** report:
- Issues in third-party dependencies (report to the upstream project)
- Spam or social engineering attacks
- Issues requiring physical access to a user's device
- Reports from automated tools without validation
- Issues in outdated or unsupported versions
- Theoretical vulnerabilities without proof of exploitability

## 🔐 Security Best Practices for Contributors

If you're contributing code:

### Do:
- ✅ Validate and sanitize all user input
- ✅ Use Angular's built-in security features
- ✅ Follow OWASP Top 10 guidelines
- ✅ Use parameterized queries (when we add a backend)
- ✅ Implement proper authentication and authorization
- ✅ Keep dependencies up to date
- ✅ Review Dependabot alerts and act on them

### Don't:
- ❌ Trust user input
- ❌ Disable security features (without excellent reason)
- ❌ Use `eval()` or similar dynamic code execution
- ❌ Expose sensitive data in client-side code
- ❌ Commit secrets, keys, or credentials
- ❌ Use deprecated or vulnerable libraries

## 📚 Security Resources

### Angular Security
- [Angular Security Guide](https://angular.io/guide/security)
- [Content Security Policy (CSP)](https://angular.io/guide/security#content-security-policy)

### OWASP
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)

### Firebase Security
- [Firebase Security Rules](https://firebase.google.com/docs/rules)
- [Firebase Authentication Best Practices](https://firebase.google.com/docs/auth/web/auth-best-practices)

## 📞 Contact

**Security Issues:** [kencrismon@crismonicwave.com](mailto:kencrismon@crismonicwave.com)  
**General Questions:** [GitHub Discussions](https://github.com/CrismonicWave-org/recipesgalore-web/discussions)

## 📄 Disclosure Policy

When a security issue is reported and fixed:

1. We'll publish a **security advisory** on GitHub
2. We'll update our changelog with security fix details
3. We'll credit the researcher (if they agree)
4. We'll coordinate timing with the reporter
5. We'll share lessons learned with the community

## 🙏 Thank You

Security research takes time and skill. We're grateful to everyone who helps keep RecipesGalore safe and secure. Your responsible disclosure protects our users and makes open source better for everyone.

**Thank you for helping us build a safer recipe community!** 🛡️👨‍🍳👩‍🍳

---

*Last Updated: April 2026*  
*Version: 1.0*
