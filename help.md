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

[Set up](#set-up) · [Use](#use) · [Settings](#settings) · [In Home Assistant](#in-home-assistant) · [Something wrong?](#something-wrong)

## Set up

You need Home Assistant reachable over **HTTPS** (for example Home Assistant Cloud) and your phone with **Garmin Connect** near the watch.

1. **Install the integration.** In Home Assistant, add [WristTalk](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) through HACS.
2. **Copy the address.** The integration's options show the address for the watches as a link. On a phone: tap it and copy it from the browser.
3. **Paste it in Garmin Connect.** WristTalk → Settings → **House address** → Save.
4. **Pair.** In Home Assistant: WristTalk → **Add watch**. Open WristTalk on the watch and confirm the code it shows.

The watch always talks to Home Assistant through your phone - also at home.

## Use

| | |
|---|---|
| **START** | Speak a command. Press again to send it at once. |
| **BACK** | Cancel a command. On the idle screen: close the app. |
| **UP / DOWN** | Scroll the conversation. |
| **Hold UP** | Text only on / off. |
| **Touch** | Drag to scroll. A tap only wakes the screen. |

## Settings

In Garmin Connect: WristTalk → Settings.

| Setting | What it does |
|---|---|
| **House address** | Where the watch finds your Home Assistant. |
| **Reconnect to the house** | Pairs the watch again from the start. Switches itself off afterwards. |
| **Listen as soon as it opens** | Opening the app starts listening at once. |
| **After a reply** | *Wait for START* or *Keep listening* for a conversation. Keep listening can take a nearby voice or radio for a command. |
| **Reply** | *Voice and text* or *Text only*. |
| **Reply volume** | Quiet, Medium or Loud. |
| **Text size** | Small or Large. |
| **Vibration** | *Full*, *Minimal* (reply and errors) or *Off*. |
| **Close when idle** | After this time the app asks *Stay?*, then closes. |

## In Home Assistant

Each watch has its own device card with three settings.

| Setting | What it does |
|---|---|
| **Assistant** | The Assist pipeline the watch uses. |
| **Finished speaking detection** | How soon a command ends after you stop. *Default* suits most. |
| **Reply voice quality** | *Fast* (default) arrives soonest. *Best* sounds better with headphones. |

## Something wrong?

| On the watch | What to do |
|---|---|
| **No connection to the phone** | Turn on Bluetooth and open Garmin Connect. |
| **The house address must start with https://** | Use an HTTPS address. Plain http:// does not work, not even at home. |
| **Update WristTalk on the watch** | Update the watch app. |
| **Update the WristTalk integration in Home Assistant** | Update the integration in HACS. |
| **I did not hear anything** | Press START and say it again. |
| **Pairing again** | The watch was removed in Home Assistant, or Reconnect was on. Use **Add watch**. |

Questions: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com) · [Privacy policy](../privacy/)
