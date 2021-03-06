---
description: Utilize the STT and TTS services of a remotely hosted mycroft-core instance.
---

# Remote STT and TTS

{% hint style="warning" %}
This feature is experimental.
{% endhint %}

Enabling "Remote TTS" and "Remote STT" in the options make Mycroft-GUI act as a routing client for sending and receiving raw audio. This is intended to be used with a remotely hosted mycroft-core instance on the local network.

Please note, this is completely experimental. It is being worked on for running Mycroft-GUI on the hardware with limited on-board processing power such as the PinePhone, however it should work on any Linux system. 

### Requirements

You must have mycroft-core hosted on a different local machine. On the device running mycroft-core, you need:

* [Wave Client](https://github.com/AIIX/wave-client): should be installed in /mycroft/clients/wave/ and entries added to start it up in `start-mycroft.sh` and `stop-mycroft.sh`
* [Remote-STT Skill](https://github.com/AIIX/remote-stt)  
* [Remote-TTS Skill](https://github.com/AIIX/remote-tts) 
* Changes to your `mycroft.conf`: `{ "remote": true, "remote-server": "your.local.ipaddress.here" }` 

