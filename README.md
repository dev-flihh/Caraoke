# 🎤 Caraoke

Show synced lyrics on your Android Auto screen — without switching your music app.

Play music on Spotify or YouTube Music like you normally would. Caraoke reads 
the song, fetches the synced lyrics, and displays them on your head unit.
Just sing.

![Caraoke on Android Auto]
<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/8430cdc6-acfe-40b1-a701-f515e3517b6f" />

<img width="2880" height="1800" alt="image" src="https://github.com/user-attachments/assets/9ff42fae-d591-450d-8fbb-3d49720179d4" />
---

## Download

Head to [Releases](https://github.com/dev-flihh/caraoke/releases) 
to download the latest APK.

> Caraoke is in early access. Feedback is very welcome.

---

## How It Works

1. Play a song on Spotify, YouTube Music, or any music app that creates 
   an Android media notification
2. Caraoke reads the song info from your phone's media session
3. Synced lyrics appear on your Android Auto screen, following playback

Audio stays in your music app. Caraoke only handles the lyrics.

---

## Requirements

- Android phone
- Android Auto installed on your phone
- A car head unit that supports Android Auto
- A music app that provides an Android media notification
  (Spotify, YouTube Music, etc.)
- Internet connection (to fetch lyrics from LRCLIB)

---

## Setup (One Time)

**1. Install the APK**
Download from the Releases page. Enable "Install from unknown sources" 
on your phone, then install.

**2. Open Caraoke — Allow Notification Access**
Caraoke needs this to read what song is playing. It does not read 
your chats or personal notifications.

**3. Enable Android Auto Developer Mode**
Open Android Auto → tap "Version" several times until developer 
settings appear → enable "Unknown sources."

**4. Connect to Your Car**
Plug in your phone, open Android Auto launcher, select Caraoke. 
Play a song — lyrics will appear.

---

## Current Limitations

- Android Auto only (not Apple CarPlay)
- Lyrics availability depends on the [LRCLIB](https://lrclib.net) database
- If a song isn't in LRCLIB, the app will show "Lyrics not found"
- Not yet on the Google Play Store

---

## Lyrics Source

Caraoke fetches synced lyrics from [LRCLIB](https://lrclib.net) — 
an open source lyrics database. Thanks to everyone who contributes to it.

---

## Feedback & Bug Reports

Open an [Issue](https://github.com/dev-flihh/caraoke/issues) 
if you run into a bug or have a suggestion.
