# Explanation

## The Problem

Online retailers lose an estimated $101 billion annually to return fraud. Unlike payment fraud, return fraud is harder to detect because it exploits a process that is supposed to be generous — lenient return policies are a deliberate business decision to build customer trust. Fraudsters weaponize that trust at scale.

The challenge is not simply detecting fraud. It is doing so without making the 96–98% of legitimate customers feel like suspects.

## What Fraud Actually Looks Like

Return fraud is not a single behaviour — it is a spectrum of attacks, each requiring different detection strategies.

- **Wardrobing** is when a customer purchases a product with the intent to use it temporarily and return it. A dress worn to a wedding, electronics used for a trip, tools rented-by-purchase. The item comes back in technically returnable condition, but the purchase was never genuine.

- **Item Not Received (INR) abuse** involves a customer claiming a delivered package never arrived. Carrier scan data shows delivery, but the customer disputes it. At low volumes this is often genuine; at scale, it becomes a pattern.

- **Falsified damage claims** involve customers submitting photos of damaged products that were either damaged intentionally, photographed before purchase, or sourced entirely from the internet. The image metadata and pixel-level manipulation signatures are the only technical signals available.

- **Receipt manipulation** ranges from editing a receipt's date or price in a PDF editor to using a different product's receipt for a higher-value return.

- **Friendly fraud** occurs when a customer receives the product, keeps it, and then files a chargeback with their bank claiming the transaction was unauthorised. By the time the dispute resolves, the retailer has lost both the product and the money.

- **Organised return rings** are the most damaging pattern — coordinated groups operating across dozens of synthetic or stolen accounts, rotating through addresses and devices, submitting high-value fraud claims that individually look legitimate but collectively form a network signature.

## The Core Tension You Must Resolve

The estimated business cost of incorrectly blocking one legitimate customer — in refund support time, loyalty erosion, social media escalation, and potential legal exposure — is greater than the average value of one fraudulent return.

---

### Note: This serves only as a reference example. Innovative ideas and unique implementation techniques are highly encouraged and warmly welcomed! 
