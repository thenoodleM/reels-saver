# Reel Saver

**Save media from supported links, directly from Android's share sheet.**

Reel Saver is a native Android application designed to make saving media straightforward. Share a supported link to the app, and it handles the download in the background while keeping the original app accessible.

The project focuses on a streamlined user experience backed by a download pipeline designed to handle media extraction, background processing, and file management.

## Showcase


https://github.com/user-attachments/assets/8ae90d0e-64ba-41fe-ab93-fb49fc425c15



## Features

- **Share-Sheet Integration:** Send supported links directly to Reel Saver from other applications.
- **Background Downloads:** A foreground service manages downloads while the app is not in the foreground.
- **Download Queue:** Queue multiple shared links for processing.
- **Progress Tracking:** Display download progress and transfer speed.
- **Chunked Downloads:** Custom download handling with parallel requests, retries, and resumable transfers where supported.
- **YouTube Quality Selection:** Choose from available media quality options.
- **Optional Instagram Login:** Sign in through Instagram's website to access content available to your account.
- **Floating Progress Interface:** Optionally display download progress over the source application.
- **Gallery Integration:** Save downloaded media to appropriate device storage locations.
- **Notifications:** Receive download status notifications.
- **Downloader Updates:** Check for downloader updates to help address changes in supported services.

## Tech Stack

- **Language:** Kotlin
- **UI:** Jetpack Compose
- **Networking:** OkHttp
- **Asynchronous Processing:** Kotlin Coroutines
- **Media Extraction:** yt-dlp
- **Media Processing:** FFmpeg
- **Android Components:** Foreground services, share-sheet integration, notifications, and overlay windows
- **Platform:** Android

## Technical Highlights

### Background Download Pipeline

Reel Saver uses an Android foreground service to manage downloads beyond the lifetime of the visible screen. This allows users to share a link and continue using other applications while processing continues.

### Custom Download Handling

The project includes a chunked downloader with parallel requests, retries, and resumable transfers where the source supports them. Transfer progress and speed are surfaced to the application interface.

### Share-Sheet Workflow

The share receiver accepts shared text links, allowing users to initiate downloads without manually switching to Reel Saver and pasting each link.

### Media Processing

The application integrates yt-dlp and FFmpeg for media extraction and processing, including quality selection for supported YouTube downloads.

### Optional Account Integration

Instagram authentication is handled through the Instagram website. The app stores session cookies locally for authenticated access rather than asking users to enter their password directly into a custom login form.

## Requirements

- Android 10 or newer
- ARM64 Android device
- Internet connection
- Additional Android permissions may be required for overlay progress indicators and notifications

Some functionality depends on the source platform, account access, and changes to its services.

## Project Status

Reel Saver is a completed application project. Its compatibility with third-party services may change as those services update their systems.

## Important Notes

- Download availability depends on the source platform and the content accessible to the user.
- Respect copyright, content ownership, and the terms applicable to each platform. Only download content you are authorized to save.
- Authentication cookies and other sensitive information should be kept private.
- This project is intended to demonstrate Android application development, media processing, networking, and background task management.

