---
id: get-transaction
title: Get Transaction Details by issueID
---

Retrieves all transactions associated with a specific issueID, including details such as transaction IDs, amounts, statuses, and metadata.

### Endpoints
`POST https://api.chimoney.io/v0.2.4/accounts/issue-id-transactions`

### Base URL
All API requests are made to the following base URL:
`https://api.chimoney.io/v0.2.4/accounts/issue-id-transactions`

### Query Parameters

| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| issueID   | string | Yes      | The unique identifier of the issued transaction you want to fetch details for. |

### Example Request
```bash
curl -X GET "https://api.chimoney.io/v0.2/payment/issue-id?issueID=abc12345" \
  -H "Content-Type: application/json" \
  -H "X-API-Key: YOUR_API_KEY"
```

### Example Response

```json
{
  "success": true,
  "data": {
    "issueID": "abc123xyz",
    "status": "completed",
    "amount": 50,
    "currency": "USD",
    "recipient": "user@example.com",
    "dateIssued": "2025-08-20T12:34:56Z",
    "dateCompleted": "2025-08-21T14:22:31Z"
  }
}
```
