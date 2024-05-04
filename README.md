## Kani Ida

## Introduction
Savory Season Spices, an ecommerce platform specializing in spices, aims to enhance their customer experience by offering a comprehensive online service. The platform seeks to provide seamless product discovery, efficient order processing, and robust customer
interaction through a feature-rich web application. The application will handle various operations such as product listings, searches, user-specific order histories, and customer service inquiries, thereby facilitating a user-friendly and efficient shopping 
experience for both new and returning customers.

## Key Features

### Audit Trail
The system logs all user activities, providing a detailed audit trail.
Audit logs help administrators monitor and review user actions for security and compliance purposes.

### User Authentication and Authorization
Users must authenticate themselves to access the system, ensuring secure access.

### Multi-Factor Authentication (MFA)
Users can enable MFA for an additional layer of security during login.

### Access Control
Role-based access control allows to define user privileges based on their roles and permissions, maintaining data integrity.
Authorized users can perform actions (update, delete, etc) on documents.

### Product Catalogue and Search
Products are displayed with essential details, and users can view them with pagination to handle large datasets.
Users can search the product catalog by keywords, check availability, and sort by price, facilitating an easier and more tailored shopping experience.

### Order Processing
Users can view their entire order history, allowing them to track past purchases and their statuses.
Users can retrieve specific order details, and have the ability to cancel their orders if necessary.

### Shopping Cart Functionality
Users can add, update, or remove items from their shopping cart, view the contents of their cart, and clear their cart entirely.
The cart updates dynamically as items are added, removed, or changed in quantity.

# Functional Requirements

## User Account

**New Account**
1. The application should allow users to create a new account using basic information, email(all emails are unique), and password.
2. The application should disabled all newly created accounts until verified.
3. The application should send an email with a link to confirm new user account.
4. Only after verifying a new account should a user be able to log into the application.

**Log In**
1. The application should allow users to enter an email and password to log in.
2. If MFA is set up, the application should ask for a QR code after entering correct email and password.
3. After 6 failed login attempts, user account should be locked for 15 minutes (mitigate brute force attack).
4. After 90 days, user password should expire therefore can't log in until password is updated (password rotation).

**Reset Password**
1. The application should allow users to reset their password.
2. The application should send a link to users' email to reset their password (link to be invalid after being clicked on).
3. The application should present a screen with a form to reset password when the link is clicked.
4. If a password is reset successfully, user should be able to log in using the new password.
5. The application should allow users to reset their password as many times as they need.

**MFA (Multi-Factor Authentication)**  
1. The application should allow users to set up Multi-Factor Authentication to help secure their account.
2. Multi-Factor Authentication should use a QR code on users' mobile phone.
3. The application should allow users to scan a QR code using an authenticator application on their phone to set up Multi-Factor Authentication.
4. The application should ask users to enter the QR code from their mobile phone authenticator application in order to log in successfully.

**Profile**
1. The application should allow users to update their basic information while logged in.
2. The application should allow users to update their password while logged in.
3. The application should allow users to update their account settings while logged in.
4. The application should allow users to update their profile picture while logged in.

## Product Management

**Products**
1. Users should be able to view all available products. The system must support pagination to manage large inventories.
2. Users can search for products based on keywords, availability, and price. Search results should be paginated and sortable.

## Order Management

**Order**
1. Users must be able to place orders through the system. This includes integration with payment gateways to handle transactions.
2. Users should be able to view their past orders to track purchase history and order statuses.
3. Users can retrieve details of a specific order.
4. Users have the ability to cancel their orders if needed.

## Shopping Cart Management

**Shopping Cart**
1. Users can add items to their shopping cart.
2. Users should be able to update the quantity of the items in their cart.
3. Users can remove items from their shopping cart.
4. Users can view all items in their cart.
5. Users have the option to clear all items in their shopping cart at once.
