<div align="center">

# Club Cam: Turn an Android Phone into a Wireless OBS Camera

**Free Android app that streams your phone camera over Wi-Fi to OBS as an RTSP source. Built for live pool and snooker table streams.**

[![Latest release](https://img.shields.io/github/v/release/Hrishank21s/club-cam-releases?label=latest%20APK)](https://github.com/Hrishank21s/club-cam-releases/releases/latest)
![Platform: Android](https://img.shields.io/badge/platform-Android%207%2B-3DDC84?logo=android&logoColor=white)
![Protocol: RTSP](https://img.shields.io/badge/stream-RTSP-0f172a)

**[⬇ Download the latest APK](https://github.com/Hrishank21s/club-cam-releases/releases/latest/download/app-release.apk)** · [All releases](https://github.com/Hrishank21s/club-cam-releases/releases)

</div>

---

## What it does

Club Cam runs an RTSP server on your phone. Open OBS on a computer on the same Wi-Fi, add the phone's address as a Media Source, and the phone becomes a wireless camera. No cables, no capture card, no extra software.

## Features

- **Live RTSP stream to OBS.** The app shows the exact `rtsp://<phone-ip>:8554/` address to paste into OBS.
- **Keeps streaming in the background.** Runs as a foreground service, so the stream survives the screen turning off or you leaving the app. Only the **Stop** button ends it.
- **Self-healing.** A watchdog checks every second and restarts a stalled camera, a dead encoder or a stopped server, then restores your lens and zoom.
- **Pick any lens.** Switch between the phone's rear, wide and ultra-wide cameras.
- **Zoom.** Pinch on the viewfinder, use the slider, or nudge with the +/- buttons.
- **Camera settings that match your phone.** Resolution, frame rate and bitrate lists are built from what that camera actually supports, so you cannot pick a combination it can't do.
- **Exposure lock.** Stops the picture getting brighter or darker when players lean over the table.
- **Touch lock.** One toggle disables every control so nobody changes the framing by accident.
- **Live status.** See LIVE/fps, how many OBS clients are connected, and the current resolution at a glance.
- **Stays awake.** Screen-on, Wi-Fi lock and wake lock keep the connection steady for hours.
- **Landscape, full-screen viewfinder** with immersive mode.

## Install

1. Download [`app-release.apk`](https://github.com/Hrishank21s/club-cam-releases/releases/latest/download/app-release.apk) on your Android phone.
2. Open it. You may need to allow "Install unknown apps" for your browser or file manager once.
3. Open **Club Cam** and allow Camera and Notifications.

To update, install the newer APK over the old one.

## Use with OBS

1. Put the phone and the OBS computer on the same Wi-Fi (or turn on the phone's hotspot and join it).
2. Open Club Cam. Wait for **● LIVE**.
3. In OBS: **Sources → + → Media Source**, untick **Local File**, paste the `rtsp://…:8554/` address shown in the app.
4. Tip: set Network Buffering low (0–1 MB) in OBS for the lowest delay.

## Specifications

| | |
|---|---|
| Platform | Native Android (Kotlin), Android 7.0+ (API 24) |
| Protocol | RTSP server on port 8554 |
| Video | Selectable resolution, fps and bitrate (Auto by default) |
| Audio | Video only |
| Permissions | Camera, Notifications, Wi-Fi state, Internet (local network only) |
| Distribution | Release APKs on GitHub Releases |

## About this repository

This repository hosts **official release builds only**. No source code is published here.
Built by [Hrishank Soni](https://hrishank21s.github.io). More projects on [GitHub](https://github.com/Hrishank21s).
