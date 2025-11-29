<div align="center">

# 🎮 py-clash-bot

### *Automated Clash Royale Gameplay - Powered by AI*

[![Discord](https://img.shields.io/discord/YOUR_DISCORD_ID?color=7289da&label=Discord&logo=discord&logoColor=white)](https://discord.gg/nqKRkyq2UU)
[![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)](https://www.python.org/)
[![License](https://img.shields.io/badge/License-Open%20Source-green)](https://github.com/pyclashbot/py-clash-bot)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS-lightgrey)](https://github.com/pyclashbot/py-clash-bot)

**Open-source automation tool for Clash Royale** using advanced image recognition, intelligent card placement, and seamless Android emulation integration.

[**Download Latest Release**](https://github.com/pyclashbot/py-clash-bot/releases) • [**Join Discord**](https://discord.gg/nqKRkyq2UU) • [**Report Issues**](https://github.com/pyclashbot/py-clash-bot/issues)

---

</div>

---

## ✨ Features

<table>
<tr>
<td width="50%">

### ⚔️ **Battle Automation**

- **🏆 Trophy Road 1v1** - Climb the ladder automatically
- **🌟 Path of Legends** - Competitive ranked battles
- **👥 2v2 Matches** - Team battles with clanmates
- **🎲 Random Decks** - Auto-randomize before each battle
- **🧠 Smart AI**:
  - **Strategic Mode**: Intelligent elixir management with phase-based card selection
  - **Random Mode**: Fast mag-dump plays - randomly spam cards every 8 seconds for quick battles

</td>
<td width="50%">

### 🎁 **Rewards & Management**

- **💎 Card Mastery** - Auto-collect mastery rewards
- **⬆️ Card Upgrades** - Upgrade cards after battles
- **♻️ Deck Cycling** - Switch between 10 saved decks
- **📊 Real-time Stats** - Track W/L, chests, upgrades
- **⚙️ Smart Logic** - Skip fights when chests full

</td>
</tr>
</table>

### 🖥️ **Platform Support**

| Emulator | Windows | macOS | Notes |
|----------|---------|-------|-------|
| **Google Play Games** | ✅ | ❌ | Easiest setup, recommended for beginners |
| **MEmu 9.2.5.0** | ✅ | ❌ | Requires UEFI + Hyper-V in BIOS |
| **BlueStacks 5** | ✅ | ✅ | Cross-platform, stable performance |

---

## 🚀 Quick Start Guide

> **📋 Requirements:** Python 3.12+ • Android Emulator • 4GB RAM • Windows/macOS

### Step 1️⃣: Choose Your Emulator

<details open>
<summary><b>🎯 Google Play Games (Recommended - Easiest)</b></summary>

```powershell
# 1. Download from official site
https://developer.android.com/games/playgames/emulator

# 2. Install and complete Google sign-in
# 3. Accept USB debugging when prompted
# 4. Install Clash Royale from emulator
# 5. Complete tutorial manually
# 6. Close emulator
```

**✅ Pros:** Simple setup, official Google emulator  
**⚠️ Cons:** Windows only

</details>

<details>
<summary><b>💎 MEmu 9.2.5.0 (Advanced)</b></summary>

```powershell
# 1. Download MEmu 9.2.5.0
https://www.memuplay.com/

# 2. BIOS Requirements (CRITICAL)
- Enable UEFI
- Enable Hyper-V

# 3. Let bot auto-create "pyclashbot-96" VM
# 4. Install Clash Royale manually
# 5. Complete tutorial
# 6. Close MEmu
```

**✅ Pros:** Powerful, feature-rich  
**⚠️ Cons:** Requires BIOS configuration, hardware-intensive

</details>

<details>
<summary><b>🌟 BlueStacks 5 (Cross-Platform)</b></summary>

```powershell
# 1. Download BlueStacks 5 (NOT X/10)
https://www.bluestacks.com/

# 2. Let bot auto-create "pyclashbot-96" instance
#    OR manually create "Pie 64-bit" instance
# 3. Install Clash Royale
# 4. Complete tutorial
# 5. Close BlueStacks
```

**✅ Pros:** Works on Windows & macOS, stable  
**⚠️ Cons:** Slightly slower than MEmu

</details>

---

### Step 2️⃣: Install py-clash-bot

```powershell
# Clone or download the repository
cd py-clash-bot-master

# Install dependencies
py -m pip install -e .

# Launch the bot
py -m pyclashbot
```

---

### Step 3️⃣: Configure & Start

1. **Select Emulator Type** from dropdown
2. **Choose Fight Mode**: 1v1, 2v2, Trophy Road
3. **Enable Jobs** (optional):
   - ✅ Card Upgrades
   - ✅ Card Mastery Collection
   - ✅ Deck Randomization
4. **Select Play Style**:
   - 🧠 **Strategic**: Smart elixir management, phase-based tactics
   - 🎲 **Random**: Fast spam mode (mag-dump cards every 8s)
5. **Click START** 🚀

The bot handles everything: emulator restarts, battles, rewards, and deck management!

---

## 🎯 How It Works

### 🤖 Battle AI Modes

#### 🧠 **Strategic Mode** (Recommended)
Intelligent card placement with dynamic elixir management:

- **Phase Detection**: Adapts strategy based on battle time (early/single/double/triple elixir)
- **Smart Elixir Thresholds**: Probabilistic card selection based on current elixir count
- **Anti-Spam Logic**: Tracks recently played cards to avoid repetitive plays
- **Card Classification**: Groups cards by type (spell, tank, spawner, etc.) for optimal placement
- **Bridge Positioning**: Places troops at perfect offensive positions

**Example Strategy:**
```
Early Phase (0-60s):  Only play at 5-9 elixir (defensive)
Single Elixir:        Mixed aggression, 4-9 elixir plays
Double Elixir:        Increased aggression, 5-9 elixir focus
Triple Elixir:        Maximum pressure, 5-8 elixir spam
```

#### 🎲 **Random Mode** (Fast Grinding)
Speed-focused auto-play for rapid chest farming:

- **Mag Dump System**: Plays 1-3 random cards every 8 seconds
- **No Strategy**: Pure card spam for fastest battles
- **Quick Matches**: Ideal for chest slots/daily quests
- **Zero Delay**: Ignores elixir, just spams available cards

**Use Cases:**
- ✅ Grinding chests quickly
- ✅ Completing daily quests
- ✅ Trophy dropping
- ❌ Trophy pushing (use Strategic Mode)

---

## 🔧 Troubleshooting

<details>
<summary><b>⚠️ Google Play Games Issues</b></summary>

**Black screen / Won't boot:**
- Check for hidden browser popup (Google sign-in required)
- Try: System Tray → Google Play Games → Graphics Settings → Vulkan Override
- Run installer as admin: Task Manager → File → Run New Task → Browse to installer → "Run as admin"

**USB Debugging not working:**
- Restart emulator and watch for "Allow USB Debugging" prompt
- Accept the prompt immediately

</details>

<details>
<summary><b>⚠️ MEmu Issues</b></summary>

**Black screen / Won't render:**
- Switch render mode in bot GUI (Vulkan → DirectX → OpenGL)
- Enable UEFI in BIOS: [Video Guide](https://www.youtube.com/watch?v=uAMLGIlFMdI)
- Enable Hyper-V: [Microsoft Guide](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/get-started/install-hyper-v)

**Corrupted VM:**
- Delete "pyclashbot-96" VM from MEmu Multi-Instance Manager
- Restart bot to auto-create fresh VM

</details>

<details>
<summary><b>⚠️ BlueStacks 5 Issues</b></summary>

**Wrong BlueStacks version:**
- Ensure BlueStacks 5 (NOT BlueStacks X or 10)
- Install path should be: `C:\Program Files\BlueStacks_nxt`

**Instance creation failed:**
- Open Multi-Instance Manager
- Click "Instance" → "Fresh Instance" → "Pie 64-bit (Android 9)"
- Let bot rename it to "pyclashbot-96"

**Poor performance:**
- Try different render modes (OpenGL/DirectX/Vulkan)
- Allocate more RAM in BlueStacks settings

</details>

<details>
<summary><b>⚠️ Bot Not Detecting Game</b></summary>

**Clash Royale language:**
- Set game to **English** (required for image recognition)

**Screen resolution:**
- Bot expects 419x633 resolution (auto-configured)
- Don't manually resize emulator window

**Tutorial incomplete:**
- Complete the tutorial manually before starting bot

</details>

---

Having trouble with your emulator? This section provides troubleshooting tips for common issues with all supported emulators.

### BlueStacks 5 Emulator Debugging

- Use BlueStacks 5 only (BlueStacks 10/X are not supported)
- Ensure install path exists: `C:\Program Files\BlueStacks_nxt`
- If startup fails, create a clean "Pie 64-bit (Android 9)" instance in Multi-Instance Manager (no Google account yet), then click Retry in the bot so it can auto-configure
- Switch render mode in the bot (OpenGL/DirectX/Vulkan) if you see black screens or poor performance, then start again
- Fully close BlueStacks if it becomes unresponsive; the bot will relaunch it

### Google Play Games Emulator Debugging

- **Use the correct version** - Make sure you're using the DEVELOPER Google Play Games emulator, not the BETA version. Download it from [https://developer.android.com/games/playgames/emulator](https://developer.android.com/games/playgames/emulator)
- **Watch for login prompts** - Google Play makes a popup in your default browser for the Google sign-in prompt. Sometimes you might miss this during emulator boot, and it'll hang forever. If you're experiencing booting issues, check for a login prompt in a minimized browser window!
- **Adjust rendering settings** - If it's still not rendering properly, try adjusting render mode settings at System tray > Google Play Games emulator > Graphics settings > Vulkan device override OR Graphics > Graphics stack override
- **Installer download fix** - If you're having trouble downloading the emulator installer, this tested solution works: Open your task manager, click File, press "Run new task", drop the installer path, and press "Run as admin"

### MEmu Emulator Debugging  

- **Hardware requirements** - MEmu is more hardware intensive, so if you're on a low-end machine try using Google Play Games emulator instead
- **Black screen or boot issues** - If it's showing a black screen or never fully booting, try adjusting render mode via the ClashBot settings, then start the bot to apply those settings
- **BIOS requirements** - MEmu REQUIRES your BIOS to have UEFI and Hyper-V enabled!
  - Enable UEFI: [https://www.youtube.com/watch?v=uAMLGIlFMdI](https://www.youtube.com/watch?v=uAMLGIlFMdI)  
  - Enable Hyper-V: [https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/get-started/install-hyper-v?tabs=powershell&pivots=windows](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/get-started/install-hyper-v?tabs=powershell&pivots=windows)
- **Version conflicts** - Some old versions of pyclashbot create corrupt instances of MEmu. If you're switching between versions and MEmu is breaking, try deleting your existing MEmu VMs, or reinstalling MEmu entirely

## 🎯 Demo

<div align="center">

<table>
<tr>
<td width="50%">
<img src="https://github.com/pyclashbot/py-clash-bot/blob/master/assets/demo-game.gif?raw=true" width="100%" alt="Game Demo"/>
<p align="center"><i>🎮 Battle automation in action</i></p>
</td>
<td width="50%">
<img src="https://github.com/pyclashbot/py-clash-bot/blob/master/assets/demo-gui.gif?raw=true" width="100%" alt="GUI Demo"/>
<p align="center"><i>🖥️ User interface and controls</i></p>
</td>
</tr>
</table>

</div>

---

---

## 🤝 Contributing

We welcome contributions from the community! Whether you have ideas for new features, bug reports, or want to help with development:

<table>
<tr>
<td align="center" width="25%">
<br>
<b>🐛 Report Issues</b><br><br>
Found a bug?<br>
<a href="https://github.com/pyclashbot/py-clash-bot/issues">Open an Issue</a>
<br><br>
</td>
<td align="center" width="25%">
<br>
<b>💡 Feature Requests</b><br><br>
Have an idea?<br>
<a href="https://github.com/pyclashbot/py-clash-bot/issues">Suggest a Feature</a>
<br><br>
</td>
<td align="center" width="25%">
<br>
<b>💻 Code Contributions</b><br><br>
Want to code?<br>
<a href="CONTRIBUTING.md">Contributing Guide</a>
<br><br>
</td>
<td align="center" width="25%">
<br>
<b>💬 Community Support</b><br><br>
Help others!<br>
<a href="https://discord.gg/nqKRkyq2UU">Join Discord</a>
<br><br>
</td>
</tr>
</table>

---

## ⚠️ Disclaimer

**Educational & Automation Purposes Only**

This tool is designed for educational purposes and personal automation. Please ensure you comply with Clash Royale's Terms of Service. The developers are not responsible for any consequences resulting from the use of this software, including but not limited to account bans or suspensions.

**Use at your own risk.** Bot usage may violate Supercell's Terms of Service and could result in account penalties.

---

<div align="center">

**Made with ❤️ by the py-clash-bot community**

*Automate your Clash Royale experience and focus on what matters most - strategy and fun!*

[![Star this repo](https://img.shields.io/github/stars/pyclashbot/py-clash-bot?style=social)](https://github.com/pyclashbot/py-clash-bot)
[![Fork this repo](https://img.shields.io/github/forks/pyclashbot/py-clash-bot?style=social)](https://github.com/pyclashbot/py-clash-bot/fork)

[⬆ Back to Top](#-py-clash-bot)

</div>
