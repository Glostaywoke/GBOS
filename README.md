# GBOS ROM Patcher

A browser-based string and palette editor for the **GBOS** firmware used on the **EverDrive GB Rev.H Pro+** flash cartridge.

**Live tool:** [glostaywoke.github.io/GBOS](https://glostaywoke.github.io/GBOS/)

---

## What it does

Lets you patch the GBOS firmware ROM directly in your browser — no install, no server, no data ever leaves your machine.

**String patches (70+ fields across 8 tabs):**
- All menu and navigation labels
- Cheats / code menu strings
- Save RAM menu labels
- About screen (cart name, developer credit, email, URL, button hints)
- Device info and cart info screen labels
- Mapper type names and ROM size strings
- System paths, file extensions, option values, separator line, error message
- ROM header title
- Boot splash strings

**Color patches:**
- CGB palette — 4-color RGB picker with live preview and 10 preset themes
- DMG palette — grayscale shade mapping for original Game Boy hardware

**Tools:**
- Arbitrary byte patcher (offset + hex bytes)
- Header checksum auto-repair (runs on every build)
- Hex viewer

---

## How to use

1. Open the [live page]https://glostaywoke.github.io/GBOS/ (or open `index.html` locally)
2. Drop your `GBOS.GB` file onto the upload area
3. Edit strings and colors across the tabs
4. Click **Build Patched ROM**
5. Right-click the download link → **Save link as...**
6. Flash the patched file using the standard EverDrive OS update procedure

---

## Running locally

No build step. Just open `index.html` in any modern browser.

```
git clone https://glostaywoke.github.io/GBOS/
cd gbos-patcher
open index.html
```

---

## Verified offsets

All patch offsets are verified against **GBOS.GB Rev.00 (32KB, ROM-ONLY mapper)**.  
If you have a different revision the string addresses may differ — use the hex viewer tab to inspect before patching.

---

## Credits & disclaimer

**GBOS firmware** © [I. Golubovskiy / krikzz](http://krikzz.com)  
This tool is an **unofficial fan project** and is not affiliated with or endorsed by Krikzz in any way.  
All firmware rights belong to their respective owner.  
Use at your own risk. Always keep a backup of your original GBOS.GB.

---

## License

The patcher tool itself (HTML/CSS/JS) is released under the [MIT License](LICENSE).  
The GBOS firmware it patches is **not** covered by this license.
