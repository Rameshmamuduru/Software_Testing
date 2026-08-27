**Functional + Validation + Boundary + Negative + UI + Security + Compatibility**

# Registration — Main Test Cases

## 1. Functional Testing

These verify that the registration functionality actually works.

| ID          | Test case                                                                     |
| ----------- | ----------------------------------------------------------------------------- |
| REG-FUN-001 | Verify user can navigate to the Registration page                             |
| REG-FUN-002 | Verify user can register successfully with valid mandatory details            |
| REG-FUN-003 | Verify user can register successfully with valid mandatory + optional details |
| REG-FUN-004 | Verify account is created after successful registration                       |
| REG-FUN-005 | Verify appropriate success/confirmation message is displayed                  |
| REG-FUN-006 | Verify user is redirected to the expected page after registration             |
| REG-FUN-007 | Verify newly registered user can log in with the registered credentials       |
| REG-FUN-008 | Verify email/OTP verification is triggered after registration, if applicable  |
| REG-FUN-009 | Verify user can complete registration after successful email/OTP verification |
| REG-FUN-010 | Verify Privacy Policy/Terms acceptance is handled correctly                   |

---

# 2. Validation Testing

These verify field-level rules.

| ID          | Test case                                                              |
| ----------- | ---------------------------------------------------------------------- |
| REG-VAL-001 | Verify mandatory fields cannot be left blank                           |
| REG-VAL-002 | Verify valid First Name is accepted                                    |
| REG-VAL-003 | Verify valid Last Name is accepted                                     |
| REG-VAL-004 | Verify valid email format is accepted                                  |
| REG-VAL-005 | Verify invalid email format is rejected                                |
| REG-VAL-006 | Verify valid phone number is accepted, if applicable                   |
| REG-VAL-007 | Verify invalid phone number is rejected                                |
| REG-VAL-008 | Verify valid password is accepted                                      |
| REG-VAL-009 | Verify password not meeting requirements is rejected                   |
| REG-VAL-010 | Verify Confirm Password must match Password                            |
| REG-VAL-011 | Verify leading/trailing spaces are handled according to requirements   |
| REG-VAL-012 | Verify invalid/special characters are handled according to field rules |

---

# 3. Boundary Value Testing

Use the **actual limits defined in the requirements**.

| ID          | Test case                                   |
| ----------- | ------------------------------------------- |
| REG-BVA-001 | Verify First Name at minimum allowed length |
| REG-BVA-002 | Verify First Name at maximum allowed length |
| REG-BVA-003 | Verify First Name beyond maximum length     |
| REG-BVA-004 | Verify Last Name at minimum allowed length  |
| REG-BVA-005 | Verify Last Name at maximum allowed length  |
| REG-BVA-006 | Verify Email at maximum supported length    |
| REG-BVA-007 | Verify Password at minimum allowed length   |
| REG-BVA-008 | Verify Password at maximum allowed length   |
| REG-BVA-009 | Verify Password beyond maximum length       |
| REG-BVA-010 | Verify Phone number below required length   |
| REG-BVA-011 | Verify Phone number at required length      |
| REG-BVA-012 | Verify Phone number above required length   |

For example, if the requirement says:

```text
Password = 8–20 characters
```

you test:

```text
7  → ❌
8  → ✅
20 → ✅
21 → ❌
```

---

# 4. Negative Testing

Here you're deliberately trying invalid/unexpected conditions.

| ID          | Test case                                                        |
| ----------- | ---------------------------------------------------------------- |
| REG-NEG-001 | Register with all mandatory fields blank                         |
| REG-NEG-002 | Register with one mandatory field blank                          |
| REG-NEG-003 | Register with invalid First Name                                 |
| REG-NEG-004 | Register with invalid Last Name                                  |
| REG-NEG-005 | Register with invalid email                                      |
| REG-NEG-006 | Register with invalid phone number                               |
| REG-NEG-007 | Register with invalid/weak password                              |
| REG-NEG-008 | Register with mismatched Password and Confirm Password           |
| REG-NEG-009 | Register using an already registered email                       |
| REG-NEG-010 | Register without accepting mandatory Privacy Policy              |
| REG-NEG-011 | Submit registration with incomplete information                  |
| REG-NEG-012 | Verify registration behavior when the registration service fails |
| REG-NEG-013 | Verify registration behavior when email/OTP service fails        |

