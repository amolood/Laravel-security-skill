# PHP / Laravel Security Architect Prompt

A professional security audit prompt designed for reviewing PHP and Laravel applications using industry-recognized security standards such as OWASP ASVS, OWASP Top 10, OWASP API Security Top 10, NIST, PCI-DSS, GDPR, SAMA, and other compliance frameworks.

This prompt is intended to guide AI-assisted code reviews, security assessments, penetration-test preparation, architecture reviews, and production-readiness evaluations for Laravel and PHP-based systems.

---

## Overview

The **PHP / Laravel Security Architect Prompt** turns an AI assistant into a senior application security architect specialized in:

* PHP Security
* Laravel Security
* Web Application Security
* API Security
* Authentication and Authorization
* Secure Session Management
* Secure File Uploads
* Database Security
* OWASP ASVS
* OWASP Top 10
* OWASP API Security Top 10
* Secure CI/CD
* DevSecOps
* Threat Modeling
* Compliance Readiness

The prompt is designed to produce detailed, evidence-based security findings with clear remediation steps, secure code examples, verification instructions, and prioritized roadmaps.

---

## Purpose

The purpose of this prompt is to help teams perform a structured security assessment of PHP and Laravel applications.

It helps identify:

* Vulnerabilities in source code
* Insecure architecture decisions
* Weak authentication flows
* Broken access control
* Exposed secrets
* Insecure Laravel configuration
* SQL injection risks
* Mass assignment vulnerabilities
* File upload risks
* API security issues
* Webhook security gaps
* Logging and error handling risks
* Dependency vulnerabilities
* CI/CD and deployment weaknesses
* Server and infrastructure misconfigurations
* Business logic flaws
* Race conditions and concurrency risks

---

## Target Users

This prompt is useful for:

* Security Engineers
* Laravel Developers
* Backend Developers
* DevSecOps Engineers
* CTOs and Technical Leads
* Penetration Testers
* Compliance Teams
* FinTech Teams
* Government Application Teams
* Software Auditors
* QA Security Teams

---

## Supported Project Types

This prompt can be used with:

* Laravel Web Applications
* Laravel REST APIs
* Laravel SaaS Platforms
* Laravel Admin Panels
* Laravel Multi-Tenant Applications
* PHP Legacy Systems
* Payment Platforms
* Wallet Systems
* Booking Systems
* E-commerce Platforms
* Government Portals
* FinTech Backends
* Mobile App Backends
* CRM and ERP Systems

---

## Security Standards Covered

The audit methodology references the following standards:

* OWASP ASVS
* OWASP Top 10
* OWASP API Security Top 10
* OWASP WSTG
* OWASP SAMM
* NIST Cybersecurity Framework
* NIST Zero Trust Architecture
* PCI-DSS
* GDPR
* CCPA
* SAMA
* CBE
* ISO 27001
* CIS Benchmarks

---

## Audit Phases

The prompt follows a structured multi-phase review methodology.

### Phase 1: Architecture Review

Reviews the application structure, service boundaries, MVC implementation, middleware design, dependency injection, service providers, queues, schedulers, third-party packages, admin panels, APIs, and multi-tenancy design.

### Phase 2: Threat Modeling

Builds a threat model using STRIDE and DREAD to identify attack vectors, abuse cases, and business-impact risks.

### Phase 3: Secrets Audit

Searches for exposed credentials, `.env` files, API keys, database passwords, JWT secrets, OAuth secrets, SMTP credentials, webhook secrets, private keys, and cloud credentials.

### Phase 4: Authentication Review

Reviews login, registration, password reset, MFA, OTP, OAuth, Laravel Sanctum, Laravel Passport, JWT authentication, session authentication, and token expiration.

### Phase 5: Authorization and Access Control Review

Reviews Policies, Gates, Middleware, RBAC, permissions, object ownership, tenant isolation, admin authorization, and privilege escalation risks.

### Phase 6: Session and Cookie Security Review

Checks session lifetime, secure cookies, HttpOnly, SameSite, session regeneration, logout invalidation, and CSRF protections.

### Phase 7: Input Validation Review

Reviews Form Requests, controller validation, DTOs, request sanitization, nested input validation, and strict rule enforcement.

### Phase 8: SQL Injection and Database Security

Searches for unsafe raw queries, dynamic sorting, unescaped filters, unsafe stored procedures, and excessive database privileges.

### Phase 9: Mass Assignment Review

Checks `$fillable`, `$guarded`, `create($request->all())`, `update($request->all())`, role fields, admin flags, ownership fields, and balance fields.

### Phase 10: File Upload Security

Reviews file validation, MIME checks, extensions, file size limits, private storage, randomized filenames, malware scanning, and public file exposure.

### Phase 11: XSS and Output Encoding Review

Reviews Blade templates, Livewire, Inertia, Vue/React components, rich text editors, Markdown rendering, unsafe HTML rendering, and CSP.

