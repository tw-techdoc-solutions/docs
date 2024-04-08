# Exploring a Payments API

This page will help you get started with the Payments API

## Introduction

Today, in the dynamic world of e-commerce and financial transactions, a robust and efficient API (Application Programming Interface) is an essential component for companies.

In this article, we will explore an API equipped with two main endpoints.

The first endpoint, which uses the POST method, allows sellers to create payments objects, enabling smooth financial transactions. 

The second endpoint, powered by the GET method, provides comprehensive payments reports, offering valuable information on transaction history.  
Together, these endpoints form a powerful tool for modern businesses to streamline payments processes and gain actionable insights based on data.

## Product journey

We will explore the path of an API with two main endpoints: one that uses the POST method to create payments objects for sellers and the other that uses the GET method to generate payments reports. These endpoints are key to facilitating transactions and tracking payments activity.

#### [Create payments](https://matthewsls.stoplight.io/docs/intro-docs-reference/api%2Fpayments-json%2Foperations%2Fcreate-a-payment)

1. **Request:**

Method: POST  
Description: Use this endpoint to make payments.

2. **Request Parameters:**

`external_id`: The unique identifier of the seller initiating the payment.  
`amount`: The payment amount.  
`payment_method`: The chosen payment method (e.g. credit card, PayPal).  
`order_id`: Uniquely identify each order placed by a customer. This makes it easier to track order status, manage stock and generate invoices.

3. **Response:**

Status Code: 201 (Created)  
Description: Upon a successful request, a payments object is created, and the system return a confirmation.

#### [Consult your payments reports](https://matthewsls.stoplight.io/docs/intro-docs-reference/api%2Fpayments-json%2Foperations%2Fget-a-payment)

1. **Request:**

Method: GET  
Description: Use this endpoint enables users to access payments reports, offering insights into transaction history.

2. **Request Parameters:**

`report_id`: The unique identifier of the vendor to retrieve payments reports for.

3. **Response:**

Status Code: 200 (OK)  
Description: The system responds with the requested payments reports, providing detailed information on all transactions within the specified time period.

The route of this API is divided into two essential endpoints: one for creating payment objects and the other for generating payment reports. The POST endpoint facilitates the initiation of transactions by allowing sellers to create payment objects, while the GET endpoint allows users to retrieve payment reports, giving them valuable information about their transaction history.

This API not only simplifies payments processes but also enhances transparency and accountability in financial transactions, making it an indispensable tool for businesses and vendors alike in the digital commerce landscape.

### Understanding the Payments Status API

The world of payments means that the status of transactions is crucial for both companies and their customers. To simplify this process, payments APIs play a key role in ensuring transparency and efficiency. This article will explain the payments API that handles seven essential payments status: **Enrolled**, **Expired**, **Ready to Enroll**, **Enrolling in Process**, **Created**, **Canceled**, and **Rejected**.

![image](https://github.com/tw-techdoc-solutions/docs/assets/61173495/b0510065-21ae-41ec-b047-091fe497447f)



#### Enrolled

- **Status:** This indicates that a user or entity has successfully enrolled in a payments system or program.
- **Use Case:** Typically, when a user registers for a subscription, this status confirms their successful enrollment. This is an optimistic start to the payments journey.

#### Expired

- **Status:** The "Expired" status is a clear indicator that a payments or subscription has passed its validity period and can no longer be utilized.
- **Use Case:** This status is crucial for automatic subscription renewals and signifies the end of a payments cycle.

#### Ready to Enroll

- **Status:** When a user expresses interest in a payments program but hasn't completed the enrollment process, their status is "Ready to Enroll."
- **Use Case:** It serves as a waypoint, indicating that a user is on the brink of joining a payments system, often requiring them to take some final actions.

#### Enrolling in Process

- **Status:** "Enrolling in Process" suggests that a user is in the midst of the enrollment process, and their application is being reviewed.
- **Use Case:** This status allows businesses to keep track of pending enrollments and ensures a seamless transition from "Ready to Enroll" to "Enrolled."

#### Created

- **Status:** Once the enrollment process is successfully completed, the status changes to "Created," indicating the birth of a new payments or subscription.
- **Use Case:** This is a crucial status to identify when a payments method or subscription is set up and ready for future transactions.

#### Canceled

- **Status:** The "Canceled" status implies that a user or entity has chosen to terminate their subscription or payments program.
- **Use Case:** This status is vital for tracking churn rates and managing customer retention strategies.

#### Rejected

- **Status:** When a payments request is denied or an enrollment application is rejected, the status is marked as "Rejected."
- **Use Case:** This status helps businesses identify unsuccessful transactions and the need for remedial actions.
