# Filament Take Picture Field v1

A custom Filament 4 form component to capture photos from your device camera.

## Features

- Take photos directly from the user's device camera
- Seamless integration with Filament 4 forms
- Configurable storage options (disk, directory, visibility)
- Camera selector for devices with multiple cameras
- Adjustable aspect ratio and image quality
- Modal support for better user experience

## Installation

```bash
composer require emmanpbarrameda/filament-take-picture-field
```

## Requirements

- PHP: 8.1^
- Filament: v3^ and v4^
- A device with camera access (desktop or mobile)

## Usage

Add the component to your Filament form:

```php
use emmanpbarrameda\FilamentTakePictureField\Forms\Components\TakePicture;

// ...

TakePicture::make('camera_test')
    ->label('Camera Test')
    ->disk('public')
    ->directory('uploads/services/payment_receipts_proof')
    ->visibility('public')
    ->useModal(true)
    ->showCameraSelector(true)
    ->aspect('16:9')
    ->imageQuality(80)
    ->shouldDeleteOnEdit(false)
```

## Configuration Options

| Method | Description |
|--------|-------------|
| `disk(string $disk)` | Set the storage disk for saving photos (default: 'public') |
| `directory(string $directory)` | Set the directory path within the disk where photos will be stored |
| `visibility(string $visibility)` | Set the file visibility (e.g., 'public', 'private') |
| `useModal(bool $useModal)` | Enable or disable modal view for the camera (default: 'true') |
| `showCameraSelector(bool $showSelector)` | Enable or disable camera selection option for devices with multiple cameras (default: 'true') |
| `aspect(string $aspect)` | Set the aspect ratio for the captured image (e.g., '16:9', '4:3', '1:1') |
| `imageQuality(int $quality)` | Set the JPEG quality of the captured image (0-100) |
| `shouldDeleteOnEdit(bool $shouldDelete)` | Whether to delete the previous file when editing (default: 'false') |

## ❗ IMPORTANT NOTICE: For Local development

The browser's Camera API only works on **secure origins** (HTTPS). Many browsers treat `https://localhost` as secure, but **plain** `http://` over an IP (e.g., `http://127.0.0.1:8000`) is considered insecure and the camera will be blocked. If it isn't working for you on `localhost`, switch to HTTPS or use the temporary Chrome test flags below.

### Recommended (safer) options

### Temporary Chrome workaround (for testing only)

If you must test over plain HTTP on a LAN IP, you can launch Chrome to *temporarily* treat that origin as secure. **Do not use this for normal browsing.** Use a separate profile and close all Chrome windows first.

Replace `http://127.0.0.1:8000` with your dev server's URL.

**Windows:**

```cmd
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:\chrome-dev-test" --unsafely-treat-insecure-origin-as-secure=http://127.0.0.1:8000 --disable-web-security
```

**macOS:**

```bash
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome \
  --user-data-dir="/tmp/chrome-dev-test" \
  --unsafely-treat-insecure-origin-as-secure=http://127.0.0.1:8000 \
  --disable-web-security
```

**Linux:**

```bash
google-chrome \
  --user-data-dir="/tmp/chrome-dev-test" \
  --unsafely-treat-insecure-origin-as-secure=http://127.0.0.1:8000 \
  --disable-web-security
```

### Security notes

* These flags **removes important browser protections**. Use them **only** for local testing of your app.
* Always use a **separate** `--user-data-dir` so your main Chrome profile stays safe.
* Close all Chrome windows before running the command, and avoid visiting untrusted sites in that session.

## Screenshots

![image](https://github.com/user-attachments/assets/12813349-b4f0-4ef2-91b7-430104b57742)
![image](https://github.com/user-attachments/assets/2643f1af-b8bb-4a1b-b745-337b4290d74b)
![image](https://github.com/user-attachments/assets/e7a9c5eb-e32c-418c-80b7-d3e425f0edae)

## Contributing

This is version 1.0 of the filament-take-picture-field component plugin. Contributions and pull requests for improvements are welcome!

## License
MIT

## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Glowing%20Star.png" alt="Glowing Star" width="40" height="40" /> Get in touch

<p align="center">
  <a href="https://emmanpbarrameda.github.io" target="_blank"><img src="https://img.shields.io/badge/My Portfolio-%20-blue?style=for-the-badge&logo=web"></a>
  &nbsp;&nbsp;
  <a href="mailto:emmanuelbarrameda1@gmail.com" target="_blank"><img src="https://img.shields.io/badge/Email-%20-red?style=for-the-badge&logo=gmail"></a>
  &nbsp;&nbsp;
  <a href="https://facebook.com/emmanpbarrameda/" target="_blank"><img src="https://img.shields.io/badge/Facebook-%20-blue?style=for-the-badge&logo=facebook"></a>
  &nbsp;&nbsp;
  <a href="https://t.me/emmanpbarrameda/" target="_blank"><img src="https://img.shields.io/badge/Telegram-%20-blue?style=for-the-badge&logo=telegram"></a>
  &nbsp;&nbsp;
  <a href="https://linkedin.com/in/emmanpbarrameda/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-%20-blue?style=for-the-badge&logo=linkedin"></a>
  &nbsp;&nbsp;
  <a href="https://github.com/emmanpbarrameda/" target="_blank"><img src="https://img.shields.io/badge/GitHub-%20-black?style=for-the-badge&logo=github"></a>
</p>
<br>

<p align="center">

  <!-- my name https://kapasia-dev-ed.my.site.com/Badges4Me/s/ -->
  <img alt='/e/' src='https://img.shields.io/badge/MADE_BY - EMMAN_P_BARRAMEDA-100000?style=for-the-badge&logo=/e/&logoColor=1877F2&labelColor=FFFFFF&color=1877F2'/>
  
  <!-- made with love -->
  <img alt='' src='https://img.shields.io/badge/MAKE_WITH_LOVE_FROM_PH-❤️-100000?style=for-the-badge&labelColor=EF4041&color=C1282D'/>
  
</p>
