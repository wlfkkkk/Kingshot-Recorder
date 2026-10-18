# Kingshot Recorder

A Windows app that records your Android emulator (LDPlayer or BlueStacks) at higher quality than OBS, and has a built-in **Blurrer** that hides the in-game chat and Backpack screens in your videos before you share them.

It also records a whole screen or a single window, and can record an emulator and your screen at the same time.

## Install

1. Download **KingshotRecorder-win-Setup.exe** from the [latest release](https://github.com/wlfkkkk/Kingshot-Recorder/releases/latest) and run it.
2. It installs for your user only, with no admin rights, and adds a Start menu and Desktop shortcut.
3. Updates are automatic: click the gear button and choose **Check for updates**. Only the changed files are downloaded, and your settings and videos stay as they are.

Windows only. Needs ADB access enabled in the emulator's settings.

## Record

1. Start your emulator (LDPlayer or BlueStacks) and open Kingshot.
2. In Kingshot Recorder, pick the emulator (or screen / window) to record.
3. Choose a **quality**: Small, Balanced, High, Very high or Maximum. High is the usual choice.
4. Press **Start recording**, play, and press **Stop & save** when you are done.

Recordings are saved to `Videos\Kingshot Recorder\Original Videos`. The video is encoded while you record, so saving at the end is quick. You can change the folders in the gear panel.

## Blur

Open the **Blur** tab, tick the recordings you want to blur and start. The Blurrer:

- finds the Chat and Backpack screens in the video and blurs only the parts that show them, only while they are open;
- switches the blur on and off on the exact frame, so nothing leaks and nothing is blurred longer than needed;
- checks its own result frame by frame at every switch, and tells you if something is wrong;
- keeps finished parts if it is stopped, so you can resume later without starting over.

Blurred videos go to `Videos\Kingshot Recorder\Blurred`. You can drag files onto the Blur tab, and the sound is kept unless you turn it off.

**Quality presets for the blurred video:** Tiny, Compact, Small, Balanced, High, Very high, Ultra and Maximum. Each is named by its approximate size per hour (1.5 GB/h up to 5 GB/h). High (3.5 GB/h) is the recommended one.

## Graphics cards

The encoder is chosen automatically: **NVIDIA** (NVENC) first, then **AMD** (AMF), then **Intel** (QSV), and finally the **CPU**, which works on any PC but is much slower. On NVIDIA cards the scan also uses the GPU for decoding.

## Problems?

Every recording and blur writes a log. When you report a bug, send the log files from the **Logs folder** button in the gear panel. They show what the app saw and decided, plus your PC's specs and folder paths, so look them over before sharing.

---

Kingshot Recorder by wlfk - 685
