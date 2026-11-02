# Kingshot Recorder

Records Kingshot from your Android emulator at higher quality than OBS, and has a built-in **Blurrer** that hides the in-game chat in your videos before you share them.

It can also record a whole screen or a single window, and can record an emulator and your screen at the same time. Windows only.

| | Version | Status |
|---|---|---|
| **Windows** | 2.0.2 | Current release, with automatic updates. |

## Install

1. Download **KingshotRecorder-win-Setup.exe** from the [latest release](https://github.com/wlfkkkk/Kingshot-Recorder/releases/latest) and run it.
2. It installs for your user only, with no admin rights, and adds a Start menu and Desktop shortcut. The installed program is about 110 MB.
3. Windows may show "Windows protected your PC" because the installer is not signed. Click **More info** and then **Run anyway**.

**You need:** Windows 10 or 11 (64-bit), and LDPlayer 9 or BlueStacks 5 with ADB turned on in the emulator's settings. A graphics card is optional (see below).

## Updates

The app updates itself from this page's releases. Click the gear button and choose **Check for updates**. Only the changed files are downloaded (a typical update is a few hundred KB to a few MB), and your settings and videos stay as they are. The app never updates during a recording or a blur.

## Access key

On the first start the app asks for a key, which you get from the person who shared the app with you. It is asked once on each computer (and again if a later version changes the key). This is a simple gate to keep casual users out, not real protection.

## Record

1. Start your emulator and open Kingshot.
2. In Kingshot Recorder, pick the emulator, a screen or a window to record. You can record two sources at once (for example an emulator and the whole screen).
3. Choose a **quality**: Small, Balanced, High, Very high or Maximum (about 3 to 13.5 GB per hour). High is the usual choice.
4. Press **Start recording**, play, and press **Stop & save** when you are done.

The video is encoded while you record, so saving at the end is quick. If the screen capture is lost (a lock screen, a security prompt), the app restarts it by itself and tells you which part has no picture. After saving, a small window asks **"What gamemode were you in?"** and names the video for you, for example `Swordland_31.10.2026` (you can skip it or switch it off). Recordings older than 24 hours move into an **Old Videos** folder by themselves (also switchable).

Recordings are saved to `Videos\KSR Original`, and blurred videos to `Videos\KSR Blurred`. You can change the folders in the gear panel. The PC stays awake while you record or blur (the screen may still turn off).

## Blur

Open the **Blur** tab, tick the recordings you want to blur and start. The Blurrer:

- finds the chat in the video (the chat screen, the bar at the bottom, and the Tri-Alliance Clash chat) and blurs only the parts that show it, only while it is visible; pop-up cards stay sharp while the chat beside them is blurred;
- switches the blur on and off on the exact frame, so nothing leaks and nothing is blurred longer than needed;
- checks its own result in every frame of the finished video, and re-blurs a spot by itself if it finds one;
- shows each step with its own bar and time left, and a **Notes** button next to each blurred video opens a short report: a clear verdict first (safe to upload or not, with the times to look at), then what was done;
- keeps finished parts if it is stopped, and asks whether to continue or start over;
- works on emulator recordings and on phone recordings (including iPhone and long recordings with a changing frame rate).

Blurred videos go to the **KSR Blurred** folder. The check reports are kept in the Logs folder (in a `reports` subfolder), so the folder you upload from holds only videos. You can drag files onto the Blur tab. The sound is left out of the blurred video unless you tick **Keep sound**. Nothing is ticked for you: you choose which videos to blur.

**Quality presets for the blurred video:** Tiny, Compact, Small, Balanced, High, Very high, Ultra and Maximum. Each is named by its approximate size per hour (1.5 GB/h up to 5 GB/h). High (3.5 GB/h) is the recommended one.

## Graphics cards

The encoder is chosen automatically: **NVIDIA** (NVENC) first, then **AMD** (AMF), then **Intel** (QSV), and finally the **CPU**, which works on any PC but is much slower. On NVIDIA cards the scan and the emulator recordings also use the GPU for decoding. While other programs keep your PC busy, the Blurrer uses fewer parts at once so the PC stays smooth.

## Problems?

Every recording and blur writes a log. When you report a bug, send the log files from the **Logs folder** button in the gear panel. They show what the app saw and decided, plus your computer's specs and folder paths, so look them over before sharing.

---

Kingshot Recorder by wlfk - 685

Copyright (c) 2026 wlfk - 685. All rights reserved. Not open source: you may not copy, modify or redistribute this program or its code, with or without AI tools. See LICENSE.txt. The third-party programs it uses (FFmpeg, scrcpy, NumPy and others) keep their own licenses: see THIRD-PARTY-NOTICES.txt.
