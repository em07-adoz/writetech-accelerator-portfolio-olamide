# Chimoney API Documentation

## Overview
The Chimoney API allows developers to send payments globally in multiple forms — airtime, gift cards, bank transfers, and more. It supports creating and managing payouts, querying balances, and redeeming vouchers.

## Key Features
- **Global Payouts**: Send airtime, gift cards, or bank transfers to users in different countries.
- **Account Management**: Query and manage your Chimoney account balance.
- **Voucher Redemption**: Redeem Chimoney gift cards or vouchers securely.
- **Scalability**: Automate single or bulk payouts for businesses and applications.

## BASE URL  
`https://api.chimoney.io/v0.2.4`

## Authentication
All API calls require authentication via an **API Key**, which should be included in the request headers as a Bearer token.

### Example:
```http
Authorization: Bearer YOUR_API_KEY
```

## Typical Use Cases
- Sending airtime rewards to users in multiple countries.
- Automating gift card distribution for promotions or campaigns.
- Enabling global payments in applications with just a few API calls.
- Checking account balances and managing funds programmatically.