---

# 5. UI Testing

These verify the registration interface itself.

| ID         | Test case                                                         |
| ---------- | ----------------------------------------------------------------- |
| REG-UI-001 | Verify Registration page layout                                   |
| REG-UI-002 | Verify all required fields are displayed                          |
| REG-UI-003 | Verify field labels and placeholders                              |
| REG-UI-004 | Verify mandatory fields are clearly indicated                     |
| REG-UI-005 | Verify Password field is masked                                   |
| REG-UI-006 | Verify Show/Hide Password works, if available                     |
| REG-UI-007 | Verify Register button is displayed and usable                    |
| REG-UI-008 | Verify validation messages are displayed correctly                |
| REG-UI-009 | Verify validation messages appear near the appropriate fields     |
| REG-UI-010 | Verify error messages disappear/update after correcting the input |
| REG-UI-011 | Verify Privacy Policy/Terms links work                            |
| REG-UI-012 | Verify Login link works                                           |
| REG-UI-013 | Verify tab order/navigation works correctly                       |
| REG-UI-014 | Verify page doesn't break when validation errors are displayed    |

---

# 6. Security Testing

These are **basic security checks appropriate for QA**. Deep penetration testing would normally be handled by a security/AppSec team.

| ID          | Test case                                                                          |
| ----------- | ---------------------------------------------------------------------------------- |
| REG-SEC-001 | Verify password is not displayed in plain text                                     |
| REG-SEC-002 | Verify password is not exposed in the URL                                          |
| REG-SEC-003 | Verify sensitive information is not exposed in error messages                      |
| REG-SEC-004 | Verify registration input handles basic XSS attempts safely                        |
| REG-SEC-005 | Verify registration input handles injection attempts safely                        |
| REG-SEC-006 | Verify duplicate registration/account enumeration behavior is secure               |
| REG-SEC-007 | Verify registration endpoint has appropriate rate limiting/abuse protection        |
| REG-SEC-008 | Verify user cannot manipulate registration data to obtain an unauthorized role     |
| REG-SEC-009 | Verify verification/OTP cannot be reused after successful verification             |
| REG-SEC-010 | Verify expired verification/OTP cannot be used                                     |
| REG-SEC-011 | Verify sensitive information is not unnecessarily exposed in API/browser responses |
| REG-SEC-012 | Verify registration uses HTTPS                                                     |

---

# 7. Compatibility Testing

Test against the **browser/device matrix supported by your project**.

| ID           | Test case                                                        |
| ------------ | ---------------------------------------------------------------- |
| REG-COMP-001 | Verify registration works in Chrome                              |
| REG-COMP-002 | Verify registration works in Edge                                |
| REG-COMP-003 | Verify registration works in Firefox                             |
| REG-COMP-004 | Verify registration works in Safari, if supported                |
| REG-COMP-005 | Verify registration works on supported Android devices/browsers  |
| REG-COMP-006 | Verify registration works on supported iOS devices/browsers      |
| REG-COMP-007 | Verify registration page is responsive on supported screen sizes |
| REG-COMP-008 | Verify registration works under supported network conditions     |

---

# Final Registration Test Suite

So if you are the **UI QA owner for Registration**, your overall structure can be:

```text
REGISTRATION
│
├── Functional
│   ├── Successful registration
│   ├── Account creation
│   ├── Verification
│   ├── Confirmation
│   └── Post-registration login
│
├── Validation
│   ├── Mandatory fields
│   ├── Email
│   ├── Phone
│   ├── Password
│   └── Name fields
│
├── Boundary
│   ├── Minimum values
│   ├── Maximum values
│   └── Out-of-range values
│
├── Negative
│   ├── Missing data
│   ├── Invalid data
│   ├── Duplicate account
│   └── Service failures
│
├── UI
│   ├── Layout
│   ├── Fields
│   ├── Buttons
│   ├── Messages
│   └── Navigation
│
├── Security
│   ├── Password protection
│   ├── XSS/injection
│   ├── Enumeration
│   ├── Rate limiting
│   ├── Role manipulation
│   └── Sensitive data
│
└── Compatibility
    ├── Browsers
    ├── Devices
    └── Screen sizes
```
