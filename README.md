# DOSBox Cheat Engine

A modern, cross-platform, single-page web application to scan, edit, and freeze emulated memory in **DOSBox Staging (0.83+)**. Built as a direct response to the DOSBox Staging developer challenge!

![Screenshot of DOSBox Cheat Engine](https://placehold.co/800x400/2a2b3d/00ffcc?text=Replace+this+with+a+screenshot+of+the+app)
*(Place your screenshot here)*

---

## 🎯 The Challenge
In the release notes of DOSBox Staging 0.83, the developers introduced the new Web Server API with a challenge:
> *"HTTP API to muck around with the emulated memory and DOS internals to write modding and cheat tools as simple single-page web applications. The first one to reimplement Gold Box Companion using this API gets a prize!"*

**Challenge Accepted!**  
This tool provides a full Cheat Engine / GameConqueror style experience directly connected to your DOS games.

## ✨ Features
- **Cross-Platform:** Runs flawlessly on Windows, Linux, and macOS.
- **No Dependencies:** Built 100% with Python's standard library. No `pip install` required.
- **Familiar UI:** Search for values, filter results, and add addresses to a Cheat Table.
- **Value Freezing (Active):** Lock your health, ammo, or coins so they never decrease.
- **Smart Polling (Live Update):** Watch memory values change in real-time, with a toggle to pause background polling during CPU-heavy game segments (prevents game crashes during memory overlays).
- **Save/Load:** Export your cheat tables as JSON files and share them with others.
- **Range Selection:** Use Shift+Click and Ctrl+Click just like a traditional desktop file manager.

## 🚀 How to Use

### 1. Enable the DOSBox Staging API
You must be using **DOSBox Staging version 0.83 or newer**.
Open your `dosbox-staging.conf` file, locate the API section, and enable the web server:
```ini
[webserver]
webserver_enabled = on
```
*(By default, this runs on http://127.0.0.1:8086)*

### 2. Run the Cheat Engine
You have two options:
* **Option A (Executables):** Simply download the pre-compiled binary for your OS (Windows/Linux) from the [Releases page](../../releases) and double-click it.
* **Option B (Source code):** If you have Python installed, just run:
  ```bash
  python app.py
  ```

### 3. Cheat!
1. Start your DOS game.
2. The DOSBox Cheat Engine will automatically open in your browser.
3. Enter your current gold/health and click **First Scan**.
4. Go back to the game, change the value (spend gold, take damage).
5. Enter the new value and click **Next Scan**.
6. Select the remaining addresses and click **Add to Cheat Table**.
7. Double-click the value in the table to edit it, or check the box to **Freeze** it!

---

## 🛠️ Building from source (PyInstaller)
If you want to build the standalone executables yourself:
```bash
pip install pyinstaller
pyinstaller --onefile --noconsole app.py
```
*(Tip: To build a highly compatible Linux binary, build it on an older distribution like Ubuntu 20.04).*

## 👨‍💻 Architect
Created by **George Petrakis**.

## 📜 License
MIT License
