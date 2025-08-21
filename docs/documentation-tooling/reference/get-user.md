---
id: get-contact
title: Get Contact
---

# Get Contact

This endpoint allows you to **retrieve details of a specific contact** in Mautic.

## Endpoint

```http
GET /api/contacts/{contactId}

## Full URL Example
```text
http://your-mautic-domain.com/api/contacts/123
```

## Authentication

Mautic supports the following authentication methods for API access:

- **OAuth2**  
- **Basic Auth**  
- **API Key**

:::tip
Make sure your credentials have access to contacts.
:::

## Request Example (cURL)
```bash
curl -X GET \
  -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
  http://your-mautic-domain.com/api/contacts/123
```

## Response Example
```json
{
  "contact": {
    "id": 123,
    "firstname": "John",
    "lastname": "Doe",
    "email": "john.doe@example.com",
    "tags": ["lead", "newsletter"],
    "points": 15,
    "dateCreated": "2025-08-20T14:00:00+00:00"
  },
  "success": true
}
```

## Notes

- Returns **404 Not Found** if the contact ID does not exist.  
- Can include additional fields by using query parameters such as `?fields=firstname,lastname,email`.  
- Useful for **integrating Mautic contacts into external apps** or displaying contact info programmatically.