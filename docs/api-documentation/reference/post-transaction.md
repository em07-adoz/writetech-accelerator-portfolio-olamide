---
id: post-transaction
title: AI Invoice Data Generator
---

Generates an invoice based on provided instructions.

### Endpoint
`POST https://api.chimoney.io/v0.2.4/ai/invoice/generate`


### Request Body

| Field        | Type   | Required | Description                                       |
|--------------|--------|----------|---------------------------------------------------|
| businessName | string | ✅ Yes   | The name of the business issuing the invoice.     |
| customerName | string | ✅ Yes   | The name of the customer to bill.                 |
| items        | array  | ✅ Yes   | List of items/services (with description, quantity, and price). |
| currency     | string | ✅ Yes   | Currency code (e.g., USD, NGN).                   |

### Example Request

```bash
curl -X POST "https://api.chimoney.io/v0.2/invoice/ai-generator" \
  -H "X-API-Key: YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "businessName": "TechWorld Ltd.",
    "customerName": "Jane Doe",
    "currency": "USD",
    "items": [
      { "description": "Web Hosting", "quantity": 1, "price": 100 },
      { "description": "Domain Registration", "quantity": 2, "price": 15 }
    ]
  }'
  ```

### Example Response
```json
{
  "success": true,
  "invoiceID": "inv_78910",
  "data": {
    "businessName": "TechWorld Ltd.",
    "customerName": "Jane Doe",
    "currency": "USD",
    "totalAmount": 130,
    "items": [
      { "description": "Web Hosting", "quantity": 1, "price": 100 },
      { "description": "Domain Registration", "quantity": 2, "price": 15 }
    ],
    "generatedAt": "2025-08-29T11:00:00Z"
  }
}
```