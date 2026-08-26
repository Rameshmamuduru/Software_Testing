## Manual testing project:
- project introduction
- understanding and explore the functionality
- test plan
- test scenarios
- test cases and reviews
- test environment and Build Deployment
- Test Execution
- Bug reporting and tracking
- Sanity testing, re-testing and regression testing
- test reports
- Test signoFF

### Frontend:
```
|      # | Customer Activity         | What the Customer Does                                       |
| -----: | ------------------------- | ------------------------------------------------------------ |
|  **1** | **Register**              | Create an account                                            |
|  **2** | **Login**                 | Login using username/password, OTP, etc.                     |
|  **3** | **Manage Profile**        | Update name, phone, email, password, etc.                    |
|  **4** | **Browse Products**       | Browse categories and products                               |
|  **5** | **Search Products**       | Search for a particular product                              |
|  **6** | **Filter & Sort**         | Filter by price, brand, rating, etc.                         |
|  **7** | **View Product**          | Check product details, images, price, stock, reviews         |
|  **8** | **Add to Wishlist**       | Save products for later                                      |
|  **9** | **Add to Cart**           | Add products to shopping cart                                |
| **10** | **Manage Cart**           | Change quantity, remove products, review total               |
| **11** | **Manage Address**        | Add/select/edit delivery address                             |
| **12** | **Checkout**              | Review products, address, shipping, taxes, discounts         |
| **13** | **Apply Coupon/Offer**    | Apply promotional codes or discounts                         |
| **14** | **Make Payment**          | Pay using card, UPI, net banking, wallet, etc.               |
| **15** | **Place Order**           | Confirm and place the order                                  |
| **16** | **View Order**            | Check order details and order history                        |
| **17** | **Track Order**           | Track shipment and delivery status                           |
| **18** | **Cancel Order**          | Cancel an eligible order                                     |
| **19** | **Return Product**        | Request return for an eligible product                       |
| **20** | **Request Refund**        | Track/request refund after cancellation/return               |
| **21** | **Rate & Review**         | Rate and review purchased products                           |
| **22** | **Receive Notifications** | Receive order, payment, shipping, and delivery notifications |
| **23** | **Contact Support**       | Raise complaints or support requests                         |
| **24** | **Logout**                | Logout from the application                                  |

```

### Backend - Admin:
```
|      # | Admin Activity                   | What the Admin Does                                                   |
| -----: | -------------------------------- | --------------------------------------------------------------------- |
|  **1** | **Admin Login**                  | Login securely to the admin portal                                    |
|  **2** | **Dashboard**                    | View sales, orders, customers, inventory and business metrics         |
|  **3** | **User Management**              | View, create, update, deactivate or manage customer accounts          |
|  **4** | **Product Management**           | Add, edit, delete and view products                                   |
|  **5** | **Category Management**          | Create, edit and delete product categories/subcategories              |
|  **6** | **Inventory Management**         | Update stock, monitor inventory and manage out-of-stock products      |
|  **7** | **Price Management**             | Add/update product prices                                             |
|  **8** | **Offer & Coupon Management**    | Create, modify, activate/deactivate coupons and offers                |
|  **9** | **Order Management**             | View and manage customer orders                                       |
| **10** | **Order Status Management**      | Update order status such as Processing, Shipped, Delivered, Cancelled |
| **11** | **Cancellation Management**      | Review and process cancellation requests                              |
| **12** | **Return Management**            | Review and approve/reject product returns                             |
| **13** | **Refund Management**            | Process or approve customer refunds                                   |
| **14** | **Payment Management**           | View payment status, failed payments and transaction details          |
| **15** | **Shipping Management**          | Manage shipping information, carriers and delivery status             |
| **16** | **Customer Support**             | View and respond to customer complaints/tickets                       |
| **17** | **Reviews & Ratings Management** | Monitor, approve/remove inappropriate reviews                         |
| **18** | **Content Management**           | Manage banners, promotional content, product descriptions, etc.       |
| **19** | **Reports & Analytics**          | Generate sales, revenue, order, customer and inventory reports        |
| **20** | **Admin/User Roles**             | Create admin users and assign permissions                             |
| **21** | **Security & Audit**             | Monitor admin activities, login history and audit logs                |
| **22** | **Notifications**                | Configure or send customer notifications                              |
| **23** | **Configuration**                | Manage application/business settings                                  |
| **24** | **Logout**                       | Securely logout from the admin portal                                 |

```
### How to understand the Application/system:
- By using the Functional requirement specificational document (FRS)
- 

### UI security checklist:

```text
Registration
├── Password policy
├── Duplicate accounts
├── Account enumeration
├── Email/OTP verification
├── Rate limiting
├── Input validation
├── Role manipulation
└── Sensitive data exposure
```

### Login

```text
Login
├── Authentication bypass
├── Brute-force protection
├── Account enumeration
├── Session management
├── Session timeout
├── Logout/session invalidation
├── Input validation
├── Password protection
├── Authorization
└── Sensitive data exposure
```

### Search

```text
Search
├── Input validation
├── XSS protection
├── Injection protection
├── Excessive/oversized input handling
├── Unauthorized data exposure
├── Search parameter manipulation
├── Rate limiting
└── Sensitive data exposure
```

### Product

```text
Product
├── Unauthorized product access
├── Product ID manipulation
├── Price manipulation
├── Stock manipulation
├── XSS in product data/reviews
├── Unauthorized product modification
├── Sensitive data exposure
└── API authorization
```

### Cart

```text
Cart
├── Unauthorized cart access
├── Other user's cart access
├── Product ID manipulation
├── Quantity manipulation
├── Price manipulation
├── Discount/coupon manipulation
├── Stock validation
├── Cart/session manipulation
├── API authorization
└── Sensitive data exposure
```

### Checkout

```text
Checkout
├── Unauthorized checkout access
├── Other user's checkout access
├── Price manipulation
├── Quantity manipulation
├── Discount manipulation
├── Shipping-cost manipulation
├── Address manipulation
├── Order/user ID manipulation
├── Input validation
├── API authorization
└── Sensitive data exposure
```

### Payment

```text
Payment
├── Payment authorization
├── Payment amount manipulation
├── Order ID manipulation
├── Transaction replay/duplicate requests
├── Payment-status manipulation
├── Unauthorized payment access
├── Payment response validation
├── Sensitive payment data protection
├── API authentication/authorization
└── Secure communication
```

### Orders

```text
Orders
├── Unauthorized order access
├── Other user's order access
├── Order ID manipulation
├── Order-status manipulation
├── Cancellation authorization
├── Refund authorization
├── Order data exposure
├── API authorization
└── Session validation
```

### User Profile

```text
User Profile
├── Unauthorized profile access
├── Other user's profile access
├── User ID manipulation
├── Email-change authorization
├── Password-change authorization
├── Input validation
├── XSS protection
├── Session validation
└── Sensitive data exposure
```

### Password Reset

```text
Password Reset
├── Account enumeration
├── Reset-token security
├── Token expiration
├── Token reuse
├── Token manipulation
├── Rate limiting
├── Password policy
├── Unauthorized password change
└── Sensitive data exposure
```

### File Upload

```text
File Upload
├── File-type validation
├── File-size validation
├── Malicious-file handling
├── Filename/path manipulation
├── Unauthorized file access
├── File execution prevention
├── Content-type validation
└── Sensitive file exposure
```

### Admin

```text
Admin
├── Role/privilege escalation
├── Unauthorized admin access
├── Admin API authorization
├── User-management authorization
├── Product-management authorization
├── Order-management authorization
├── Audit/logging
├── Input validation
└── Sensitive data exposure
```
