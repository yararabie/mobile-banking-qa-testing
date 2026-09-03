# Mobile Banking Application - QA Testing Portfolio

Manual QA testing project for a Mobile Banking web application, covering functional, negative, boundary, security, UI/UX, and business-logic testing across all core modules.

## 📋 Project Overview

This repository contains a complete manual testing cycle performed on a Mobile Banking Dashboard application, including:
- Test case design and execution
- Bug discovery, reproduction, and documentation
- Root-cause analysis linking related defects across modules

**Application modules tested:**
- 🔐 Login / Authentication
- 👤 User Management (Create, Search, List)
- 💳 Account Management (Create, Search, List)
- 💸 Transactions (Deposit, Withdrawal, Transfer, Payment)

## 📁 Repository Structure

```
├── test-cases/
│   └── Mobile_Banking_Test_Cases.xlsx   # All test cases (Login, Users, Accounts, Transactions)
├── bug-reports/
│   └── Mobile_Banking_Bug_Reports.xlsx  # Consolidated bug tracker with full reproduction steps
└── README.md
```

## 🧪 Testing Approach

Each module was tested across the following categories:
- **Positive testing** – valid inputs and expected happy-path flows
- **Negative testing** – invalid inputs, empty fields, boundary values
- **Security testing** – SQL Injection, XSS, session handling
- **Business logic validation** – account type rules, credit limit behavior, balance calculations
- **UI/UX testing** – keyboard navigation, responsive design, loading states
- **Boundary Value Analysis (BVA)** – min/max field lengths, numeric precision limits

## 🐞 Bug Summary

**50 bugs documented**, including:

| Severity | Count |
|---|---|
| Critical | 4 |
| High | 16 |
| Medium | 21 |
| Low | 9 |

**Notable findings:**
- Server crashes (HTTP 500) exposing internal database schema and backend implementation details
- User-entered unique identifiers (Account Number, Transaction Reference) silently ignored and overwritten by the system
- Credit Limit business logic not enforced during account creation or transaction validation
- Session not properly invalidated across browser tabs after logout
- Search functionality returning all records instead of empty results for non-matching queries

Each bug report includes: severity, priority, steps to reproduce, test data, expected vs. actual result, and business impact.

## 🛠️ Tools Used

- Manual testing (Chrome DevTools - Network, Console)
- Excel for test case documentation and bug tracking
- Postman-style API response inspection for backend error analysis

## 👤 About

QA / Software Testing portfolio project by **Yara Rabie** — showcasing manual testing skills including test case design, bug discovery, and defect documentation for a banking application.
