# 📡 Project Pulse | Standalone Server Telemetry Monitor

Project Pulse is a lightweight, zero-dependency background utility built to monitor system hardware performance and instantly stream critical alert thresholds directly to a designated Discord channel via Webhooks. Designed for game server administrators, homelab hobbyists, and DevOps engineers.

## ✨ Key Features
* 🚀 **Zero Installation:** Runs natively as a compiled `.exe` binary without requiring Python or pip dependencies on the host machine.
* ⚙️ **Automated Configuration:** Autogenerates a persistent, localized `config.ini` profile on its first execution loop.
* 📉 **Ultra Low Footprint:** Consumes minimal CPU cycles and memory overhead while actively polling system states.
* 🔒 **100% Private:** Operates entirely client-side. Your webhooks and system metrics never pass through a third-party server.

## 🛠️ How It Works
The script utilizes `psutil` to sample hardware utilization metrics at user-defined intervals. If data breaches your specified threshold profiles, the engine bundles the telemetric payload into a structured JSON packet and transmits it across Discord's secure REST API.

## 🚀 Quick Start Guide
1. Head over to the **Releases** tab on the right side of this repository and download the latest `Project_Pulse_v1.0.zip`.
2. Extract the folder anywhere on your machine.
3. Create a **Webhook URL** inside your target Discord channel's integration settings.
4. Open the generated `config.ini` file using any text editor and paste your webhook link:
   ```ini
   discord_webhook_url = [https://discord.com/api/webhooks/](https://discord.com/api/webhooks/)...
