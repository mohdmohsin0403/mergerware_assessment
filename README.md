# Loan Management App

A simple loan management application built with Meteor and Blaze, allowing users to register, request loans, and manage loan transactions. 

Implemented the following features:

* **User Registration**: Users can register using their email. They can choose roles (admin, borrower, lender) during registration.
* **Loan Request**: Borrowers can request a loan, and the request is reflected on their dashboard.
* **Loan Confirmation**: Lenders can confirm and pay the loan, and the transaction is reflected on both the lender's and borrower's dashboards.
* **Dashboard Updates**: Changes in loan status are reflected on each user's dashboard.
* **Admin Dashboard**: Admin users can view complete transaction history.

### Getting Started

1. Fork and clone this repository.
2. Install dependencies using the `meteor npm install` command.
3. Start the web server using the `meteor` command. The app will be served at <http://localhost:3000/>.
4. Go to <http://localhost:3000/> in your browser.

## Dependencies

### Meteor Packages
* accounts-ui
* accounts-password
* kadira:flow-router
* kadira:blaze-layout
* twbs:bootstrap
* themeteorchef:jquery-validation
* jquery
* tprzytula:remember-me
* fortawesome:fontawesome

### NPM Modules
* Meteor
* Bcrypt
* @babel/runtime
* meteor-node-stubs

## Example Code

```javascript
LoanManagementApp.requestLoan(userId, amount, (error) => {
  if (error) {
    // Handle error and show appropriate message
  } else {
    // Update borrower's dashboard
    FlowRouter.go('/dashboard');
  }
}, loanDetails);
```

### Process
This application is an extension of the existing Meteor/Blaze project. I added new functionalities for user roles, loan requests, and transactions. I utilized Meteor's reactive nature to ensure real-time updates on user dashboards.

### Next Steps
- Enhance security measures, especially for financial transactions.
- Implement a "Forgot password" function.
- Expand functionality for advanced features.
- Conduct thorough testing and review for production readiness.
