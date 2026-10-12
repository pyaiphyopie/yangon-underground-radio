# Mixxx + BUTT Configuration Guide

**Goal:** Send a clean live audio stream from your computer to the AzuraCast / Icecast server.

## Prerequisites
- Mixxx installed (https://mixxx.org/)
- BUTT installed (https://danielnoethen.de/butt/)
- Stream server credentials from hosting signup (host, port, mount, source password)
- Wired headphones (prevent feedback)
- USB microphone or interface connected

## Option A: Mixxx Direct Broadcast (simplest for live DJ sets)

1. Open Mixxx.
2. Go to **Options → Preferences → Broadcasting** (or Live Broadcasting).
3. Enable broadcasting.
4. Settings:
   - **Type:** Icecast 2 (or SHOUTcast if your host requires it)
   - **Host:** your AzuraCast server hostname or IP
   - **Port:** usually 8000 or the port given by the host
   - **Mount:** `/stream` or the mount point from AzuraCast (e.g. `/yur`)
   - **Login:** `source` (or the username provided)
   - **Password:** source password from AzuraCast
   - **Format:** MP3, 128 kbps or 192 kbps (start at 128 for reliability)
   - **Channels:** Stereo
5. Click **OK** and start broadcasting from the Mixxx interface.
6. Confirm the stream appears live in your AzuraCast dashboard and on a second device.

## Option B: BUTT (more control, recommended if Mixxx broadcast has issues)

1. Open BUTT.
2. Go to **Settings → Main**.
3. Add a new server:
   - **Type:** Icecast
   - **Address:** your server host
   - **Port:** stream port
   - **Password:** source password
   - **Mountpoint:** `/stream` (or your mount)
   - **User:** source
4. Audio settings:
   - **Codec:** MP3
   - **Bitrate:** 128 kbps
   - **Samplerate:** 44100 Hz
   - **Channels:** Stereo
5. Set audio device to your system output or Mixxx output (use a virtual cable if needed, e.g. BlackHole on Mac or VB-Cable on Windows).
6. Click **Play** in BUTT to start streaming.
7. In Mixxx, play tracks as normal; BUTT captures the audio.

## Audio Level Checklist
- Mixxx master output: peak around -6 to -3 dB.
- Microphone: clear, no clipping, use pop filter.
- Monitor only with headphones.
- Test for 5 minutes, then listen back on phone/laptop.

## Troubleshooting
- Connection refused → check host, port, password, and that the station is enabled in AzuraCast.
- No audio → verify audio device in BUTT/Mixxx and that tracks are playing.
- High latency → lower bitrate or check upload speed.
- Disconnects → test internet stability; keep a recorded backup playlist in AzuraCast AutoDJ.

## Private Test Procedure
1. Load 3–5 rights-cleared tracks in Mixxx.
2. Start stream.
3. Listen on a second device for 5 minutes.
4. Record the test (OBS or AzuraCast recording).
5. Note any issues and stop the stream.

Do not leave the stream public until cleared.