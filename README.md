# Free n8n Server on Google Cloud

This repository documents how I set up a free **n8n server** on Google Cloud as an alternative to paying monthly subscriptions for automation tools like **Zapier, Make, or n8n Cloud**.  

## Overview
Instead of using hosted automation services, I deployed n8n on a free Google Cloud VM (Free Tier).  
This allows me to build and run automation workflows without any monthly costs.

## Steps

1. **Create a VM instance**  
   - Use Google Cloud Free Tier (e2-micro instance).  

2. **Install Docker**  
   ```bash
   sudo apt update && sudo apt install docker.io -y
   
3. **Run n8n in Docker**  
```bash
docker run -it --rm \
  --name n8n \
  -p 5678:5678 \
  n8nio/n8n
```

4. **Configure Firewall**
Open port `5678` in Google Cloud firewall rules.

6. **Access n8n**
   Open `http://<your-external-ip>:5678` in your browser.
   
## Outcome
- A fully functional **self-hosted n8n instance** running for free
- Can integrate with services such as `Google Sheets`, `Gmail`, `Slack`, and more
- Saves subscription costs by avoiding paid automation platforms like `Zapier`, `Make`, or `n8n Cloud`
## Reference
Based on:  
[`Stop paying monthly n8n automation fees: Build your own free n8n server on Google Cloud`](https://drlee.io/stop-paying-monthly-n8n-automation-fees-build-your-own-free-n8n-server-on-google-clouds-free-84be73299220)
