# Tmux Configuration Guide

This directory contains a customized and documented Tmux configuration (`tmux.conf`). Below is an explanation of the custom shortcut keybindings, behavioral configurations, and appearance customizations.

---

## 🚀 Getting Started

To use this configuration, copy `tmux.conf` to your home directory:

```bash
cp tmux/tmux.conf ~/.tmux.conf
```

If you are already inside a Tmux session, you can reload the configuration using the reload shortcut:
* **`Ctrl-x` followed by `r`**

---

## ⌨️ Custom Keybindings

This configuration overrides several default Tmux keybindings to provide an easier and faster navigation experience.

### 1. The Prefix Key
* **Default:** `Ctrl-b`
* **Custom:** `Ctrl-x` (Press `Ctrl-x` before executing any Tmux command)

### 2. Pane Navigation & Splitting
Panes divide your window into multiple terminal regions.

| Action | Shortcut | Description |
| :--- | :--- | :--- |
| **Split Side-by-Side** | `Ctrl-x` then `v` | Split current pane horizontally |
| **Split Top-and-Bottom** | `Ctrl-x` then `h` | Split current pane vertically |
| **Navigate Left** | `Alt + Left Arrow` | Focus pane on the left (No prefix required) |
| **Navigate Right** | `Alt + Right Arrow` | Focus pane on the right (No prefix required) |
| **Navigate Up** | `Alt + Up Arrow` | Focus pane above (No prefix required) |
| **Navigate Down** | `Alt + Down Arrow` | Focus pane below (No prefix required) |

### 3. Window Navigation & Management
Windows are like tabs in a browser.

| Action | Shortcut | Description |
| :--- | :--- | :--- |
| **Previous Window** | `Shift + Left Arrow` | Switch to the window on the left |
| **Next Window** | `Shift + Right Arrow` | Switch to the window on the right |
| **Swap Window Left** | `Alt + Shift + Left Arrow` | Move current window one slot to the left |
| **Swap Window Right** | `Alt + Shift + Right Arrow` | Move current window one slot to the right |

---

## ⚙️ Core Configuration & Options

* **Mouse Mode:** `set -g mouse on`  
  Enables mouse interactions. You can click to select panes, drag pane borders to resize them, and scroll through history.
* **Auto Rename Window:** `set-window-option -g automatic-rename on`  
  Automatically renames the window tab to show the running command (e.g., `vim`, `npm`, `bash`).
* **Activity Monitoring:** `setw -g monitor-activity on`  
  Highlights the window tab in the status bar when activity is detected in a background window.

---

## 🎨 Visual Theme & Status Bar

The status bar has a custom color scheme (primarily black, blue, and green colors):

* **Left Status Bar:** Displays the current logged-in user and the machine's hostname: `[ username | hostname ]`
* **Right Status Bar:** Displays the current date and time: `[ DD-MMM-YYYY | HH:MM AM/PM ]`
* **Center:** Lists current active and background windows.
  * Active window is highlighted in **bold with a blue background**.
  * Windows with pending activity alerts are highlighted in **white with a dark background**.
