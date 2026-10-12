# Hosting Signup Guide — Yangon Underground Radio

**Goal:** Get a working stream server (private test) within 24 hours. Prefer managed AzuraCast for month one.

## Recommended Options (Oct 2026)

| Provider | Starting Price | Listeners | Notes |
|----------|----------------|-----------|-------|
| HiredHosting / MyAutoDJ AzuraCast | ~$2.95/mo | 100 | Instant, Web DJ, AutoDJ, free SSL, trial available |
| Asura Hosting | ~$3.99/mo | 120 | Instant setup, good storage |
| Hostinger VPS + self-host AzuraCast | ~$6–13/mo | Unlimited (your bandwidth) | More control, requires Docker |

**Recommendation for first 30 days:** Managed AzuraCast at ~$3/mo. Cap listeners. Do not self-host from home.

## Step-by-Step: Managed AzuraCast (HiredHosting example)

1. Go to the provider site (search “HiredHosting AzuraCast” or “MyAutoDJ AzuraCast”).
2. Choose the Basic / Starter plan (~$2.95–4/mo).
3. Create account (use station email).
4. Complete payment (card or supported method). Note: Myanmar payment options may require international card or agent.
5. Wait for instant activation email.
6. Log into the AzuraCast control panel.
7. Create your station:
   - Station name: Yangon Underground Radio
   - Short name / URL slug: yur or yangon-underground
   - Genre: Electronic / Alternative / Hip-Hop
8. Note the stream URL, mount point, and DJ login credentials.
9. Enable AutoDJ and upload 5–10 rights-cleared test tracks.
10. Test the public stream URL in a browser or VLC before connecting Mixxx/BUTT.

## Self-Host Alternative (VPS)

If you prefer control:
```bash
# On Ubuntu VPS
mkdir -p /var/azuracast && cd /var/azuracast
curl -fsSL https://raw.githubusercontent.com/AzuraCast/AzuraCast/main/docker.sh > docker.sh
chmod a+x docker.sh
./docker.sh install
```
Then open the web installer at `http://YOUR_IP`.

## After Signup
- Record stream URL, port, mount, and source password.
- Test from a second device.
- Keep the listener limit low until public launch is cleared.
- Update the website player embed once confirmed.

**Do not announce the stream publicly until regulatory and rights checks are done.**