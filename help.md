---
layout: page
title: Help
permalink: /help/
---

<script>
  // Polish phones get the Polish page, unless the reader chose English (?lang=en)
  if (!/[?&]lang=en/.test(location.search) && (navigator.language || "").toLowerCase().startsWith("pl")) {
    location.replace("../pl/help/" + location.hash);
  }
</script>

**English** · [Polski](../pl/help/)

## Setting up

1. **In Home Assistant:** install the [WristTalk integration](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) through HACS and add it. Pick the default Assist pipeline for new watches and the **address for the watches** - an `https://` address with a trusted certificate (for example Home Assistant Cloud). The integration's options show it in full, as a link: on a phone, tap it and copy it from the browser's address bar.
2. **In Garmin Connect** on your phone: the WristTalk app's settings → **House address** → paste the address → Save.
3. **In Home Assistant:** the WristTalk integration → **Add watch**. Pairing stays open for 5 minutes.
4. **On the watch:** open WristTalk. It shows a code - compare it with the one in Home Assistant and confirm.

The watch talks to Home Assistant through your phone (Garmin Connect must be running and the phone nearby) - also at home; the watch's Wi-Fi is not used.

## On the watch

| Button | What it does |
|---|---|
| **START** | Speak a command; START again sends it at once (otherwise the watch notices you stopped speaking). During a reply: stops it and listens again. |
| **BACK** | Cancels the command in progress; on the idle screen closes the app. |
| **UP / DOWN** | Scroll the conversation. |
| **Hold UP** | Text only on / off (the speaker icon at the top shows it). |
| **Touch** | Drag to scroll. A tap only wakes the screen - commands start with START. |

## Settings (Garmin Connect)

- **House address** - where the watch finds your Home Assistant: the address for the watches from the WristTalk integration, starting with `https://`.
- **Reconnect to the house** - switch on and save to pair the watch again from the start (a new house, a new address, or the watch was removed in Home Assistant). It switches itself off after pairing.
- **Listen as soon as it opens** - on: opening the app starts listening at once. Off: the app waits for START.
- **After a reply** - *Wait for START* (default), or *Keep listening* for a back-and-forth conversation. With *Keep listening*, a conversation or a radio nearby can be taken for a command.
- **Reply** - *Voice and text*, or *Text only* (no sound; also hold UP on the watch).
- **Reply volume** - Quiet, Medium, Loud.
- **Text size** - Small or Large text in the conversation.
- **Vibration** - *Full* (also when listening starts and the command is sent), *Minimal* (the reply and errors, default), *Off*.
- **Close when idle** - after this long without use the app asks "Stay?" for 10 seconds (START: stay, BACK: close), then closes.

## Each watch in Home Assistant

The watch's device card in Home Assistant has three settings:

- **Assistant** - the Assist pipeline this watch uses (speech-to-text, agent, voice).
- **Finished speaking detection** - how soon the command ends after you stop speaking. *Default* fits most; *Aggressive* can cut a command at a pause.
- **Reply voice quality** - *Fast* (default, the smallest file, arrives soonest through the phone), *Balanced*, *Best* (worth it with headphones).

## When something is wrong

- **"No connection to the phone"** - Bluetooth is off or Garmin Connect is not running on the phone.
- **"The house address must start with https://"** - Home Assistant must be reachable over HTTPS with a trusted certificate; plain `http://` does not work through the phone, also at home.
- **"Update WristTalk on the watch" / "Update the WristTalk integration in Home Assistant"** - the watch app and the integration speak different protocol versions: update the one named.
- **"I did not hear anything"** - say the command again after START.
- **The watch asks for pairing again** - it was removed in Home Assistant, or Reconnect was switched on: add it again with **Add watch**.

Questions: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com) · [Privacy policy](../privacy/)
