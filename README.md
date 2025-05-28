# Calendr ⏳  
**Menu-bar calendar for macOS that shows only what you need – the next event and the countdown.**

[![Download](https://img.shields.io/badge/.dmg-Download-24292e?logo=apple)](https://github.com/conerst0ne/Calendr/releases/latest)
[![Release](https://img.shields.io/github/v/release/conerst0ne/Calendr)](https://github.com/conerst0ne/Calendr/releases/latest)

<p align="center">
  <img src="docs/demo-menubar.gif" width="700" alt="Calendr menubar demo">
  <br>
  <em>Stop alt-tabbing into Calendar just to know what's next.</em>
</p>

---

## ⚡ TL;DR
* **Zero distraction** – live countdown + next event in the menu bar.  
* **One-click actions** – *Remind in 5 / 15 / 30 min*, Skip, Maybe, Complete.  
* **Private & lightweight** – on-device only, idle <20 MB RAM, opens in <30 ms.  
* **100 % open source** – Swift 5.9, SwiftUI + AppKit, MIT.

---

## ✨ Key Features

|   |   |
| :-- | :-- |
| 💡 **Heads-up timer** | See exactly how many minutes until the next meeting without opening anything. |
| 🔔 **Smart snooze** | Shift an event’s alert to 5 / 15 / 30 min later with a single click. |
| ⏩ **Skip / Maybe** | Bail on that stand-up while you’re in flow – instantly updates the event via EventKit. |
| 📅 **Fast month view** | Hover or click for a full month grid & agenda (cold-open <30 ms thanks to SQLite cache). |
| 🛠 **CLI hooks** | `calendr --skip "Daily stand-up"` – perfect for automation and hotkeys. |
| 🔒 **On-device only** | Calendr never talks to the internet; no `URLSession` in the binary. |

---

## 🚀 Install

### Direct download
1. Grab the latest binary from the [releases page](https://github.com/conerst0ne/Calendr/releases/latest).  
2. Drag **Calendr.app** into **/Applications** and launch.

> **Requires macOS 11 or later** (Universal – Apple Silicon & Intel).

---

## 🤔 Why not just use Apple Calendar?

| Apple Calendar | **Calendr** |
| -------------- | ----------- |
| Open a whole window & hunt for “today”. | Lives in the menu bar. |
| No quick “Remind me in 15 min”. | One-click snooze. |
| Multiple dialogs to skip a meeting. | *Skip* button right on notification. |

---

## 🏗 Tech Stack
* **Language:** Swift 5.9  
* **UI:** SwiftUI dropdown + AppKit `NSStatusItem`  
* **Data:** EventKit ➜ CoreData (SQLite) cache  
* **CI:** GitHub Actions → codesign, notarise, upload ➜ Homebrew tap  
* **Tests:** XCTests on Bitrise (badge above)

Source is just ~2 kLOC – explore [`Sources/`](Sources/).

---

## 👥 Contributing

Bug reports, feature ideas, and PRs are ❤️.

```bash
git clone https://github.com/conerst0ne/Calendr.git
cd Calendr
open Calendr.xcodeproj   # Xcode 15+
```

1. Branch off **main**.  
2. `⌘-U` (or `make test`).  
3. Open a pull request with a descriptive title.

We especially need help with:

* Accessibility (VoiceOver flows)  
* Localisation – 🇨🇳 🇪🇸 🇫🇷 … add your language in under five lines

---

## 📈 Roadmap
- [ ] iCloud calendar colour sync  
- [ ] Natural-language create (“calendr add 'Lunch with Sam tomorrow 1 pm'”)  
- [ ] Optional busy-until menubar badge  

Vote 👍 on issues or open a new one!

---

<p align="center"><sub>Icons by SF Symbols. Not affiliated with Apple Inc.</sub></p>
