<h1 align="center"><p style="display: inline-flex; align-items: center; gap: 0.25em"><img style="width: 30px; height: 30px;" src="public/icons/favicon.png"> wplacer</p></h1>

<p align="center"><img src="https://img.shields.io/github/package-json/v/fangcognosphere/wplacer">
<a href="LICENSE"><img src="https://img.shields.io/github/license/fangcognosphere/wplacer"></a>
<a href="README.md"><img src="https://img.shields.io/badge/tradução-português_(brasil)-green"></a><//p>
<p align="center">An auto-drawing bot for [wplace.live](https://wplace.live/)</p>

## This project is for educational purposes only.

## Features ✅

- Simple and easy-to-use web UI for managing users and templates
- Supports multiple user accounts
- Automatic login and user info retrieval
- Template management: add, start, pause, and remove templates
- Automatically paints pixels according to templates
- Automatically buys ink charges (if enabled and possible)
- Handles Cloudflare (Turnstile) tokens via userscript
- Real-time status updates for each user/template

## Installation and Usage 💻
### Requirements:
- [Node.js and NPM](https://nodejs.org/en/download)
- [Tampermonkey](https://www.tampermonkey.net/)
- [git](https://git-scm.com/downloads) (not required)
### Installation:
1. [Install the userscript to manually solve Cloudflare Captchas](https://raw.githubusercontent.com/fangcognosphere/wplacer/refs/heads/main/public/wplacer.user.js)
2. Download the repository using [git](https://git-scm.com/downloads) (`git clone https://github.com/fangcognosphere/wplacer.git`) or download directly from GitHub (not recommended) 
3. In the terminal, install the dependencies with `npm i`
- If you'd like, you can change the host (local host only or all interfaces) and port of the local server in `.env`
### Usage:
1. To start the bot, simply use `npm start` or open file `start.bat`
2. After starting the bot, open the printed URL in your browser.
3. You can add as many users as you want.
   - In [wplace.live](https://wplace.live/), open DevTools (Inspect Element) or press F12, go to `Application` > `Cookies` and copy the values of the cookies named `s` and `j` (if they don't appear, try clicking/painting a pixel to trigger a request to the backend) (only older accounts have the `s` cookie so you can skip it).
   - Paste them into their respective spots on the "Add User" form.
4. After adding the users you want, go to "Add Template" and fill out the form for all users you want to use.
   - The coordinates are for the top-left corner of your image. I recommend using [BlueMarble](https://github.com/SwingTheVine/Wplace-BlueMarble) to get them; the coordinates will automatically appear once you click a pixel. Alternatively, you can go into the Network tab of DevTools, click any pixel, and look for a GET request to `https://backend.wplace.live/s0/pixel/{TX}/{TY}?x={PX}&y={PY}`.
   - Each user may only work on a single template at a time.
5. Finally, go to "Manage Templates" and click "Start All Templates" to start drawing.
   - The script will occasionally request that you paint a pixel in [wplace.live](https://wplace.live/). This is required to get the Turnstile token needed for painting pixels.

## Notes 📝

> [!CAUTION]
> This bot is not affiliated with [wplace.live](https://wplace.live/) and goes against its rules. I am not responsible for any sort of punishment against any of your accounts.

### To-dos ✅
- [ ] Add support for paid colors
- [ ] Auto-farm EXP and droplets function for users
- [ ] Easier multi-account support for one template
- [ ] Queueing system for multi-accounts
- [ ] Proxy support
- [ ] Support for painting between multiple tiles
- [ ] Automatic Turnstile solving (if possible)

### License 📜

[GNU AGPL v3](LICENSE)
