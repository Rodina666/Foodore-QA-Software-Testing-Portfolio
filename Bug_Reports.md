# Sample Defect Reports (Demonstration Only)

### BUG-001: Registration accepts email format missing TLD domain
* **Severity:** Major | **Priority:** High | **Status:** Open
* **Preconditions:** User on Registration page (`/register`).
* **Steps to Reproduce:**
  1. Input Name "Fatma Sayed".
  2. Input Email `fatma.qa@domain` (Missing `.com`).
  3. Enter valid password and submit.
* **Expected Result:** Blocked with error: "Please enter a valid email address."
* **Actual Result:** Account creates successfully and redirects to dashboard.

---

### BUG-002: Cart subtotal fails to recalculate after rapid quantity increment
* **Severity:** Critical | **Priority:** High | **Status:** Open
* **Preconditions:** Cart contains 1x Pizza ($12.00).
* **Steps to Reproduce:**
  1. Click '+' icon 3 times rapidly.
* **Expected Result:** Quantity = 4, Total = $48.00.
* **Actual Result:** Quantity updates to 4, but total remains $12.00.

---

### BUG-003: Protected page `/orders` accessible via browser Back button post logout
* **Severity:** Critical | **Priority:** High | **Status:** Open
* **Steps to Reproduce:** Log in $\rightarrow$ Navigate to `/orders` $\rightarrow$ Logout $\rightarrow$ Press Browser 'Back'.
* **Expected Result:** Session destroyed; user redirected to `/login`.
* **Actual Result:** Renders cached user order history and address details.
