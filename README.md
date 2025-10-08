# 🎧 Spotify TUI (naarvent_ version)

A fixed version of [Rigellute’s Spotify TUI](https://github.com/Rigellute/spotify-tui).  
Originally created by **Alexander Keliris**, now updated and improved by **naarvent_** for better compatibility and usability in 2025.

---

## 🧩 Description

**Spotify TUI** is a terminal-based user interface for Spotify, written in Rust.  
This fork/version updates outdated dependencies, fixes compatibility with the new `chrono` crate, and removes unsafe redirect behavior that Spotify now flags as insecure.

It allows you to:
- Connect directly to Spotify using the official **Spotify Web API**  
- Control playback, browse playlists, and search tracks from the terminal  
- Authenticate via a **localhost redirect URL** (`http://127.0.0.1:8888/callback`)  
- Store credentials locally in `~/.config/spotify-tui/client.yml`

---

## ⚙️ Features

✅ Spotify API integration (play, pause, next, previous, volume control, etc.)  
✅ Terminal interface powered by the [`tui-rs`](https://github.com/fdehau/tui-rs) crate  
✅ Fixed authentication flow with explicit port input  
✅ Dependency and build compatibility fixes for Rust 1.75+  
✅ Clean `Cargo.toml` and `chrono` patch for legacy support  
✅ Safe handling of tokens and user configuration files  

---

## 🧰 Installation

You’ll need Rust and Cargo installed:

```bash
# Clone this repository
git clone https://github.com/naarvent/spotify-tui-patched.git
cd spotify-tui-patched

# Build
cargo build --release
```

The executable will be created at:
```
target/release/spt.exe
```

---

## 🔑 Spotify API Setup

1. Go to [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/applications)  
2. Create a new app (Client ID + Secret)  
3. In the **Redirect URIs** section, add:
   ```
   http://127.0.0.1:8888/callback
   ```
4. Save your settings  
5. Run the program, and when prompted:
   - Paste your **Client ID**
   - Paste your **Client Secret**
   - Press Enter or type `8888` for the port  

---

## 🧼 Local Data

When the app runs, it creates a local config file at:

```
C:\Users\<user>\.config\spotify-tui\client.yml
```

To reset or remove personal credentials before sharing:
- Delete the folder:  
  ```
  C:\Users\<user>\.config\spotify-tui\
  ```

---

## 🧠 License

This project is licensed under the **MIT License**, with credits to:
- **Alexander Keliris (Rigellute)** – original author  
- **naarvent_** – 2025 modifications, build fixes, and redirect patch  

---

## 🚀 Notes

- The fixed version removes the forced localhost:PORT redirect bug.  
- Compatible with modern Spotify Web API authentication rules.  
- Fully buildable on **Windows 10/11** using Rust stable.  
- Future improvements may include UI refinements and updated crate dependencies.
