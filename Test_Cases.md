# Detailed Test Cases & Negative Scenarios

| Test Case ID | Module | Title | Priority | Preconditions | Test Steps | Expected Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-001** | Auth | Register with valid details | High | On Register Page | 1. Enter valid name & unique email<br>2. Enter strong password<br>3. Submit | Account registered successfully; redirected to home page. | Not Executed |
| **TC-002** | Auth | Register with duplicate email | High | Email exists | 1. Enter existing email<br>2. Submit | Registration rejected: "Email already registered." | Not Executed |
| **TC-004** | Auth | Login with valid credentials | High | Active user | 1. Enter valid email & password<br>2. Click Login | User logged in successfully; profile header displays. | Not Executed |
| **TC-005** | Auth | Login with wrong password | High | Active user | 1. Enter valid email & wrong pass<br>2. Click Login | Login rejected: "Invalid email or password." | Not Executed |
| **TC-008** | Auth | Protected page block post logout | High | User logged out | 1. Direct navigate to `/orders` | Access denied; redirected to `/login`. | Not Executed |
| **TC-010** | Discovery | Search restaurant by keyword | High | On Home Page | 1. Type "Pizza Express"<br>2. Submit | Displays matching restaurants only. | Not Executed |
| **TC-015** | Cart | Add food item to cart | High | On Menu Page | 1. Select food item<br>2. Click 'Add to Cart' | Cart badge updates to 1 item. | Not Executed |
| **TC-016** | Cart | Increase item quantity | High | Item in cart | 1. Click '+' icon on item line | Quantity increases to 2; line total updates. | Not Executed |
| **TC-019** | Cart | Verify cart subtotal & fees math | High | Cart populated | 1. Subtotal ($20) + Delivery ($3) | Grand total calculates accurately to $23.00. | Not Executed |
| **TC-022** | Checkout | Apply valid coupon code | High | At Checkout | 1. Enter `SAVE10`<br>2. Apply coupon | Subtotal discounted by 10%. | Not Executed |
| **TC-024** | Payment | Checkout via Cash on Delivery | High | Address filled | 1. Select COD<br>2. Click 'Place Order' | Order processed; confirmation page displays Order ID. | Not Executed |
| **TC-026** | Orders | Order appears in Order History | High | Order placed | 1. Open Profile $\rightarrow$ Order History | Order listed at top with active status. | Not Executed |
| **TC-029** | Responsive | Mobile view layout check | High | Viewport 375px | 1. Emulate mobile screen width | Clean layout; no horizontal scrollbar. | Not Executed |

---

## Negative & Boundary Testing Matrix
- **Invalid Email Input:** Entering `fatma.domain` blocks submission with email format error.
- **Empty Cart Checkout:** Clicking checkout on 0 items redirects to `/cart`.
- **Expired Coupon:** Submitting `EXPIRED2025` returns "Coupon code expired".
- **Zero/Negative Quantity:** Directly inputting `-1` forces quantity reset to `1`.
