---
created: 2026-07-03T08:00:28+06:30
modified: 2026-07-03T08:00:57+06:30
---

# EWA app flow

Here is the complete, regenerated feature specification document in **Markdown** format. It consolidates all previous sections (Authentication, Onboarding, Verification Logic, Disbursement, Dashboard, History, and MoMoney Phase 1 specific requirements) into one structured document.

---

# EWA Mobile Application - Complete Feature Specification Document

## 1. Authentication & Security Module
- **Sign Up (Registration)**
  - **Input:** User enters Mobile Phone Number.
  - **Verification:** System sends an OTP (One-Time Password) via SMS.
  - **Credential Setup:** Upon successful OTP validation, user creates a secure login password.
- **Login**
  - **Method:** Phone Number + Password.
  - **Security Enhancement (Optional):** Implement biometric login (Fingerprint/Face ID) after initial login for easier access.
- **Forgot Password**
  - **Flow:** User enters Phone Number → System sends OTP → User enters OTP → User creates a new Password.
- **Change Password**
  - **Flow:** User must enter current App PIN/Password → System sends OTP to registered phone → User enters OTP → User sets new Password.

## 2. Onboarding (KYC & KYE)
- **KYC - Know Your Customer (User Info)**
  - **Fields:** Full Name, Date of Birth, National Registration Card (NRC) number, Address, and optional Selfie/Live Photo for facial verification.
- **KYE - Know Your Employee (Employment Details)**
  - **Fields:** Company Name, Company Registration Number (if known), Employee ID, Department, Job Title.
  - **Data Matching:** The system uses the **Phone Number** and the **NRC Number** entered during KYC to cross-reference against the Company's uploaded **"Employee Verification List"**.

## 3. Employment Verification Engine (Smart Routing)
The system detects the relationship between the user, their phone, their NRC, and the company database. It routes the user through different flows:

- **Flow A: Direct Access (Auto-Verified)**
  - *Condition:* Company exists in the database **AND** the Phone + NRC match a record in the Company's uploaded Employee Verification List.
  - *Action:* User bypasses all approval queues and goes straight to the **Home Screen Dashboard**.
- **Flow B: Company Registration Request**
  - *Condition:* The Company does **not** yet exist in the App's database.
  - *Action:* User is prompted to fill a **"Company Request Form"** containing: **Company Name**, **Contact Person Name**, and **Contact Person Email/Phone**.
  - *Result:* This request is sent to the System Admin to register the new company.
- **Flow C: Employee Verification Request (Missing from List)**
  - *Condition:* Company already exists in database, BUT the user's Phone/NRC is **not** on the Company's Employee Verification List.
  - *Action:* User clicks "Request Access".
  - *Result:* This request is routed to the **Company Portal** (a separate web admin dashboard). The HR/Admin can view the request and **Approve or Reject it**, attaching a mandatory "Reason" if rejected.

## 4. EWA Eligibility & Disbursement Logic
Once the employment status is verified, the eligibility engine evaluates the user:

- **Scenario 1: EWA Eligible (Auto-Granted)**
  - *Action:* The **"Request Advance"** button is active. User can specify the amount (up to the displayed limit).
  - *Result:* The request triggers automatic **Disbursement** to the user's preferred payment method on schedule.
- **Scenario 2: EWA Not Eligible (Soft/Provisionary)**
  - *Action:* User sees a "Request EWA Eligibility" button.
  - *Result:* This request is routed to the **Company Portal**.
- **The Whitelist Trust & Budget Approval Process**
  - **Step 1 (Company):** Company Admin reviews the request on their portal and grants approval (Whitelisting the user).
  - **Step 2 (App Admin/Budget):** Following company approval, the request goes to the **Super Admin** for **Budget Approval** (to ensure the company has sufficient funds in their settlement account).
  - **Step 3 (Disbursement):** Once the Super Admin gives the final Budget Approval, **Disbursement is executed** to the user's bank/mobile wallet.

