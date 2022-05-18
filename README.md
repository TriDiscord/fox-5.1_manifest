<p align="center">
    <img width="300" src="https://user-images.githubusercontent.com/67373913/169030969-f106bbbc-03e3-4a49-9276-a4adc44bf700.png">
</p>

<h1 align="center">OrangeFox Recovery Manifest for Android 5.1</h1>

## Downloading Source

```bash
cd ~/orangefox
repo init --depth=1 -u https://github.com/TriDiscord/fox-5.1_manifest.git -b fox-5.1 # Initialize OrangeFox source code
# Clone whatever local manifest you have here
repo sync -c --force-sync --optimized-fetch -j$(nproc --all) # Start syncing
```

## Building

```bash
source build/envsetup.sh
export ALLOW_MISSING_DEPENDENCIES=true
export FOX_USE_TWRP_RECOVERY_IMAGE_BUILDER=1
export LC_ALL=C
export OF_LEGACY_SHAR512=1
# Run lunch for your device here, use eng
mka recoveryimage
```

## Credits

- **TeamWin Recovery Project:** Build and manifest is based on their repositories
- **OrangeFox Recovery Project:** The recovery itself
- [**@Sushrut1101:**]((https://gitlab.com/Sushrut1101) This entire 5.1 manifest is based on their works
