---
id: Campaign
title: Create Campaign
---

# Create Campaign

This endpoint allows you to **create a new campaign** in Mautic.

## Endpoint

```http
POST /api/campaigns/new
```

## Full URL Example
```text
http://your-mautic-domain.com/api/campaigns/new
```

## Authentication
Mautic supports the following authentication methods for API access:

- **OAuth2**  
- **Basic Auth**  
- **API Key**

:::tip
Ensure your credentials have permission to create campaigns.
:::

## Request Example (cURL)
```bash
curl -X POST \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{
        "name": "Summer Promotion",
        "description": "Automated campaign for summer sales",
        "isPublished": true
      }' \
  http://your-mautic-domain.com/api/campaigns/new
```
## Request Body Parameters

| Parameter     | Type    | Description                                 |
|---------------|---------|---------------------------------------------|
| `name`        | string  | Name of the campaign                        |
| `description` | string  | Description of the campaign                 |
| `isPublished` | boolean | Whether to publish the campaign immediately |

## Response Example
```json
{
  "campaign": {
    "id": 456,
    "name": "Summer Promotion",
    "description": "Automated campaign for summer sales",
    "isPublished": true,
    "dateCreated": "2025-08-21T10:00:00+00:00"
  },
  "success": true
}
```

## Notes

- Returns **400 Bad Request** if required fields are missing.
- Campaign ID is returned in the response and can be used for subsequent API operations.
- Useful for **automating marketing workflows** or integrating campaigns with external systems.

