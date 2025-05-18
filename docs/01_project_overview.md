# Reservation Widget SaaS – Project Overview

## 1. Project Goals
- A lightweight, secure, and modular reservation widget embeddable via a single script line.
- Designed for easy integration into various client websites.

---

## 2. High-Level Architecture

- **Widget Frontend:** Vanilla JS/React widget, loads via script tag, injects reservation UI into host page.
- **Backend API:** REST/GraphQL API for business logic, user management, and reservations.
- **Database:** Stores reservations, availability, user accounts, clients.
- **Admin/Management Portal:** Interface for clients to configure widget, manage reservations, view analytics.
- **Utilities/Services:** Shared logic (e.g., validation, email, logging) in dedicated modules.

---

## 3. Project Structure (Reference)

```
/docs                  # Documentation, roadmap, architecture
/frontend-widget       # Widget code (JS/React, embeddable)
  /src
/backend-api           # Backend (Node.js/Express, Python/FastAPI, etc.)
  /src
/admin-portal          # (optional, separate from widget)
  /src
/utils                 # Shared utilities, helpers
/scripts               # Deployment, automation, test scripts
/tests                 # Automated tests
```

---

## 4. Implementation Roadmap

### Step 1: Bootstrapping
- Setup project structure and tooling (linters, formatter, testing, CI/CD basics).

### Step 2: Widget MVP
- Basic embeddable widget skeleton (JS snippet, simple UI placeholder).
- Script loads remotely, injects a <div>, renders a button.

### Step 3: Backend MVP
- Set up backend API (choose stack: Node, Python, etc.).
- Implement endpoints for reservation CRUD, availability check.

### Step 4: Widget-API Integration
- Widget connects to API, submits/reads reservation data.

### Step 5: Core Utilities
- Modular utility functions (validation, logging, error handling).

### Step 6: Security & Embedding
- CSRF, CORS, sanitization, API keys/tokens.
- Ensure widget isolation (CSS encapsulation, XSS protection).

### Step 7: Admin Portal (Optional/Phase 2)
- Interface for business clients (see reservations, custom config).

### Step 8: Testing & Docs
- Unit and integration tests.
- Expand documentation.

### Step 9: Productionization
- CI/CD pipelines, monitoring, error reporting.

---

## 5. Coding and Security Best Practices

- **Keep files <200 lines:** Split logic into focused modules/files.
- **Modular Design:** Use pure functions, clear interfaces, reusable components.
- **Reusable Utilities:** Keep helpers and services DRY and separated.
- **Security:** Sanitize all inputs, use HTTPS, secure backend APIs, limit scopes, protect secrets.
- **Efficiency:** Optimize for performance (widget load time, minimal API responses).
- **Maintainability:** Write clear docs, strong typing, code reviews.

---

## 6. Reference/Summary Docs

- This and all further docs will be kept updated as the project evolves.
- See `/docs` for architecture, `/utils` for shared code, `/tests` for test coverage.

---

## 7. Next Steps

> We will now proceed to set up the project directory structure and the basic widget loader script.