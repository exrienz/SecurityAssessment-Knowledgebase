# Common Business Logic Errors Examples:

### Review Feature Testing
- Unauthorized reviews without purchase verification.
- Out-of-scale ratings (e.g., 0 or negative in 1-5 scale).
- Multiple user ratings for one product (race conditions).
- File upload field vulnerability testing.
- Impersonation of other users' reviews.
- Unprotected Cross-Site Request Forgery (CSRF) checks.

### Discount Code Feature Testing
- Code reuse attempts.
- Race conditions with same code.
- Mass Assignment or HTTP Parameter Pollution.
- XSS or SQL Injection in code application.
- Discounts on non-discounted items.

### Delivery Fee Manipulation
- Negative delivery charge experiments.
- Activation of free delivery.

### Currency Arbitrage
- Payment and refund in different currencies.

### Premium Feature Exploitation
- Accessing premium sections without a subscription.
- Usability of premium features after refund.
- True/false value alteration for unauthorized access.

### Refund Feature Exploitation
- Product accessibility post-refund.
- Currency arbitrage opportunities.
- Multiple refunds via cancellation.

### Cart/Wishlist Exploitation
- Balancing total with negative quantities.
- Adding more products than available.
- Moving products between carts.

### Thread Comment Testing
- Checking comment quantity limits.
- Exploiting race conditions for comments.
- Commenting as verified/privileged users.

### Parameter Tampering
- Manipulating payment or critical fields.
- Exploiting HTTP Parameter Pollution & Mass Assignment.
- Response manipulation for bypassing restrictions.
