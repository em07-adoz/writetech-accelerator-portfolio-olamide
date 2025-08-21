---
id: getting-started
title: Getting Started
---

# Getting Started with Mautic

This guide helps you **install, set up, and run Mautic** quickly, whether you are a marketer or developer. It balances clarity for beginners with the technical depth needed for real-world usage.

## Installation Options

### 1. Using Docker (Recommended)
Docker simplifies setup and ensures consistent environments.

```bash
docker run --name mautic -p 8080:80 mautic/mautic
```

:::tip
Access Mautic at [http://localhost:8080](http://localhost:8080) and create your **admin account** during the web setup.
:::

## 2. Using a Web Server
1. Download the latest Mautic release from [https://www.mautic.org/download](https://www.mautic.org/download).  
2. Upload the files to your web server (Apache, Nginx, etc.).  
3. Prepare a database (MySQL or MariaDB).  
4. Run the installation wizard:
   - Enter **database credentials**  
   - Create an **admin account**  
   - Configure **basic site settings**  
5. Log in to your dashboard to start configuring Mautic.

:::tip
Ensure your PHP version, extensions, and file permissions meet Mautic requirements.
:::

## Initial Setup

### Accessing Mautic
1. Open your browser and go to the URL where Mautic is hosted.  
2. Log in using the **admin account** you created during setup.  
3. Explore the **dashboard** and familiarize yourself with the interface.

### Configure Email Sending
1. Navigate to **Settings → Configuration → Email Settings**.  
2. Set up **SMTP** or third-party services (SendGrid, Mailgun).  
3. Test sending emails before launching campaigns.

### Add Contacts
1. Navigate to **Contacts → New Contact**.  
2. Import via CSV or add manually.

### Create Your First Campaign
1. Go to **Campaigns → New Campaign**.  
2. Define **triggers**, **actions**, and **goals**.  
3. Activate and monitor campaign performance.

### Set Up Forms & Landing Pages
1. Navigate to **Components → Forms / Landing Pages**.  
2. Add fields, configure actions, and embed on your website.

## Accessing the API

Mautic provides a **REST API** for developers:

```text
Base URL: http://your-mautic-domain.com/api
```

:::tip
Practical API examples such as get-contact.md and create-campaign.md are provided in the reference/ folder.
:::

## Next Steps

Once Mautic is installed:

- Explore pre-built **campaign templates**  
- Automate **lead scoring** and segmentation  
- Integrate with your **CRM or website**  
- Use **analytics and reports** to measure marketing performance