## 5. Dashboard / Home Screen Features
The home screen provides a clear, real-time snapshot of the user's financial status:
- **Header:** Personalized greeting ("Welcome back, [User Name]"). Quick access to notifications and profile.
- **Available Balance Card:** Shows the large prominent "Available Balance", the "Limit", and the amount currently "Used" (e.g., $800).
- **Usage Progress Bar:** A visual bar indicating how much of their daily/weekly wage limit has been utilized.
- **Primary Call-to-Action (CTA):** Large purple **"Request Advance"** button for initiating a withdrawal.
- **User Stats Module:**
  - **Advances:** Total number of advances taken.
  - **Completed:** Successfully paid off advances.
  - **Pending:** Advances awaiting disbursement or repayment.
- **Recent Transactions List:** Reverse-chronological list of recent financial activities showing amounts, dates, and status tags (e.g., "Requested", "Disbursed").
- **Bottom Navigation Bar:**
  - **Home:** Returns to the dashboard.
  - **History:** Displays full transaction and request history.
  - **Profile:** Manages personal details, bank account linked, security settings, and support.

## 6. Additional Features (Extrapolated)
- **Transaction History & E-Slips:** Detailed view of past advances, repayment dates, and downloadable digital receipts.
- **Repayment/Recurring Deduction Scheduler:** Automated setting to show upcoming payroll deductions to settle the advance.
- **In-App Notifications:** Real-time push notifications for Company approvals/rejections, Admin approvals, Disbursement confirmations, and upcoming repayment alerts.
- **Multi-Method Withdrawal:** Options to withdraw to local bank accounts, e-wallets, or physical payout points (phase planned).
- **Financial Health Tools (Optional Premium):** Budget calculators, financial wellness articles, or expense tracking.
- **Support & Help Center:** FAQ section, live chat support, and direct phone support integrated into the "Profile" tab.
- **Security Settings:** App lock (PIN/Fingerprint), device management, and active session control.

## 7. History & Transaction Module (Expanded Spec)
The **History** tab serves as a comprehensive financial ledger tracking every single monetary and service interaction within the app.