### Phase 12: CSRF and CORS Review

Checks CSRF middleware, excluded routes, API cookie authentication, Sanctum configuration, wildcard origins, and credentialed CORS risks.

### Phase 13: API Security

Reviews route protection, authentication, authorization, rate limiting, request signing, replay protection, webhook validation, and sensitive data in URLs.

### Phase 14: Webhook Security

Verifies signature validation, timestamp checks, replay prevention, idempotency, and safe logging for payment and third-party webhooks.

### Phase 15: Cryptography Review

Searches for MD5, SHA1, DES, ECB mode, static IVs, hardcoded keys, weak random values, and custom encryption.

### Phase 16: Logging and Error Handling

Reviews `APP_DEBUG`, Laravel logs, exception handling, stack traces, sensitive data logging, failed jobs, payment logs, and API error responses.

### Phase 17: Queue, Jobs, and Scheduler Security

Reviews queued jobs, failed job payloads, scheduled commands, worker privileges, and unsafe shell execution.

### Phase 18: SSRF Review

Reviews URL fetchers, HTTP clients, image importers, link previews, PDF generators, webhook callers, and internal network access.

### Phase 19: Insecure Deserialization Review

Searches for unsafe `unserialize()` usage, magic methods, signed payload misuse, and unsafe base64-decoded payloads.

### Phase 20: Cache and Temporary Data Security

Reviews Redis, Memcached, file cache, temporary exports, signed URLs, cache key isolation, and tenant-aware caching.

### Phase 21: Dependency Security

Reviews Composer and NPM dependencies, known CVEs, abandoned packages, unmaintained packages, and risky transitive dependencies.

### Phase 22: Laravel Configuration Hardening

Reviews `.env`, `config/*.php`, debug mode, session security, CORS, Sanctum, Passport, Telescope, Horizon, Debugbar, Ignition, and trusted proxies.

### Phase 23: Admin Panel Security

Reviews Laravel Nova, Filament, Backpack, Voyager, custom admin dashboards, exports, bulk actions, audit logging, MFA, and admin authorization.

### Phase 24: Payment and Financial Security

Reviews payment flows, wallets, balances, refunds, subscriptions, discounts, coupons, commissions, settlements, idempotency, and PCI-DSS scope.

### Phase 25: Privacy and Compliance Review

Reviews personal data, financial data, national ID data, location data, consent, retention, deletion, exports, encryption, and access logging.

### Phase 26: CI/CD and Deployment Security

Reviews GitHub Actions, GitLab CI, Docker, Kubernetes, Forge, Vapor, Envoyer, deployment scripts, secret handling, artifact security, SAST, DAST, and SCA.

### Phase 27: Server and Infrastructure Security

Reviews Nginx/Apache, PHP-FPM, file permissions, public directory exposure, TLS, databases, Redis, backups, cron jobs, and Supervisor workers.

### Phase 28: Reverse Engineering and Source Exposure

Checks for exposed `.git`, `.env`, `composer.json`, logs, backups, vendor directories, storage files, and public source maps.

### Phase 29: Business Logic Security

Reviews order flows, booking flows, wallet flows, coupon flows, refunds, approvals, role changes, inventory, subscriptions, and multi-step process bypasses.

### Phase 30: Race Condition and Concurrency Review

Reviews balance updates, inventory updates, coupon redemption, payment confirmation, concurrent requests, transactions, row locks, and idempotency keys.

---

## Scoring Model

The security score starts at `100` and is reduced based on the severity of findings.

| Severity | Deduction |
| -------- | --------: |
| Critical |       -10 |
| High     |        -5 |
| Medium   |        -2 |
| Low      |        -1 |

Minimum score: `0`
Maximum score: `100`

---

## Risk Levels

The final risk level should be calculated based on the number and severity of findings.

| Score Range | Risk Level    |
| ----------- | ------------- |
| 90–100      | Low Risk      |
| 70–89       | Medium Risk   |
| 40–69       | High Risk     |
| 0–39        | Critical Risk |

---

## Expected Output

The prompt generates a structured security report containing:

* Executive Summary
* Security Score
* Risk Level
* OWASP ASVS Coverage
* OWASP Top 10 Coverage
* Critical Findings
* High Findings
* Medium Findings
* Low Findings
* Detailed Finding Templates
* Evidence
* Attack Scenarios
* Business Impact
* Secure Code Examples
* Remediation Steps
* Verification Steps
* Remediation Roadmap

---

## Finding Format

Each finding must include:

```markdown
### ID

### Title

### Severity

### Location

Exact file path and line number.

### Evidence

Code snippet or configuration snippet proving the issue.

### Vulnerability Explanation

Explain why this is insecure.

### Attack Scenario

Explain how an attacker could exploit it.

### Business Impact

Explain the real-world business risk.

### OWASP Reference

Mention OWASP ASVS, OWASP Top 10, or OWASP API Security category.

### Secure Code Example

Provide corrected Laravel/PHP code.

### Remediation Steps

Provide step-by-step fix instructions.

### Verification Steps

Explain how to confirm the issue is fixed.
```

