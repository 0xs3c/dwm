# dwm (Dynamic Window Manager) - `0xs3c/dwm`

## Project Overview

This repository hosts a customized build of the Dynamic Window Manager (dwm) tailored for enhanced desktop workflow and streamlined window management. It integrates essential community patches to improve usability, focus, and visual consistency, particularly focusing on client stacking, window control, and visual aesthetics.

---

## ✨ Feature Set (Applied Patches)

The following patches have been integrated and configured within this build to deliver a powerful and flexible environment:

| Feature | Purpose and Benefit | Keybindings |
| :--- | :--- | :--- |
| **Gaps Control (`fullgaps` & Toggle)** | Provides granular control over window spacing (10px default gaps) and a quick toggle for borderless/gapless maximization. | Toggle: `MODKEY` + `Shift` + `=` |
| **Scratchpad Utility** | A persistent, floating terminal client that can be instantly summoned or hidden, ideal for quick commands, monitoring, or note-taking. | Toggle: `MODKEY` + `` ` `` (Grave) |
| **Window Swallowing (`swallow`)** | Improves workflow by hiding the launching terminal when a GUI application (e.g., Firefox) is spawned, reducing screen clutter. | N/A (Automatic) |
| **Stack Reordering (`movestack`)** | Allows clients to be moved up or down the stack without changing their master/stack status, ensuring optimal client organization. | Move: `MODKEY` + `Shift` + `j` or `k` |
| **Focus-Driven Tag Display** | **(`hide vacant tags`)** Cleans up the bar by automatically hiding tags (workspaces) that contain no clients. | N/A (Automatic) |
| **Window Centering (`always center`)** | Ensures all newly spawned floating windows are centered on the screen for improved visual focus. | N/A (Automatic) |

---

## 🔑 Keybinding Quick Reference

| Category | Action | Keybinding |
| :--- | :--- | :--- |
| **Launch** | Dmenu Launcher | `MODKEY` + `p` |
| | Default Terminal | `MODKEY` + `Return` |
| | Toggle Scratchpad | `MODKEY` + `` ` `` |
| **Client Control** | Kill Focused Client | `Control` + `Escape` |
| | Focus Next/Previous | `MODKEY` + `j` or `k` |
| | Move Client in Stack | `MODKEY` + `Shift` + `j` or `k` |
| | Toggle Floating Mode | `MODKEY` + `Shift` + `space` |
| **Layout Control** | Toggle Bar Visibility | `MODKEY` + `b` |
| | Set Tiling Layout | `MODKEY` + `t` |
| | Set Floating Layout | `MODKEY` + `f` |
| | Set Monocle Layout | `MODKEY` + `m` |
| | Adjust Master Count | `MODKEY` + `i` or `d` |
| | Adjust Master Size | `MODKEY` + `h` or `l` |
| **Gaps Control** | Increase / Decrease Gaps | `MODKEY` + `=` or `-` |
| | Reset Gaps | `MODKEY` + `Shift` + `-` |
| **System** | Quit DWM Session | `MODKEY` + `Shift` + `q` |

---

## 📦 Installation and Build

### Prerequisites

Ensure the following dependencies and tools are installed on your system to compile and utilize this build:

* **Compiler:** `gcc`
* **Build Utility:** `make`
* **Xorg Libraries:** `libX11` and `libXft` headers (`libx11-dev`, `libxft-dev` or equivalents)
* **Utilities:** `xbacklight` and `pactl` (for media key functionality)
* **Terminal:** `st` (If using the default `termcmd`)

### Build Steps

To compile and install, execute the following commands in the repository directory:

```bash
# Clone the repository
git clone [https://github.com/0xs3c/dwm.git](https://github.com/0xs3c/dwm.git)

# Navigate to the source directory
cd dwm

# Compile the source and install the dwm binary to /usr/local/bin/
sudo make clean install
