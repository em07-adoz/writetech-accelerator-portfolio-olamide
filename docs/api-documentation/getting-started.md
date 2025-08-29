---
id: getting-started
title: Getting Started
---

This guide will help you set up and make your first request to the Chimoney API.

## API User Requirements
Before you begin, ensure you have:
- A **Chimoney account**
- An **API key** (generated from your Chimoney dashboard)
- A tool to make requests such as [cURL](https://curl.se/) or [Postman](https://www.postman.com/)

## API Base URL
All API requests are made to the following base URL:  
`https://api.chimoney.io/v0.2.4`

## Authentication
Chimoney uses **Bearer Token authentication**.  
Your API key must be included in the `Authorization` header of each request.

**Format:**
```http
Authorization: Bearer YOUR_API_KEY
```

### Example Request
```bash
curl -X GET "https://api.chimoney.io/v0.2.4/info" \
  -H "Authorization: Bearer YOUR_API_KEY"
```
### Example Response

```json
{
  "success": true,
  "data": {
    "issueID": "abc12345",
    "amount": 50,
    "currency": "USD",
    "status": "Completed",
    "receiver": "user@example.com",
    "createdAt": "2025-08-01T10:20:30Z",
    "completedAt": "2025-08-01T10:25:00Z"
  }
}
```

## ❌ Error Handling

Chimoney returns standard HTTP status codes along with a JSON body that contains details about the error.

### Common Error Codes

| Code | Meaning                                     | Example Response |
|------|---------------------------------------------|------------------|
| **400**  | Bad Request – something is wrong with your input | ```json { "success": false, "error": "Invalid issueID" } ``` |
| **401**  | Unauthorized – missing or invalid API key   | ```json { "success": false, "error": "Unauthorized" } ``` |
| **404**  | Not Found – resource doesn’t exist          | ```json { "success": false, "error": "Transaction not found" } ``` |
| **500**  | Server Error – problem on Chimoney’s side   | ```json { "success": false, "error": "Something went wrong" } ``` |



