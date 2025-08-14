# Wplacer

## This project is for educational purposes only.

Wplacer is an auto-drawing bot for [wplace.live](https://wplace.live/).  
This project allows you to automatically draw pixel art on wplace using your account.


## Features

- Draw pixel templates automatically
- Supports multiple users
- Optionally auto-buy drawing charges
- Web interface for easy control

## How to Use
### 1. Install dependencies

```sh
npm install
```

### 2. Start the server

```sh
node index.js
```

The server will run on [http://localhost:4000](http://localhost:4000).

### 3. Get your cookies

1. Log in to [wplace.live](https://wplace.live) in your browser.
2. Open Developer Tools (`F12`).
3. Go to the **Application** tab.
4. Find your cookies for the site in `Cookies`:
    - `s` (session cookie)
    - `j` (JWT cookie)
5. Copy their values.

### 4. Use the web interface

1. Open [localhost:4000](localhost:4000) in your browser.
2. Upload your template and set coordinates.
3. Paste your cookies (`s` and `j`) into the form.
4. (Optional) Enable auto-buy charges if you want the bot to buy more drawing turns.
5. Click **Start** to begin auto-drawing.

### 5. Stop or monitor

- You can view active bot instances at `/instances`.
- Logs are saved for each user.

## Notes

- Your cookies must be valid and you must be logged in to wplace.
- If your cookies expire, you need to get new ones.

##
