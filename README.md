# Shadowrocket Custom Rules for Hong Kong

A lightweight Shadowrocket rule configuration designed to route generative AI platforms and TikTok through an external proxy node (such as Surfshark WireGuard) while keeping local Hong Kong traffic direct and blocking ads.

---

## Features

- **AI Tools via Proxy:** Routes ChatGPT, Claude, Google Gemini, NotebookLM, Apple Intelligence, and TikTok through your assigned proxy server.
- **Direct Local Traffic:** Domestic Hong Kong traffic, banking, and standard browsing connect directly at full local speed without proxy latency.
- **Built-in Ad Filtering:** Blocks common telemetry, analytics, and advertising domains at the device level.

---

## Quick Setup (Shadowrocket iOS / iPadOS)

### 1. Import the Rule File

1. Copy the raw configuration URL:
   ```text
   https://raw.githubusercontent.com/calebsze/SR-AI-Routing/main/HK_AI_AD.conf
   ```
2. Open **Shadowrocket** and select the **Config** tab at the bottom.
3. Tap the **+** icon at the top right.
4. Paste the URL and tap **Download**.
5. Tap the downloaded configuration in the list to select it (a checkmark will appear).

### 2. Add Your Proxy Node (Surfshark WireGuard Example)

1. In your **Surfshark Dashboard**, navigate to **VPN** &rarr; **Manual setup** &rarr; **WireGuard**.
2. Select a location outside Hong Kong (e.g., United States, Singapore, or Japan) and download the `.conf` file.
3. In Shadowrocket's **Home** tab:
   - Tap the **+** icon in the top right.
   - Set **Type** to **WireGuard**.
   - Input your server address, server public key, your private key, subnet IP, and port (`51820`), or open the downloaded `.conf` file directly using Shadowrocket.
4. Tap **Save**.

### 3. Activate Routing

1. On the **Home** tab, tap your proxy server node to select it.
2. Ensure **Global Routing** is set to **Config** (Rule-based routing).
3. Toggle the top switch to **Connected**.
