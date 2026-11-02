---
layout: page
title: Privacy Policy
permalink: /privacy/
---

*Effective date: 2026-11-02.*

WristTalk is a voice assistant for [Home Assistant](https://www.home-assistant.io/) on a [Garmin](https://www.garmin.com/) watch. It has two parts:

- the **[WristTalk watch app](https://github.com/grzegorz-krzyzak/garmin-wristtalk#readme)** ([Connect IQ](https://developer.garmin.com/connect-iq/)), on your Garmin watch;
- the **[WristTalk integration](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme)**, which you install in your own Home Assistant.

WristTalk is made by me, Grzegorz Krzyżak.

## In short

- Your voice, what you say and the replies go **only to your own Home Assistant**, at the address you
  set. I run no server, and **neither I nor any other person or company** receives your data from
  WristTalk.
- No analytics, no advertising, no tracking, no accounts.
- What happens to your voice in Home Assistant depends on the [Assist](https://www.home-assistant.io/voice_control/) pipeline **you** chose (for
  example the speech-to-text, conversation agent and text-to-speech services you set up there).

## What the watch app handles

| Data | What for | Where it goes | How long |
|---|---|---|---|
| Your voice while you give a command (Ogg/Opus audio) | your command | your Home Assistant | the watch keeps it only for the command in progress |
| The recognised command and the reply (text and audio) | to show and play the reply | received from your Home Assistant | on screen until the app closes; not stored |
| Pairing key | to prove the watch to your Home Assistant | stored on the watch; Home Assistant stores only a hash of it | until you pair again or remove the app |
| House address and the app's settings | to reach your Home Assistant, your preferences | stored on the watch; edited in Garmin Connect, which passes them to the watch | until you change them or remove the app |
| A watch identifier, the watch model and the app version | to tell your watches apart when pairing | sent to your Home Assistant once, at pairing | kept in Home Assistant with the watch |

The watch identifier is the one Connect IQ gives each app on each watch; it is not your Garmin
account and it differs between apps.

The app records only for a command: when you press START, when you open the app (if "listen as soon
as it opens" is on - the default) and right after a reply (if "keep listening" is on). It stops when
the command ends, shows a recording dot meanwhile, and does not listen in the background.

## How the data travels

Connect IQ apps reach the internet through the **[Garmin Connect](https://connect.garmin.com/) app on your phone**, over
Bluetooth; from the phone the request goes over HTTPS to the address you set (for example your [Home
Assistant Cloud](https://www.nabucasa.com/) address). [Garmin's privacy policy](https://www.garmin.com/privacy/) covers the Garmin Connect app and the
watch - also the app's settings (among them your house address), which you edit in Garmin Connect
and Garmin passes to the watch.

## In your Home Assistant

The [WristTalk integration](https://github.com/grzegorz-krzyzak/ha-wristtalk#readme) runs in your Home Assistant and passes your command to the Assist pipeline
you chose for the watch. WristTalk itself keeps no recordings after a command: the audio and the
reply exist only while the command runs. Your Home Assistant may still keep data according to your
own settings - for example its logs, the conversation history of your agent, or debug recordings if
you turned them on - and the speech and AI services in your pipeline process your voice and text
under their own privacy policies. Those are your choices and are outside this app.

## Your rights

Because your data from WristTalk never reaches me, I hold nothing about you to give you access to,
correct or delete. Everything is in your own Home Assistant and with the providers you chose there -
ask them, or remove it there yourself.

## Sharing

Neither I nor any other person or company receives, sells or shares your data through WristTalk.
Nothing is sent anywhere except to the address you set - through the Garmin Connect app on your
phone, and from there on to the services you chose in your own Home Assistant.

## This website

This website is hosted on GitHub Pages; GitHub may log visitors' IP addresses - see the
[GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement).
The pages load nothing from other sites (no fonts, scripts or images from elsewhere) and use no
cookies.

## Children

WristTalk is not directed at children and collects nothing about anyone for me or anyone else.

## Changes and contact

Changes to this policy will be published at this address with a new date.

Privacy questions: [wristtalk.app@gmail.com](mailto:wristtalk.app@gmail.com).

Other questions and bug reports: [ha-wristtalk issues on GitHub](https://github.com/grzegorz-krzyzak/ha-wristtalk/issues)
(public).
