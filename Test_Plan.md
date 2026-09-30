# QA Test Plan – Foodore Web Application

## 1. Test Objectives
- Verify 100% functional requirement coverage via RTM.
- Validate shopping cart math, delivery fee dynamics, and promo discount logic.
- Ensure proper system defensive behavior against invalid inputs and unauthorized route navigation.

## 2. Project Scope

### In Scope:
- **Authentication:** Registration, Email Validation, Password Policy, Login, Logout, Session Persistence.
- **Discovery:** Restaurant Listing, Keyword Search, Cuisine Filtering, Menu Details.
- **Cart & Checkout:** Add/Remove Items, Quantity Adjustments, Promo Codes, Address Management, Order Creation (COD).
- **Non-Functional:** Cross-Device Responsive Layouts, Postman REST API Testing, Basic Session Security Checks.

### Out of Scope:
- Real payment gateway transactions.
- Physical delivery driver live GPS tracking.
- Production-grade security penetration testing.
- Load, stress, and performance testing.

## 3. Test Types & Execution Approach
- **Functional Testing:** Acceptance criteria verification.
- **Negative & Boundary Testing:** Input validation, BVA, and Equivalence Partitioning.
- **UI/Responsive Testing:** Desktop (1920x1080), Tablet (768x1024), Mobile (375x812).
- **API Testing:** REST requests using Postman.
- **Regression Testing:** Re-verifying primary core paths post bug fixes.

## 4. Entry & Exit Criteria
- **Entry Criteria:** Complete requirement specifications and QA Test Plan sign-off.
- **Exit Criteria:** 100% test scenario execution with zero open Critical/High severity bugs.
