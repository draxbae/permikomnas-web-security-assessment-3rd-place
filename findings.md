# Sanitized Security Findings

This document summarizes selected security findings identified and validated during the **PERMIKOMNAS RI Bug Bounty Competition**.

All information has been sanitized for portfolio and educational purposes.

Sensitive target URLs, IP addresses, credentials, personal information, and detailed exploitation steps have been intentionally excluded.

---

## 1. Insecure Direct Object Reference (IDOR)

**Severity:** High
**Category:** Broken Access Control

### Description

An Insecure Direct Object Reference (IDOR) issue was identified in several application functions involving object references.

During validation, changing an object identifier resulted in a response for another object without sufficient server-side authorization enforcement.

### Impact

This type of vulnerability could potentially allow an unauthorized user to access resources belonging to another user or entity.

The potential impact depends on the type and sensitivity of the affected resources.

### Recommendation

Implement server-side authorization checks for every request involving object references.

The application should verify that the authenticated user is authorized to access the requested object before returning or modifying its data.

---

## 2. HTTP 507 Insufficient Storage

**Severity:** Medium
**Category:** Availability / Resource Handling

### Description

The application returned an HTTP `507 Insufficient Storage` response during testing of a specific application function.

This behavior indicated a potential issue related to server-side resource or storage handling.

### Impact

Unexpected resource exhaustion or insufficient storage conditions may affect application availability and could potentially prevent legitimate requests from being processed normally.

### Recommendation

Recommended measures include:

* Monitor storage utilization
* Implement appropriate resource limits
* Monitor application and server logs
* Establish capacity management procedures
* Investigate conditions that trigger HTTP 507 responses
* Ensure appropriate handling of resource exhaustion

---

## 3. `.env` File Existence Disclosure

**Severity:** Medium
**Category:** Information Disclosure

### Description

Testing identified a difference in the application's HTTP response behavior when requesting a `.env` file compared with a random non-existent path.

The `.env` request returned an HTTP `403 Forbidden` response, while a non-existent path returned `404 Not Found`.

Although the contents of the `.env` file were not accessible, the difference in responses could disclose information about the existence of the file.

### Impact

Information about the presence of configuration files may provide useful reconnaissance information to an attacker.

The risk could become more significant if access controls are incorrectly configured in the future and sensitive configuration contents become accessible.

### Recommendation

Recommended measures include:

* Store environment configuration files outside the web-accessible directory
* Explicitly deny access to sensitive configuration files
* Review web server access-control rules
* Ensure sensitive configuration files cannot be downloaded

---

## 4. Directory Listing Enabled

**Severity:** Medium
**Category:** Security Misconfiguration
**CWE:** CWE-548 — Information Exposure Through Directory Listing

### Description

Directory listing functionality was identified on an application asset directory.

The directory allowed accessible resources such as JavaScript, CSS, and image assets to be enumerated.

### Impact

Directory listing can expose information about application resources and file structure.

Exposed filenames and client-side assets may provide useful information for further reconnaissance and security analysis.

### Recommendation

Disable directory listing for directories that do not require it.

For Apache-based environments, directory indexing can generally be disabled using appropriate server configuration such as:

```apache
Options -Indexes
```

Additional recommendations:

* Remove unnecessary files from web-accessible directories
* Review exposed client-side assets
* Avoid leaving obsolete or development files on production systems
* Apply appropriate access controls to sensitive resources

---

## Responsible Disclosure & Scope

These findings were identified during an authorized assessment conducted as part of the **PERMIKOMNAS RI Bug Bounty Competition**.

Testing was performed within the competition's defined scope and rules of engagement.

The original reports contained sensitive information that has intentionally been removed from this portfolio version.

---

## Sanitization Notice

This document does not contain:

* Sensitive target URLs
* IP addresses
* Credentials
* Participant contact information
* Raw competition reports
* Detailed exploitation instructions
* Sensitive proof-of-concept information

The purpose of this document is to demonstrate practical experience in vulnerability identification, validation, impact assessment, and security reporting.
