# Shadowrocket Custom Rules (Hong Kong AI & Ad Block)

A tailored Shadowrocket configuration based on [SR-Rule](https://github.com/pandit-psw/SR-Rule) designed for users in Hong Kong. It routes generative AI tools and TikTok through an external proxy node while keeping local traffic direct and blocking ads.

---

## What This Configuration Does

| Traffic Type | Destination Examples | Routing Policy |
| :--- | :--- | :--- |
| **Generative AI** | ChatGPT, Claude, Gemini, Copilot, Perplexity | `PROXY` (via assigned node) |
| **Restricted Media** | TikTok | `PROXY` (via assigned node) |
| **Advertisements** | Common telemetry, tracking, and ad servers | `REJECT` (blocked on-device) |
| **Local HK & Other** | Banking, government, local sites, standard web | `DIRECT` (full local speed) |

---

## Quick Setup (Shadowrocket iOS / iPadOS)

### 1. Import the Rule File
1. Copy the raw configuration link:
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
