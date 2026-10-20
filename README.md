# Kingshot Recorder

Records Kingshot from your Android emulator at higher quality than OBS, and has a built-in **Blurrer** that hides the in-game Chat and Backpack screens in your videos before you share them.

On Windows it can also record a whole screen or a single window, and can record an emulator and your screen at the same time.

| | Version | Status |
|---|---|---|
| **Windows** | 1.0.3 | Current release, with automatic updates. **1.0.4 is planned for Friday 23 October 2026.** |

## Install on Windows

1. Download **KingshotRecorder-win-Setup.exe** from the [latest release](https://github.com/wlfkkkk/Kingshot-Recorder/releases/latest) and run it.
2. It installs for your user only, with no admin rights, and adds a Start menu and Desktop shortcut.
3. Windows may show "Windows protected your PC" because the installer is not signed. Click **More info** and then **Run anyway**.

Needs LDPlayer or BlueStacks with ADB access turned on in the emulator's settings.

## Updates

The app updates itself from this page's releases. Click the gear button and choose **Check for updates**. Only the changed files are downloaded, and your settings and videos stay as they are. The app never updates during a recording or a blur.

## Access key

On the first start the app asks for a key, which you get from the person who shared the app with you. It is asked once on each computer (and again if a later version changes the key). This is a simple gate to keep casual users out, not real protection.

## Record

1. Start your emulator and open Kingshot.
2. In Kingshot Recorder, pick the emulator (or, on Windows, a screen or window) to record.
3. Choose a **quality**: Small, Balanced, High, Very high or Maximum. High is the usual choice.
4. Press **Start recording**, play, and press **Stop & save** when you are done.

The video is encoded while you record, so saving at the end is quick. Recordings are saved to:

- Windows: `Videos\Kingshot Recorder\Original Videos`

You can change the folders in the gear panel.

## Blur

Open the **Blur** tab, tick the recordings you want to blur and start. The Blurrer:

- finds the Chat and Backpack screens in the video and blurs only the parts that show them, only while they are open;
- switches the blur on and off on the exact frame, so nothing leaks and nothing is blurred longer than needed;
- checks its own result frame by frame at every switch, and tells you if something is wrong;
- keeps finished parts if it is stopped, so you can resume later without starting over.

Blurred videos go to the **Blurred** folder next to your recordings. You can drag files onto the Blur tab. The sound is left out of the blurred video unless you tick **Keep sound**.

**Quality presets for the blurred video:** Tiny, Compact, Small, Balanced, High, Very high, Ultra and Maximum. Each is named by its approximate size per hour (1.5 GB/h up to 5 GB/h). High (3.5 GB/h) is the recommended one.

## Graphics cards

The encoder is chosen automatically. On Windows: **NVIDIA** (NVENC) first, then **AMD** (AMF), then **Intel** (QSV), and finally the **CPU**, which works on any PC but is much slower. On NVIDIA cards the scan also uses the GPU for decoding.

## Problems?

Every recording and blur writes a log. When you report a bug, send the log files from the **Logs folder** button in the gear panel. They show what the app saw and decided, plus your computer's specs and folder paths, so look them over before sharing.

---

Kingshot Recorder by wlfk - 685

Copyright (c) 2026 wlfk - 685. All rights reserved. Not open source: you may not copy, modify or redistribute this program or its code, with or without AI tools. See LICENSE.txt. The third-party programs it uses (FFmpeg, scrcpy, NumPy and others) keep their own licenses: see THIRD-PARTY-NOTICES.txt.
