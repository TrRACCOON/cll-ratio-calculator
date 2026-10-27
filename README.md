# CLL Ratio Calculator

A desktop ratio calculator for **Factorio 2.1 · Space Age**.

Pick what you want to produce and how much of it, and the calculator works out the whole production chain: how many machines you need, how many belts, which raw resources and how much power. It also helps you plan smelting columns, power plants and the equipment grid of your armor.

> **A personal hobby project.** This is not an official Factorio product. It is not sold, has no ads, asks for no donations and earns no money of any kind. Anyone is welcome to use it. See [Credits and disclaimer](#credits-and-disclaimer).

---

## Contents

- [Features](#features)
- [System requirements](#system-requirements)
- [Installation](#installation)
- [Updates](#updates)
- [Using the program](#using-the-program)
- [Uninstalling](#uninstalling)
- [Privacy](#privacy)
- [Troubleshooting](#troubleshooting)
- [For developers: building and releasing](#for-developers-building-and-releasing)
- [Credits and disclaimer](#credits-and-disclaimer)

---

## Features

The calculator has four pages, which you open from the bar at the top of the window.

### Production Chain
- **Target:** search the recipe list or pick one of your recent items.
- **Rate:** set the output per minute (quick buttons 30 / 60 / 120 / 300, or type a value). The per-second value is shown below it.
- **Machine tiers:** choose the assembler tier (1–3), the furnace type (stone, steel, electric) and the belt tier (yellow 15/s, red 30/s, blue 45/s, green 60/s).
- **Modules:** speed, productivity, efficiency and quality modules, with their effect on speed, energy, pollution and productivity. Productivity only applies to intermediate recipes, as in the game.
- **Production tree:** every step of the chain, with:
  - items per minute,
  - machines to build (rounded up) and the exact number of machines,
  - the load on the selected belt, with a marker at 50% (above that you need both lanes),
  - a whole-number machine ratio for the selected step and the steps after it,
  - the number of belts, when one is not enough.
- **Totals:** machines in total, broken down by machine type, plus the raw resources you need and the total electric power (average, including module effects).

### Mining & Smelting
- Choose the ore, the mining drill and the number of drills. The calculator gives you the ore output, the number of ore belts, and the coal and power the drills use.
- Plan the furnace columns: furnaces needed, furnaces per belt line and per row, inserters (including long inserters), and which belt lane limits the build.
- Three layouts:
  - one belt between two rows of furnaces, ore on one lane and coal on the other,
  - one belt per row,
  - two ore belts with a coal belt between them.
- Mining productivity research and modules are included in the result.

### Electricity
- Enter a power demand and choose a power source: **solar**, **steam**, **nuclear** or **fusion**.
- Solar results depend on the planet, which sets the solar strength and the day length.
- For steam you can choose the boiler fuel.
- You get a build list:
  - **Solar:** solar panels and accumulators.
  - **Steam:** boilers, steam engines, offshore pumps and fuel per minute.
  - **Nuclear:** reactors (including the neighbour bonus), heat exchangers, steam turbines and fuel cells per minute.
  - **Fusion:** fusion reactors, fusion generators and coolant.

### Armor
- Choose an armor and a planet. Then drag equipment into the grid, or click an item to place it in the first free slot.
- The power breakdown shows generation and maximum consumption for day and night, the balance, and whether your batteries get you through the night.

### Also in the program
- **A small calculator** for quick sums, opened from the button next to the page tabs.
- **Two languages:** English and German, selected with the globe button.
- **Settings are remembered:** the last page, your selections and the window size and position are restored the next time you start the program.

---

## System requirements

- Windows 10 or Windows 11, 64-bit.
- **Microsoft Edge WebView2 Runtime.** It is already installed on Windows 11 and on almost every up-to-date Windows 10 PC. If it is missing, you can get it free from Microsoft: <https://developer.microsoft.com/microsoft-edge/webview2/>
- About 10 MB of disk space.
- Administrator rights for installing, because the program goes into `C:\Program Files`.
- An internet connection is only needed for the update check. The calculator itself works offline.

---

## Installation

### The easy way: the setup file (recommended)

1. **Download the setup:**
   **[CLL-Ratio-Calculator-Setup.exe](https://github.com/TrRACCOON/cll-ratio-calculator/releases/latest/download/CLL-Ratio-Calculator-Setup.exe)**
   This link always points to the newest version.
2. **Double-click** the downloaded file.
3. **"Windows protected your PC" warning.** Because this is a free hobby project, the setup is not signed with a paid code-signing certificate, so Windows SmartScreen may warn you the first time. Click **More info** and then **Run anyway**.
4. **Confirm the Windows prompt** (User Account Control). It is needed to install into `C:\Program Files`.
5. **The CHILLLOUNGE installer opens:**
   1. **Location:** the default folder is `C:\Program Files\CHILLLOUNGE\Factorio Ratio Calculator`. Use **Browse…** to choose a different one. The installer shows how much space is needed and how much is free.
   2. Click **Install**. The progress bar and the log show what is being copied.
   3. **Done:** choose whether to start the program now and whether to create a desktop shortcut, then click **Finish**.

When the installation is finished you have:
- a **Start menu** entry called *Factorio Ratio Calculator*,
- a **desktop shortcut**, if you chose one,
- an entry under **Settings → Apps → Installed apps**, which you can use to uninstall.

If the program is already installed in the chosen folder, the installer shows **"Existing version found"** with the installed version and the new version. Click **Replace** to update. Your settings are kept.

### Manual installation from the ZIP

Every release also contains `CLL-Ratio-Calculator-<version>.zip`.

1. Download the ZIP from the [Releases page](https://github.com/TrRACCOON/cll-ratio-calculator/releases).
2. Extract it into any folder.
3. Double-click **`Install.bat`**. The same installer opens.

You can delete the extracted folder after the installation.

---

## Updates

The program checks for updates every time it starts. While it checks, the start window shows a running engineer and a short log.

**When no update is available**, the log shows *"No updates – vX is up to date"*. The calculator then loads and the main window opens.

**When an update is available**, it is installed automatically:
1. The new version is downloaded, and its SHA-256 checksum is checked so that a damaged download is never installed.
2. Windows asks once for administrator rights.
3. The program replaces its files, restarts itself and continues the log in the start window.
4. A backup of the old version is made first. If anything goes wrong, the old version is restored.

A few more details:
- **No internet:** the program simply starts without updating.
- **Declined or failed update:** if you say no to the Windows prompt, or an update fails, the program tries that update again after 24 hours instead of asking you on every start.
- **Version number:** the number shown next to the title at the top left is always the version you have installed.

> Versions before 1.2.2 show an **"Update available"** dialog instead. Click **Update now** once; after that, updates are installed automatically.

---

## Using the program

The window has no standard Windows frame. Everything is controlled from the calculator's own title bar:

| Action | How |
|---|---|
| Move the window | Drag an empty area of the top bar |
| Maximize / restore | Double-click the top bar |
| Resize | Drag the thin border around the window |
| Minimize | **—** button at the top right (or click the taskbar icon) |
| Close | **✕** button at the top right |

Links to websites open in your normal web browser.

---

## Uninstalling

Go to **Settings → Apps → Installed apps → Factorio Ratio Calculator → Uninstall** and confirm the Windows prompt.

This removes:
- the program folder,
- the Start menu entry and the desktop shortcut,
- the entry under *Installed apps*.

Your personal settings stay in `%LOCALAPPDATA%\CHILLLOUNGE\FactorioRatioCalculator`. Delete that folder as well if you want to remove everything.

---

## Privacy

- No account, no tracking, no advertising, no analytics.
- The only connection the program makes on its own is the update check. At startup it asks GitHub (`api.github.com`) for the newest release, and when there is an update it downloads it from `github.com`. No personal data is sent; GitHub only sees a normal web request.
- Settings and window position are stored only on your PC, in `%LOCALAPPDATA%\CHILLLOUNGE\FactorioRatioCalculator`.

---

## Troubleshooting

**Windows says "Windows protected your PC".**
Click **More info → Run anyway**. The setup is not signed (see [Installation](#installation)).

**"The window could not be started … Microsoft Edge WebView2 Runtime is required".**
Install the WebView2 Runtime from Microsoft (link under [System requirements](#system-requirements)), then start the program again.

**The installer does not open after I declined the Windows prompt.**
Administrator rights are needed to install into `C:\Program Files`. Start the setup again and confirm the prompt.

**The start window shows "Update server not reachable".**
There is no internet connection, or GitHub cannot be reached. The program starts normally without updating and checks again the next time it starts.

**The Start menu still shows an old icon after an update.**
Windows caches icons. Signing out and back in, or restarting the PC, fixes it.

**My settings from the browser version are gone.**
Older versions opened the calculator in your web browser. The desktop window keeps its own settings, so set your language and selections once more.

**I found a bug or have an idea.**
Please open an issue on GitHub: <https://github.com/TrRACCOON/cll-ratio-calculator/issues>

---

## For developers: building and releasing

Everything needed to build is already part of Windows: the C# compiler of .NET Framework 4.x and Windows PowerShell 5.1. No Visual Studio is needed.

### Project layout

| Path | Contents |
|---|---|
| `CLL Ratio Calculator <version>.html` | The calculator itself, as a single bundled HTML file. Its file name sets the version number. |
| `Install.ps1`, `Installer.xaml`, `Install.bat` | The graphical installer (WPF). It supports `-UpdateDir` and `-Silent -StateFile` for automatic updates. |
| `app\CalculatorWindow.cs` | The frameless main window, using WebView2 (the Edge engine). |
| `app\Splash.cs` | The start window ("console" design with the running engineer). |
| `app\Updater.cs` | The start sequence, the update check, the download and the checksum check. |
| `app\bridge.js` | Script injected into the page: window buttons, dragging the window, version number, "ready" signal. |
| `app\update-config.txt` | The GitHub repository used for updates (`owner/repository`). |
| `setup\` | Source of the single-file setup (`CLL-Ratio-Calculator-Setup.exe`). |
| `assets\`, `fonts\` | Icons, the logo, the engineer sprite sheet and the fonts. |
| `build-app.ps1` | Builds `app\Factorio Ratio Calculator.exe`. |
| `make-release.ps1` | Builds a complete release into `dist\`. |

### Publishing a new version

1. Put the new `CLL Ratio Calculator <version>.html` (for example `1.2.3`) in the project folder and remove the old one.
2. Run `make-release.ps1`. It writes three files to `dist\`:
   - `CLL-Ratio-Calculator-<version>.zip` – used by the automatic updater,
   - `CLL-Ratio-Calculator-<version>.zip.sha256` – the checksum of the ZIP,
   - `CLL-Ratio-Calculator-Setup.exe` – the single-file installer for new users.
3. On GitHub, create a new release:
   - tag `v<version>` (choose **"Create new tag on publish"**),
   - title `<version>`,
   - a short description of what changed.
4. Upload all three files and click **Publish release**. Do not mark it as a draft or pre-release, because those are ignored by the updater.

---

## Credits and disclaimer

### Factorio content

**Factorio** is a game by **Wube Software Ltd.** All Factorio-related content in this program belongs to Wube Software Ltd. and was **not created by me**. That includes:
- item, recipe, machine and equipment icons,
- sprites, including the running engineer in the start window,
- planet images,
- other game graphics,
- game names, terms and game data.

"Factorio" and related names and logos are trademarks of Wube Software Ltd. They are used here only to identify the game this tool is made for.

This project is **not affiliated with, endorsed by, sponsored by or connected to Wube Software Ltd.** in any way. Please do not contact Wube Software about this program.

If you hold rights to any of this material and would like something changed or removed, please open an issue on GitHub. I will take care of it straight away.

### A non-commercial personal project

I am a private person, and this is a personal hobby project:
- It is **not** sold or commercially marketed.
- It contains **no** advertising, paid features or donation requests.
- It does **not** generate any income or other revenue.

It is shared for free so that anyone can use it. There is no warranty of any kind; use it at your own risk.

### Third-party components

- **Titillium Web** and **JetBrains Mono** fonts – SIL Open Font License 1.1. The license texts are in `fonts\`.
- **Microsoft Edge WebView2 SDK** – © Microsoft Corporation. The license text is in `app\WebView2-LICENSE.txt`.
- **React** (bundled in the calculator page) – MIT License, © Meta Platforms, Inc. and affiliates.

### Made by

**CHILLLOUNGE** – TrRACCOON with help of AI
