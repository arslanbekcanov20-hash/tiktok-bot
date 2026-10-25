# TikTok & YouTube Shorts Video Automation Bot

An advanced, production-ready Python automation script that handles the entire pipeline of short-form video creation and publishing. This tool monitors real-time trending content via the YouTube Data API, uses generative AI models (Gemini & Pollinations) to write and style original narrative scripts, renders customized MP4 video files locally, and programmatically uploads them using the official platform APIs.

## 🚀 Key Features

* **Trend Tracking:** Automatically fetches and ranks top trending regional content via YouTube Data API.
* **AI Content Generation:** Leverages Google Gemini for scripting story arcs across multi-part series, optimal scene blocking, and directing asset generation.
* **Dynamic Audio & Visual Processing:** Implements robust local video assembly using OpenCV (numpy) and FFmpeg, featuring automated voiceover generation (Gemini TTS), subtitle alignment via Whisper ASR, camera motion (pans/zooms), dynamic filters, and synchronized sound effects/music.
* **Fault-Tolerant Direct Publishing:** Utilizes custom-built chunk-based multi-part upload protocols to securely publish finished videos to TikTok (Content Posting API via `video.upload` and `video.publish` scopes) and YouTube Shorts.
* **Resilient Infrastructure Guard:** Monitors connection status and manages network switches via ADB controls for tethered configurations, paired with fully automated job recovery states.

## 🛠️ Technology Stack

* **Core Engine:** Python 3.11+, Asyncio, Threading
* **AI & Machine Learning:** Google GenAI (Gemini 2.5/3.5/3.8), Pollinations.ai API, WinOCR, Whisper
* **Media & Processing:** FFmpeg, OpenCV (cv2), Pillow (PIL), NumPy, Rich (terminal UI)
* **Networking & Deployment:** HTTPX, Google API Client, OAuthlib, ADB (Android Debug Bridge)

## 📋 Platform Review Verification

This repository functions as the official central codebase and technical configuration anchor for our registered TikTok Developer Application. All API connections strictly target authorized endpoints (`/post/publish/video/init/`, `/post/publish/creator_info/query/`) under explicit direct-consent authorization flows to programmatically push user-approved vertical content with valid `is_aigc: true` transparency declarations.
