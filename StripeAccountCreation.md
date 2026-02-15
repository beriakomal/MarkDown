# Accept simple payments for a startup
Learn how to enable Stripe payments for your business without writing code.
This guide describes the actions you need to take in your Stripe integration to accept one-off payments as a startup.
## 1 Create a Stripe Account
Before integrating with Stripe, you must create a Stripe account.
1. [Create an account](/RedHat.md) by entering your email address, full name and country, and creating a password.
2. Fill out your business profile.
3. In the Dashboard, click **Verify your email**. Stripe sends a verification email to your email address.
4. Verify your email address.
   
## 2 Create a Payment Link
[Payment Links](/RedHat.md) let your customers pay you when you sell online. Create a single link that you can share with everyone.

**Create a payment link**

1. In the Dashboard, open the Payment Links page and click **+New**.
2. Select an existing product or click **+Add a new product**.
3. If you’re adding a new product, fill out the product details and click **Add product**.
4. Click **Create Link**.

## 3 Share the Payment Link with your customers
Use the Dashboard to copy your payment link and share it online. Click the copy icon next to an existing link on the [Payment Links](/RedHat.md) page or go to the payment link’s details page. You can share your payment link multiple times and anywhere online, including:
   
   * Emails
   * Text Messages
   * Social Media Platforms

## 4 Go Live
1. In the Dashboard, open your [Account settings]().
2. Enter your business type, tax details, business details, personal verification information and customer-facing information (for example, a statement descriptor).
3. Add bank details to confirm where to pay out your money.
4. Set up two-step authentication to secure your account.
5. You can optionally add automatic tax collection or revenue-based climate donations.
6. Review the information you entered and click **Agree and submit**.
7. After you activate your profile, Stripe updates you from sandbox mode to live mode.

**Payments**

|Quick Start|Description|
|-----------|-----------|
|Accept carbon removal payments|Enable customers to buy carbon removal using the Climate API.|
|Accept in-person payments|Get started with Stripe Terminal for in-person payments.|
|Accept subscriptions with a prebuilt checkout page|Set up recurring payments and subscription management.|
|Build an Embedded form checkout|Customers enter payment details directly on your site without redirection from your site or app.|

>Chrome extensions
We recommend you build your payment integration with Stripe (such as Elements or Checkout) on your own website. Then, set up your Chrome extension to send users to this payment page when they’re ready to complete a purchase.<br>
This method is more secure and easier to maintain than trying to handle payments directly within the extension.

To install the Stripe CLI with [homebrew](), run:

```
brew install stripe/stripe-cli/stripe
```

![Image](/Images/imgae1.png)


Was this page helpful?
`Yes`   `No `