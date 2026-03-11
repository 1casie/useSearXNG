# useSearXNG

A free, open source Safari extension that redirects your address bar searches to a [SearXNG](https://searxng.org) instance of your choice. Because paying $3.99 for a search redirector is insane.

Supports Google, DuckDuckGo, Bing, Yahoo, and Ecosia as source engines. Defaults to [searx.be](https://searx.be) but you can set any public or self-hosted SearXNG instance.

---

## Requirements

- macOS 12 or later
- Safari 15 or later
- [Xcode](https://apps.apple.com/app/xcode/id497799835) (free on the Mac App Store)

---

## Installation

Because this extension isn't on the Mac App Store (that costs $99/year, lol), you'll need to build it yourself from source. It sounds scary, it isn't.

### 1. Clone the repo

```bash
git clone https://github.com/1casie/useSearXNG.git
cd useSearXNG
```

### 2. Open in Xcode

Double-click `useSearXNG.xcodeproj`, or from terminal:

```bash
open useSearXNG.xcodeproj
```

### 3. Set your Team (optional but recommended)

In Xcode, click the project in the left sidebar → select the **macOS (App)** target → go to **Signing & Capabilities** → set Team to your personal Apple ID. This avoids some signing warnings.

### 4. Build and run

Make sure the scheme at the top of Xcode is set to **useSearXNG (macOS)**, then hit **Cmd+R**. A small app window will appear — that's normal, Safari extensions require a container app.

### 5. Enable the extension in Safari

Safari extensions built outside the App Store are considered "unsigned" and require a developer setting to be enabled. You'll need to do this **every time Safari restarts**:

1. Open **Safari → Settings → Advanced** and tick **"Show features for web developers"**
2. Go to **Safari → Develop → Allow Unsigned Extensions** ✓
3. Go to **Safari → Settings → Extensions** and toggle **useSearXNG** on

That's it. Search something and you'll land on SearXNG.

---

## Usage

By default, searches are redirected to [searx.be](https://searx.be).

To use your own instance:

1. Click the **useSearXNG icon** in the Safari toolbar
2. Enter your instance URL (e.g. `https://your.searxng.instance`)
3. Hit **Save**

Changes take effect immediately on your next search.

---

## A note on the "Allow Unsigned Extensions" thing

Yes, it's annoying that you have to re-enable this every time Safari restarts. This is Apple's way of ensuring only App Store-vetted extensions run by default.

The proper fix is **notarization**, which requires an Apple Developer account ($99/year). If you have one and want to help get this properly signed and distributed, please open an issue or a PR — it would mean users never have to touch the Develop menu again and the extension would persist across Safari restarts like a normal extension. It'd be massively appreciated. 🙏

---

## Supported search engines

These are the engines that will be intercepted and redirected:

- Google
- DuckDuckGo
- Bing
- Yahoo
- Ecosia

---

## License

The Unlicense.
