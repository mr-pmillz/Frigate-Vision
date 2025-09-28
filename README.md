# Frigate-Vision
---
<sup>**Firstly, credit where credit is due!** A lot of this automation was inspired and even copied from both @SgtBatten's [Frigate notification Blueprint](https://community.home-assistant.io/t/frigate-mobile-app-notifications-2-0/559732) and @valentinfrlch's [LLMVision Blueprint](https://llmvision.gitbook.io/getting-started/setup/blueprint). If anyone has an issue with content or code, please reach out.</sup>

[After sharing a screenshot](https://www.reddit.com/r/homeassistant/comments/1lohkx9/my_take_on_a_frigatellm_vision_notification/) of one of my Frigate automations the other day, a few of you asked if I had a blueprint. At the time I didn’t… so I sat down, taught myself how to build one and here it is!

Introducing **Frigate Vision**; a blueprint designed to bring intelligent notifications and AI object recognition to your Home Assistant setup, powered by Frigate, LLMVision, and Home Assistant.

---

**📄 Get the Blueprint:**

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmr-pmillz%2FFrigate-Vision%2Fblob%2Fmain%2Ffrigate_vision.yaml)

---
[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://buymeacoffee.com/zacharyd3)
#### 💡 What Frigate Vision Does

* **🚨 Listens for new Frigate detection events** from any camera you choose using MQTT
* **🧠 Integrates with LLMVision** to enrich notifications with event summaries
* **🕒 Enforces per-camera cooldowns** so you’re not spammed when a squirrel does laps in your yard
* **📱 Pushes mobile notifications** with custom text, camera names, and optional sublabels (e.g., who or what was recognized)
* **🧩 Uses input helpers** so you can easily reuse this blueprint across cameras without editing YAML
* **🎛️ Multiple notification devices** now available
* **🐛 Debug mode** lets you preview all variables and logic without sending notifications

---

### 🛠️ Why I Built It:
I’ve used @SgtBatten’s reworked Frigate notifications for years and finally decided to break it down and recreate it to my liking. It started out as a fun project, but once I discovered **LLMVision** and the ability to generate dynamic event summaries from clips, I was *hooked*.

I’ve since spent time crafting what I felt was the ultimate smart notification setup for me. The blueprint includes 3 built-in notification actions and is currently optimized for Android (with iOS support planned). This is still a **beta version**, but it’s what I’d call *mostly complete*—and I’m already planning to add more customization options like SgtBatten’s original in future releases.


---

### ⚙️ Requirements:

* [Frigate installed](https://docs.frigate.video/integrations/home-assistant/) with MQTT events enabled
* [LLMVision](https://llmvision.org/) installed and configured
* Home Assistant mobile app (for push notifications)
* An input_boolean helper for multi-camera queuing
* A dashboard to use as a landing page ( LLMVision event summary suggested )

---

### 🧠 TL;DR:

**Frigate Vision** makes your HA notifications smarter by blending real-time detection with AI object recognition and smart logic; all wrapped in one reusable, configurable blueprint.

---

I’d love your feedback, ideas, bug reports (via github please), and feature requests. If you use it and like it, drop a comment; let’s make Frigate Vision even smarter!
