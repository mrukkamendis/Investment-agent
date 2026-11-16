# Investment Agent app: putting it on your phone

The app is a small website that installs to your home screen like a normal app. It runs on iPhone and Android. It downloads Binance's public price data directly on your phone and works out the signals there. There is no login, no API key, and no way for it to trade.

It needs to be hosted somewhere first. GitHub Pages does this for free and takes about 10 minutes once. A computer is easiest, but a phone works too.

## What's in the zip

| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Lets the phone install it as an app |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | Home-screen icons |
| `INSTALL.md` | This guide (no need to upload it) |

Unzip it first. On iPhone, tap the zip in the Files app. On Android, use Files by Google and tap Extract.

## Step 1: GitHub account

Go to **github.com** and sign up (free). Use any username: it becomes part of your app's address.

## Step 2: Make a repository

1. Tap **+** (top right), then **New repository**.
2. Name: `investment-agent`
3. Choose **Public**. Free GitHub Pages needs this. The code becomes publicly visible, but it holds nothing private: your settings and signal log stay on your phone.
4. Tick **Add a README file**, then tap **Create repository**.

## Step 3: Upload the files

1. On the repository page, tap **Add file**, then **Upload files**.
   On a phone, if you can't see "Add file", switch your browser to desktop view (Safari: **aA**, then **Request Desktop Website**; Chrome: **⋮**, then **Desktop site**).
2. Choose the six app files: `index.html`, `manifest.webmanifest` and the four `.png` files.
3. Tap **Commit changes**.

## Step 4: Turn on GitHub Pages

1. In the repository, open **Settings**, then **Pages** (left menu).
2. Under **Build and deployment**, set Source to **Deploy from a branch**, Branch to **main**, folder **/ (root)**, then **Save**.
3. Wait 1–2 minutes and refresh the page. It will show your address:
   `https://YOUR-USERNAME.github.io/investment-agent/`

## Step 5: Install it on your phone

Open that address on your phone.

- **iPhone (Safari):** tap the Share button, then **Add to Home Screen**.
- **Android (Chrome):** tap **⋮**, then **Install app** or **Add to Home screen**.

It now opens full-screen from its own icon.

## Using it

- **Signals:** opens automatically and reruns once per day after the daily close (05:30 Sri Lanka time). Tap **Refresh** any time.
- **Backtest:** how the same rules did in the past compared with simply holding.
- **Log:** every signal so far, kept on the phone. **Download CSV** saves it for Excel.
- **Settings:** portfolio size, risk limits, rule numbers, and the watchlist. **Browse TradFi contracts** lists everything Binance offers; tap to add.

## Updating the app later

When I send you a new `index.html`, open the repository on GitHub, tap **Add file**, then **Upload files**, choose the new file, and commit. The phone picks it up the next time the app opens. Your settings and log are kept.

## If something goes wrong

| What you see | Fix |
|---|---|
| "Could not reach Binance" | Check your internet. Some office and public Wi-Fi networks block Binance; try mobile data. |
| "Binance refused the connection (HTTP 451 or 403)" | Binance blocks some countries and networks. Try another connection. |
| GitHub shows a 404 page | Pages takes a few minutes the first time. Check that `index.html` is at the top level of the repository, not inside a folder. |
| The app shows old numbers | Tap **Refresh**. |
| Settings or log vanished | They are stored in the browser. Clearing Safari or Chrome data, or using private mode, wipes them. |

Things to remember: TradFi contracts on Binance are leveraged futures, not shares or gold you own. The app assumes no leverage, shows the funding cost of holding each one, and gives signals that are mechanical rule outputs, not predictions.
