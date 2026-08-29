# Vafa Bank - Simple Banking Management System

An autonomous, client-side web application designed to simulate core real-world banking workflows across three operational roles: **Employees**, **Administrators**, and **Customers**. This project explores client-side routing, DOM manipulation, form validation, and relational transactional states handled entirely within the browser sandbox.

---

## 🚀 Key Features

*   **Role-Based Access Control (RBAC):** Common entry portal route-splitting into three distinct dashboards depending on explicit user credentials.
*   **Employee Module (Front-Desk Operator):** Captures customer KYC metadata via multi-field entry forms, creates non-repeating 14-digit Account Numbers, issues Customer IDs, and manages manual localized over-the-counter deposits and withdrawals.
*   **Admin Module (Back-Office Approver):** Features a live queues dashboard tracking pending registrations, a manual trigger to unlock profile activations, and an automated rule-based credential maker that couples the profile's ID with their Date of Birth.
*   **Customer Module (Self-Service Dashboard):** Comprehensive balance overview interface, full account summary cards, and a dual-entry ledger tracking instant balance transfers between active account nodes.
*   **Digi Passbook:** Live chronological transaction ledger computing absolute running balances following cross-account fund movements or manual physical ledger changes.

---

## 📂 File Architecture

The repository consists of modular decoupled views and centralized execution engines:

```text
├── index.html       # Shared login gateway & role router
├── admin.html       # Administrative approval interface & pending application queue
├── employee.html    # Customer onboarding dashboard & transactional desk 
├── customer.html    # Personalized customer dashboard & Digi Passbook statement
├── script.js        # Core client-side execution engine & localStorage logic
└── style.css        # Centralized theme layouts, component styles, and responsiveness
```

---

## 🛠️ Tech Stack & Hardware Baseline

### Software Layer
*   **Structure:** HTML5
*   **Styling & UI:** CSS3 (Featuring full layout grid alignment and fluid desktop responsiveness)
*   **Application Logic:** Modern JavaScript (ES6 Modules, Event Delegation, DOM Node Operations)
*   **Persistence Mocking:** Web Storage API (`window.localStorage`) for handling simulated cross-session records

### Hardware Specifications Used
*   **Host Environment:** Any modern browser running on Windows / macOS / Linux
*   **Host CPU:** Intel Core i3 or equivalent AMD architecture minimum
*   **Memory Allocations:** 4 GB RAM minimum with 10 GB internal disk space overhead

---

## 🔄 System Workflow & Process Topology

```text
                  ┌──────────────────────┐
                  │      Login Portal    │
                  └──────────┬───────────┘
                             │
            ┌────────────────┼────────────────┐
            ▼                ▼                ▼
     ┌────────────┐    ┌────────────┐   ┌────────────┐
     │  Employee  │    │   Admin    │   │  Customer  │
     └──────┬─────┘    └─────┬──────┘   └─────┬──────┘
            │                │                │
            ▼                ▼                ▼
     ┌────────────┐    ┌────────────┐   ┌────────────┐
     │ Open/Draft │───>│ Approve    │   │ Fund       │
     │ New Account│    │ Account    │   │ Transfers  │
     └────────────┘    └─────┬──────┘   └─────┬──────┘
                             │                │
                             ▼                ▼
                       ┌────────────┐   ┌────────────┐
                       │ Generate   │   │ Write Live │
                       │ Credentials│   │ Passbooks  │
                       └────────────┘   └────────────┘
```

1.  **Drafting Profiles:** The Employee records raw data inputs. The client-side logic assigns unique identification signatures and sets a pending flag attribute.
2.  **Back-Office Validation:** The Admin reviews the active registry arrays. Affirming a record updates its state flag from pending to active and saves their auto-generated passcodes into local storage arrays.
3.  **Active Transaction Loops:** Active customer logs unlock secure routing access. Initiating transfers calls safety checks to match balance availability with the recipient profile before updating both passbooks instantly.

---

## 🔮 Roadmap & Next Steps

*   **Server-Side Migration:** Replacing the browser's volatile `localStorage` runtime with a persistent web backend (Node.js/Express) combined with a structural transactional relational database (MySQL/MongoDB).
*   **Cryptographic Layer:** Moving away from plaintext client string storage to server-side token management, cryptographic password hashing (bcrypt), and Multi-Factor Authentication schemes.
*   **Advanced Features:** Building automated parsing modules to output downloadable, print-ready PDF statements and configuring multi-tiered analytics reports for administrators.

---

## 🎓 Contributor Credits

Developed as part of the Full Stack Java Programming Track at the **Lokmanya Tilak College of Engineering (An Autonomous Institute Affiliated to Mumbai University)**:

*   **Vansika Vipin Mishra** (AIMLB226)
*   **Ashutosh Anilkumar Pathak** (AIMLB235)
*   **Shaikh Abuzar Abdullah** (AIMLB246)
*   **Shaikh Mohd Faisal Shamshad** (AIMLB247)
