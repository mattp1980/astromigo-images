# AstroMigo hosted Messier images

This folder contains 35 pre-optimized JPEG files. All files are below 85 KB and fit within 350×320 pixels. **They are not guaranteed to decode on the ESP32 until hardware tested.**

## Publish on GitHub Pages

1. Create a **public** GitHub repository named `astromigo-images` (or choose another name).
2. Upload the **contents of this folder** to the repository root. Keep `images/M6.jpg` etc. as-is.
3. In repository **Settings → Pages**, select **Deploy from a branch**, branch `main`, folder `/ (root)` and save.
4. Wait for GitHub Pages to publish. Visit `https://YOUR_USERNAME.github.io/astromigo-images/images/M6.jpg` in a browser. You should see the Butterfly Cluster image.
5. In `AstroMigo_Stage12E_110_Messier_GitHub_Pages_main.cpp`, find `ASTROMIGO_IMAGE_BASE_URL = ""` and change it to `ASTROMIGO_IMAGE_BASE_URL = "https://YOUR_USERNAME.github.io/astromigo-images/images/";` with your real username/repo.
6. Before flashing, run `verify_hosted_images.py` from the firmware package to confirm all 35 URLs. Then copy the updated `main.cpp` into your PlatformIO project and build/upload.

**Do not flash before the image host is published and verified.**

## Important image licensing note

Read `ATTRIBUTION.md`. The original candidates were found through Wikipedia/Wikimedia thumbnails. Their individual licences have **not** been checked. For a publicly accessible repository, verify each image's licence and required attribution on its Wikimedia Commons file page before publishing. Replace images if redistribution is not permitted. The provided URLs are source leads, not licence grants.
