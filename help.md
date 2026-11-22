---
layout: page
title: Help
permalink: /help/
---

- [Set up](#set-up)
- [Use](#use)
- [Settings](#settings)
- [In Home Assistant](#in-home-assistant)
- [Questions](#questions)
- [Something wrong on the watch?](#something-wrong-on-the-watch)
- [Contact & support](#contact--support)

## Set up

You need Home Assistant reachable over **HTTPS** (for example Home Assistant Cloud) and your phone with **Garmin Connect** near the watch - the watch talks to your house through it.

1. **Install the integration.** In Home Assistant, add [WristTalk](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) from the Marketplace (Home Assistant 2026.11 or newer: Settings → Marketplace → **Add from link**) or through HACS.
2. **Copy the address.** The integration's options show the address for the watches as a link - copy it.
3. **Paste it in the Connect IQ app.** WristTalk → Settings → **House address** → Save.
4. **Pair.** In Home Assistant: WristTalk → **+ Add watch**. Open WristTalk on the watch and type the code it shows in Home Assistant. Pairing stays open for 3 minutes.

The watch always talks to Home Assistant through your phone - also at home.

## Use

| Button | What it does |
|---|---|
| **START** | Speak a command. Press again to send it at once. |
| **BACK** | Cancel a command. On the idle screen: close the app. |
| **UP / DOWN** | Scroll the conversation. |
| **Hold UP** | Menu: *Text only* on / off, *Pair again*, the app's version. |
| **Touch** | Drag to scroll. A tap only wakes the screen. |

**From the watch face:** add WristTalk to a Face It face or to a Connect IQ face that takes other apps' complications, then hold it to open WristTalk. Garmin's built-in faces do not take it (checked on the fēnix 8).

## Settings

In the Connect IQ app on your phone: WristTalk → Settings.

| Setting | What it does |
|---|---|
| **House address** | Where the watch finds your Home Assistant. |
| **Listen as soon as it opens** | Opening the app starts listening at once. |
| **After a reply** | *Wait for START* or *Keep listening* for a conversation. With *Keep listening*, the watch may take a conversation or a radio nearby for a command. |
| **Reply** | *Voice and text* or *Text only*. |
| **Reply volume** | Quiet, Medium or Loud. |
| **Vibration** | *Off*, *Minimal* (reply and errors) or *Full*. |
| **Close when idle** | After this time the app asks *Stay?*, then closes. |
| **Watch face text** | The text of WristTalk on a watch face, up to 12 characters. Empty: the icon alone. See [Questions](#questions) when the face keeps the old text. |

## In Home Assistant

Each watch has its own device card with three settings and a status.

| Setting | What it does |
|---|---|
| **Assistant** | The Assist pipeline the watch uses. |
| **Finished speaking detection** | How soon a command ends after you stop. *Default* suits most. |
| **Reply voice quality** | *Balanced* (default) sounds clear on the watch. *Fast* is smaller and a little rougher; *Best* is the largest. |
| **Status** | *Paired* or *Needs pairing again*. |

**Pair again:** the ⚙ next to the watch in the WristTalk integration. The watch and its settings stay; only its key changes.

## Questions

<details markdown="1">
<summary><b>Can I put WristTalk on my watch face?</b></summary>

Yes, on a **Face It** face (in the Connect IQ app) and on Connect IQ faces that take other apps' complications. Hold it on the face to open WristTalk - a tap does not open it. Garmin's built-in faces, the hot keys and the controls menu do not take Connect IQ apps (checked on the fēnix 8).

</details>

<details markdown="1">
<summary><b>The face shows nothing, or "--", where WristTalk should be.</b></summary>

Open WristTalk once after installing or updating it - the face gets its text then. Some faces show only the text, not the icon: with an empty *Watch face text* they show nothing.

</details>

<details markdown="1">
<summary><b>I changed the watch face text, but the face still shows the old one.</b></summary>

Open WristTalk (or any app) from the glance list or the app list, then go back to the watch face. Opening WristTalk by holding it on the face does not refresh the face.

</details>

<details markdown="1">
<summary><b>Why does the WristTalk icon look blurry in the Connect IQ app?</b></summary>

The phone enlarges the watch's small icon (30 × 30 pixels). On the watch it is sharp.

</details>

<details markdown="1">
<summary><b>Which watches does WristTalk work on?</b></summary>

The store page lists the watches it installs on. It is tested on a fēnix 8 Solar 51 mm. Would you like it on another watch? Ask through the store page.

</details>

## Something wrong on the watch?

What the watch says, and what to do.

<details markdown="1">
<summary><b>No connection to the phone</b></summary>

Turn on Bluetooth and open Garmin Connect.

</details>

<details markdown="1">
<summary><b>The house address must start with <code>https://</code></b></summary>

Use an HTTPS address. Plain `http://` does not work, not even at home.

</details>

<details markdown="1">
<summary><b>Update WristTalk on the watch</b></summary>

Update the watch app.

</details>

<details markdown="1">
<summary><b>Update the WristTalk integration in Home Assistant</b></summary>

Update the integration in the Marketplace (or HACS).

</details>

<details markdown="1">
<summary><b>I did not hear anything</b></summary>

Press START and say it again.

</details>

<details markdown="1">
<summary><b>Speech recognition in Home Assistant is not working</b></summary>

Press START and say it again. If it keeps coming back, check speech-to-text in your Assist pipeline in Home Assistant.

</details>

<details markdown="1">
<summary><b>Home Assistant cannot take the command right now - try again shortly</b></summary>

Home Assistant is restarting or reloading WristTalk, or its Assist pipeline failed. Press START in a moment. If it keeps coming back, check the Assist pipeline in Home Assistant, and that the watch is not disabled there (Settings → Devices & services → WristTalk → the watch: enable it).

</details>

<details markdown="1">
<summary><b>Command already sent</b></summary>

You pressed BACK after Home Assistant had your command: it runs anyway (a gate opens, a light turns on) - only the reply is not shown.

</details>

<details markdown="1">
<summary><b>Voice did not arrive</b></summary>

The reply is on the screen; only its voice is missing. If it keeps coming back, keep the phone near the watch and check text-to-speech in your Assist pipeline in Home Assistant.

</details>

<details markdown="1">
<summary><b>Voice cut off</b></summary>

The voice stopped midway - the whole reply is on the screen. Usually the phone lost the watch for a moment; keep it near.

</details>

<details markdown="1">
<summary><b>The watch shows a pairing code</b></summary>

After *Pair again*: in Home Assistant, the ⚙ next to the watch, or Settings → Repairs → **Fix**. The watch was removed in Home Assistant: **+ Add watch**. Then type the code from the watch. If the code is not typed within 3 minutes, the watch shows a new one. After 10 minutes the watch stops asking: *Pairing stopped* - press START to try again.

</details>

## Contact & support

- **Something not working?** [Report it on GitHub](https://github.com/grzegorz-krzyzak/ha-wristtalk/issues) - one place for the watch app and the integration. Do not paste your house address.
- **No GitHub account, a question or an idea?** Write to [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com).
- **WristTalk is free.** If it is useful to you, you can support it on [GitHub Sponsors](https://github.com/sponsors/grzegorz-krzyzak).
