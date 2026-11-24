# Sources

## Device images

- iPhone 17 Pro, Deep Blue: [KPN product page](https://www.kpn.com/shop/mobiel/apple/iphone-17-pro-5g/deep-blue-1tb), [source PNG](https://images.ctfassets.net/m5g3wfd9m3nr/2qkS6bDS4QEQy8egQJJ8Gy/9f750c87fd8e7da061ee2ed030b38d71/iPhone_17_Pro_Deep_Blue_FrontBack.png).
- Google Pixel 6, Stormy Black: [Clove product page](https://www.clove.co.uk/products/google-pixel-6), [source PNG](https://www.clove.co.uk/cdn/shop/products/google-pixel-6-stormy-black-front-back_1200x.png?v=1665057482).
- MacBook Air M5, Midnight: Sketchfab render, [source JPEG](https://media.sketchfab.com/models/b5de6df714354099ac7678ca49ceb68c/thumbnails/1e3f519a0a4d4557bc91286409d782c7/blob.jpeg), provided by the profile's author. `macbook-air-m5-midnight.png` is that image with the grey background and its shadow removed (`_tools/matte.py`), cropped and scaled down.

Product images belong to their respective rights holders. They illustrate devices owned by this profile's author.

`devices-dark.svg` and `devices-light.svg` embed the iPhone and Pixel PNGs unchanged and the MacBook cut-out. The layout adds a background, labels and soft contact shadows; a vector clipping mask hides the white surround of the Pixel image. No generated device imagery is used.

## Telegram avatar

`telegram-avatar.jpg` is the public avatar of [t.me/weikton](https://t.me/weikton), taken from `https://t.me/i/userpic/320/weikton.jpg`. GitHub does not load external images inside SVG, so the JPEG is embedded into `link-telegram-dark.svg` and `link-telegram-light.svg` as `<image id="tg-avatar" href="data:image/jpeg;base64,...">`.

The workflow `.github/workflows/telegram-avatar.yml` refreshes it once a day (03:00 UTC, or by hand from the Actions tab). `.github/scripts/telegram_avatar.py` swaps only that image and commits as `github-actions[bot]`, and only when the avatar bytes have changed. When t.me answers with an error or its placeholder, nothing is changed.

## Type and icons

- Text in every SVG is converted to outlines from [JetBrains Mono](https://github.com/JetBrains/JetBrainsMono) 2.304, SIL Open Font License 1.1.
- Brand icons (Telegram, VK, Steam, NVIDIA, Intel and the stack) come from [Simple Icons](https://simpleicons.org) 16.30.0, CC0 1.0. The trademarks belong to their owners. Simple Icons has no Windows logo, so the OS and RAM rows use neutral glyphs.

Every card exists in two versions, `-dark.svg` and `-light.svg`; the README picks one with `<picture>` and `prefers-color-scheme`.