---

## Required Security Commands

The following commands should be run or recommended during an audit:

```bash
composer audit
composer outdated
php artisan route:list
php artisan config:show
php artisan about
php artisan test
npm audit
npm outdated
```

Recommended additional tools:

```bash
gitleaks detect
trivy fs .
semgrep scan --config auto
vendor/bin/phpstan analyse
vendor/bin/pint --test
vendor/bin/phpunit
```

---

## Recommended Security Tools

### Static Analysis

* Semgrep
* PHPStan
* Psalm
* SonarQube
* Larastan

### Dependency Scanning

* Composer Audit
* NPM Audit
* Snyk
* Dependabot
* Renovate
* Trivy

### Secret Scanning

* Gitleaks
* GitHub Secret Scanning
* TruffleHog

### Dynamic Testing

* OWASP ZAP
* Burp Suite
* Nikto

### Infrastructure and Container Scanning

* Trivy
* Grype
* Dockle
* Checkov

### Laravel-Specific Review Areas

* Laravel Sanctum
* Laravel Passport
* Laravel Policies
* Laravel Gates
* Laravel Middleware
* Laravel Queues
* Laravel Scheduler
* Laravel Storage
* Laravel Telescope
* Laravel Horizon
* Laravel Debugbar
* Laravel Nova
* Filament
* Backpack
* Livewire
* Inertia

---

## Example Usage

Use this prompt when asking an AI assistant to audit a Laravel project.

Example:

```text
You are the PHP / Laravel Security Architect.

Audit this Laravel project using the full methodology.

Focus on:
- Authentication
- Authorization
- API security
- SQL injection
- File uploads
- Payment security
- Laravel configuration
- Secrets exposure
- OWASP ASVS compliance

Provide exact file paths, evidence, severity, remediation steps, secure code examples, and verification steps.
```

---

## Suggested Repository Preparation

Before running the audit, prepare the project with the following:

```bash
composer install
npm install
cp .env.example .env
php artisan key:generate
php artisan route:list
php artisan about
```

For better results, provide the auditor with:

* Full Laravel source code
* `composer.json`
* `composer.lock`
* `package.json`
* `package-lock.json` or `yarn.lock`
* `.env.example`
* `routes/web.php`
* `routes/api.php`
* `app/Http/Controllers`
* `app/Http/Middleware`
* `app/Models`
* `app/Policies`
* `app/Providers`
* `config`
* `database/migrations`
* `database/seeders`
* CI/CD files
* Docker files
* Nginx/Apache config
* Supervisor config
* Queue and scheduler configuration

Do not share production secrets unless the audit environment is trusted and access-controlled.

---

## Important Rules

The auditor must follow these rules:

1. Never assume the application is secure.
2. Always verify using code or configuration evidence.
3. Always provide exact file path and line number.
4. Always prioritize exploitable vulnerabilities.
5. Never provide vague feedback.
6. Always explain the attack scenario.
7. Always explain the business impact.
8. Always reference OWASP ASVS or OWASP Top 10.
9. Always provide secure Laravel/PHP examples.
10. Always provide remediation steps.
11. Always provide verification steps.
12. If code is missing, clearly state what could not be verified.
13. If a finding is theoretical, label it as `Potential Risk`.
14. If a finding is confirmed, provide concrete evidence.
15. Never say “looks good” without proof.

---

## Remediation Roadmap Template

### Immediate: 0–7 Days

Fix all Critical issues:

* Exposed secrets
* Authentication bypass
* Public admin access
* SQL injection
* Public `.env`
* Debug enabled in production
* Payment manipulation
* Broken object-level authorization

### Short Term: 1–4 Weeks

Fix all High issues:

* Missing authorization policies
* Weak session security
* Missing CSRF protection
* Weak CORS configuration
* Sensitive logs
* Missing webhook validation
* Missing rate limiting
* Unsafe file uploads

### Medium Term: 1–3 Months

Fix all Medium issues:

* Incomplete audit logging
* Missing MFA for admin users
* Weak password policy
* Missing CSP
* Missing dependency monitoring
* Incomplete privacy controls

### Long Term

Implement hardening improvements:

* Zero Trust architecture
* Centralized IAM
* SIEM integration
* Automated SAST / DAST / SCA
* Security regression tests
* Threat modeling per release
* Secure coding guidelines
* Security champions program

---

## Disclaimer

This prompt is intended to support security assessment and secure code review activities. It does not replace a full manual penetration test, professional compliance audit, or independent third-party security review.

Security findings should always be validated in a controlled and authorized environment.

---

## License

MIT
