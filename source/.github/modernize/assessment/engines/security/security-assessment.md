# Security Assessment Report

**Generated:** 2026-06-22 10:20:06 UTC

## Summary

| Metric | Count |
|--------|-------|
| Total Findings | 11 |
| CVE Vulnerabilities | 6 |
| CWE Vulnerabilities | 5 |
| Total Rules Assessed | 59 |
| Rules Passed | 54 |

### By Severity

| Severity | Count |
|----------|-------|
| mandatory | 7 |
| optional | 1 |
| potential | 3 |

### By Category

| Category | Count |
|----------|-------|| Code Quality | 2 |
| File & Path Security | 1 |
| CVE | 6 |
| Credentials & Secrets | 2 |

## CVE Findings (Dependency Vulnerabilities)
### CVE-2026-32933: AutoMapper Vulnerable to Denial of Service (DoS) via Uncontrolled Recursion
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:6, SocialGoal.Tests/packages.config:3, SocialGoal.Web.Core/packages.config:3

[CVE-2026-32933](https://github.com/advisories/GHSA-rvv3-g6hj-g44x): AutoMapper Vulnerable to Denial of Service (DoS) via Uncontrolled Recursion

Severity: HIGH

Affected dependencies:
  - AutoMapper:3.1.1-ci1000 (declared at SocialGoal/packages.config:6)
  - AutoMapper:3.1.1-ci1000 (declared at SocialGoal.Tests/packages.config:3)
  - AutoMapper:3.1.1-ci1000 (declared at SocialGoal.Web.Core/packages.config:3)

Recommended fix:
  - Upgrade AutoMapper to 15.1.1 or later
### CVE-2023-33170: Microsoft Security Advisory CVE-2023-33170: .NET Security Feature Bypass Vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:15

[CVE-2023-33170](https://github.com/advisories/GHSA-25c8-p796-jg6r): Microsoft Security Advisory CVE-2023-33170 - .NET Security Feature Bypass Vulnerability

Severity: HIGH

Affected dependencies:
  - Microsoft.AspNet.Identity.Owin:1.0.0 (declared at SocialGoal/packages.config:15)

Recommended fix:
  - Upgrade Microsoft.AspNet.Identity.Owin to 2.2.4 or later
### CVE-2022-29117: .NET Denial of Service Vulnerability
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:24, SocialGoal/packages.config:21, SocialGoal.Tests/packages.config:7

[CVE-2022-29117](https://github.com/advisories/GHSA-3rq8-h3gj-r5c6): .NET Denial of Service Vulnerability

Severity: HIGH

Affected dependencies:
  - Microsoft.Owin.Security.Cookies:2.0.0 (declared at SocialGoal/packages.config:24)
  - Microsoft.Owin:2.0.0 (declared at SocialGoal/packages.config:21)
  - Microsoft.Owin:2.0.0 (declared at SocialGoal.Tests/packages.config:7)

Recommended fix:
  - Upgrade Microsoft.Owin.Security.Cookies to 4.2.2 or later
  - Upgrade Microsoft.Owin to 4.2.2 or later
### CVE-2020-1045: Cookie parsing failure in Microsoft.Owin
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:21, SocialGoal.Tests/packages.config:7

[CVE-2020-1045](https://github.com/advisories/GHSA-hxrm-9w7p-39cc): Cookie parsing failure in Microsoft.Owin

Severity: HIGH

Affected dependencies:
  - Microsoft.Owin:2.0.0 (declared at SocialGoal/packages.config:21)
  - Microsoft.Owin:2.0.0 (declared at SocialGoal.Tests/packages.config:7)

Recommended fix:
  - Upgrade Microsoft.Owin to 4.1.1 or later
### CVE-2021-21252: Regular Expression Denial of Service in jquery-validation
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:12

[CVE-2021-21252](https://github.com/advisories/GHSA-jxwx-85vp-gvwm): Regular Expression Denial of Service in jquery-validation

Severity: HIGH

Affected dependencies:
  - jQuery.Validation:1.11.1 (declared at SocialGoal/packages.config:12)

Recommended fix:
  - Upgrade jQuery.Validation to 1.19.3 or later
### CVE-2024-21907: Improper Handling of Exceptional Conditions in Newtonsoft.Json
- **Severity:** mandatory
- **Story Points:** 1
- **Files:** SocialGoal/packages.config:33

[CVE-2024-21907](https://github.com/advisories/GHSA-5crp-9r3c-p9vr): Improper Handling of Exceptional Conditions in Newtonsoft.Json

Severity: HIGH

Affected dependencies:
  - Newtonsoft.Json:5.0.6 (declared at SocialGoal/packages.config:33)

Recommended fix:
  - Upgrade Newtonsoft.Json to 13.0.1 or later

## CWE Findings (Code-Level Vulnerabilities)
### CWE-772: Missing Release of Resource after Effective Lifetime
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 3
- **Files:** SocialGoal/Controllers/AccountController.cs

In AccountController.cs, the UploadProfilePic action (lines 400-433) creates Bitmap objects (original at line 400/414, img at line 420) that implement IDisposable but are never disposed via using statements or explicit Dispose() calls. GDI+ resources held by Bitmap objects are not released, causing resource leaks.
### CWE-775: Missing Release of File Descriptor or Handle after Effective Lifetime
- **Category:** Code Quality
- **Severity:** potential
- **Story Points:** 3
- **Files:** SocialGoal/Controllers/AccountController.cs

In AccountController.cs, Bitmap objects (which internally hold GDI+ file handles) created via Bitmap.FromStream (line 414) and new Bitmap (line 499 in CreateImage) are not wrapped in using blocks or explicitly disposed, leaking unmanaged GDI handles.
### CWE-732: Incorrect Permission Assignment for Critical Resource
- **Category:** Credentials & Secrets
- **Severity:** optional
- **Story Points:** 5
- **Files:** SocialGoal/Web.config

In Web.config (line 24), ELMAH error logging is configured with 'elmah.mvc.requiresAuthentication=false' and 'elmah.mvc.allowedRoles=*', allowing unauthenticated users to access the /elmah error log endpoint. This exposes sensitive stack traces, database connection details, and internal application errors to any visitor.
### CWE-778: Insufficient Logging
- **Category:** Credentials & Secrets
- **Severity:** potential
- **Story Points:** 3
- **Files:** SocialGoal/Controllers/AccountController.cs

No logging framework (ILogger, log4net, NLog, Serilog, etc.) is used anywhere in the application. Security-critical events such as failed login attempts, password changes, profile picture uploads, and account registration are not logged. AccountController handles all authentication events without any security event logging.
### CWE-434: Unrestricted Upload of File with Dangerous Type
- **Category:** File & Path Security
- **Severity:** mandatory
- **Story Points:** 8
- **Files:** SocialGoal/Controllers/AccountController.cs

In AccountController.cs, the UploadProfilePic action (around lines 410-430) accepts a file upload via model.File (HttpPostedFileBase) without validating the file content type or extension. The uploaded file's input stream is directly passed to Bitmap.FromStream() without any MIME type or extension whitelist check, allowing any file type to be submitted and processed as an image.

