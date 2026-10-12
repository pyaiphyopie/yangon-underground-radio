# Yangon Underground Radio

Independent internet radio for underground music in Yangon. Burmese + English. Internet-first (no FM transmitter).

## Status
- Landing page live (this repo)
- Stream: private testing phase
- Public launch: conditional on regulatory guidance and rights clearance

## Tech Stack (Month 1)
- **Mixing:** Mixxx (free)
- **Encoder:** BUTT (Broadcast Using This Tool)
- **Server:** AzuraCast (self-hosted on VPS or managed host ~$3/mo)
- **Video:** OBS Studio
- **Website:** This static page

## Quick Start - Stream Hosting
1. Sign up for managed AzuraCast (e.g. HiredHosting, MyAutoDJ, or similar from ~$2.95/mo for 100 listeners) **or**
2. Deploy AzuraCast on a cheap VPS (Hostinger, DigitalOcean, etc.):
   ```bash
   mkdir -p /var/azuracast && cd /var/azuracast
   curl -fsSL https://raw.githubusercontent.com/AzuraCast/AzuraCast/main/docker.sh > docker.sh
   chmod a+x docker.sh
   ./docker.sh install
   ```
3. Create station in AzuraCast dashboard.
4. Configure Mixxx or BUTT to stream to the Icecast/SHOUTcast mount.
5. Embed the HTML5 player from AzuraCast into index.html.

## Rights
Only play tracks with documented permission. Maintain a rights register.

## Regulatory
Confirm current Ministry of Information guidance for online broadcasting before public monetized launch.

## Brand
Dark luxury / underground cyberpunk. Colors: #070707, #00AEEF, #8B5CF6, #F5F7FA.

---
*Planning date: 12 October 2026*