# cloudflare-ddns

Uses Cloudflare API to change the A, AAAA records of your domain. Useful for those with dynamic IPs.
Open the .env file to edit these variables:

**API_KEY**: your Cloudflare API key, with Zone:DNS Edit, Zone:Zone Read, Zone:Zone Settings Read, for the zone that your domain is in.

**DOMAIN**: the domain which you want to update the records for.

**PROXY**: true/false to toggle Cloudflare's proxy setting.