### A. Transaction Categories (Data Types)
The history list must explicitly classify the following types of items:
- **Disbursements (Inflows):** Actual funds transferred to the user (e.g., "Advance Payout", "Bonus Adjustment").
- **Repayments (Outflows):** Deductions of funds from the user's salary or manual repayments (e.g., "Payroll Deduction", "Manual Repayment").
- **Services / Fees (Transactions):** Processing fees, instant transfer fees, or late payment penalties (e.g., "EWA Processing Fee").
- *(Note: Pending Requests that haven't been funded should also be included here but marked with a distinct status).*

### B. Transaction Details (Deep-Dive View)
When a user taps on any history row, it should open a **"Transaction Details"** drawer/page containing:
- **Reference / Transaction ID:** A unique alphanumeric ID for traceability.
- **Date & Timestamp:** Exact date and time the transaction was recorded.
- **Transaction Type:** Explicitly labeled (`Disbursement`, `Repayment`, `Service Fee`).
- **Amount:** The exact monetary value, including fees if applicable.
- **Status:** `Success`, `Pending`, `Failed`, `Cancelled`.
- **Payment Method:** Bank account name/number or Mobile Wallet used (masked for security).
- **Related Advance ID:** *Crucial for repayment transparency.* If it is a repayment, it must state which Advance Request ID it belongs to.
- **Balance After Transaction:** Shows the remaining available EWA balance immediately after this transaction.
- **Digital Receipt:** Option to download the transaction as a PDF/E-receipt.

### C. Filtering & Sorting ("Base on type of History")
To address the "base on type of History" requirement, the module must include:
1.  **Tabbed Filters (Top of screen):** 
    - `All` (Shows every transaction)
    - `Disbursements`
    - `Repayments`
    - `Fees & Services`
2.  **Advanced Search/Dropdown Filters:**
    - **Date Range:** Custom date picker (This week, This month, Custom range).
    - **Status:** Filter by `Success`, `Pending`, `Failed`.
3.  **Sorting Options:**
    - *Newest First* (Default)
    - *Oldest First*
    - *Amount (Highest to Lowest)*
    - *Amount (Lowest to Highest)*

### D. UI/UX Implementation
- **Color-Coded Icons & Arrows:**
  - 🟢 **Green arrow pointing down** for **Disbursements** (Money entering).
  - 🔴 **Red arrow pointing up** for **Repayments** (Money leaving).
  - 🟠 **Orange tag/gem** for **Service/Fees**.
- **Status Badges:** Distinct chip colors (e.g., Light Green for "Success", Light Yellow for "Pending").
- **Search Bar:** A global search bar to allow users to search by Amount, Date, or Reference ID.

## 8. Disbursement Channel Selection (Request Advance Flow)
This feature defines the user's choice of receiving funds when requesting an advance.

### A. Phase 1 Constraint (Scope)
- **Current State:** In Phase 1 of the rollout, **only "MoMoney Wallet"** is supported as the disbursement channel.
- **Future State:** Phase 2 will introduce Bank Account transfers (with auto-filled IBAN/Account Numbers), and other local e-wallets.

### B. Linking the Wallet (Pre-requisite)
Before a user can request an advance, the system must ensure they have a linked payout destination.
- **Location:** The "Profile" → "Payment Methods" or "Wallet Settings" menu.
- **MoMoney Linking Flow:**
  - User selects "Add MoMoney Wallet".
  - User enters their MoMoney registered Mobile Number.
  - **Verification (Optional but recommended):** System sends an OTP to that MoMoney number to verify ownership. 
  - Once verified, the MoMoney number is saved as the user's primary payout wallet.
- **Validation:** If a user tries to click "Request Advance" without adding a MoMoney wallet, the system intercepts them with a prompt: *"Please add your MoMoney Wallet in the Profile section before requesting an advance."*

### C. Request Advance UI Integration
When the user clicks the purple **"Request Advance"** button on the Home Screen:
1.  **Amount Input:** Display the standard numeric keypad or slider to enter the desired advance amount (capped at the "Available Balance" limit).
2.  **Channel Selection Section:** Below the amount, include a dedicated row labeled:
    - `Select Channel to Receive:`
    - **UI Element:** Because there is only one option, use a **disabled drop-down** or a **statically selected radio button** (highlighted in purple) with the text: `MoMoney Wallet`.
    - **Readability:** Display the linked MoMoney phone number right next to it, e.g., `MoMoney Wallet (09-XXX-XXXX)` to confirm the destination for the user.
3.  **Review Summary:** On the final confirmation screen, explicitly show:
    - *Advance Amount:* $XXX
    - *Service Fee:* $X.XX (if applicable)
    - *Total to Receive:* $XXX
    - *Payout Channel:* MoMoney Wallet (09-XXX-XXXX)

### D. Backend & Disbursement Logic
- **Payload:** When the user submits the request, the `POST /api/request-advance` API payload must include the `payoutChannel` field explicitly set to `"MoMoney_Wallet"` alongside the linked `walletPhoneNumber`.
- **Approval Routing:** The request goes through the Company Portal and Admin Budget Approval queues.
- **Disbursement Execution:**
  - Once final approval is given, the backend system picks up the approved request.
  - It calls the **MoMoney Payment Gateway API**.
  - It pushes the exact approved amount to the verified MoMoney phone number.
- **Status Updates:** Immediately upon executing the API call, the system updates the transaction:
  - `Status`: "Disbursed" (or "Pending" if the API takes a few seconds).
  - **History Log:** This transaction is recorded in the History tab with the `Type: Disbursement`, `Channel: MoMoney Wallet`, and `Reference ID` from MoMoney.

### E. Error Handling for MoMoney Payouts
- **MoMoney API Down:** If the MoMoney gateway is offline, the system should place the request in a `Payout Queue` with a retry mechanism. The user sees `Status: Pending Disbursement` until the retry succeeds.
- **Invalid Number / Account Closed:** If the MoMoney API returns an error (e.g., "Wallet not found"), the system must halt the disbursement, mark the Advance Request as `Failed`, and instantly push an in-app notification: *"Disbursement failed. Please update your MoMoney wallet details in Profile and contact Support to retry the payout."*
