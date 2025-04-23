# telegram-tools

A collection of Python utilities using the Telegram API to export group messages, download images, and download files from Telegram groups.
---

## Features

- **Message Exporter**  
  Export all messages from a Telegram group or channel into a structured CSV file.

- **Media Downloader**  
  Download all photos and videos from a group or channel to your local machine.

- **File Downloader**  
  Download all shared documents (e.g., PDFs, ZIPs) from a group or channel.

- **Modular Design**  
  Shared login system using Telethon across all tools.

---

## Table of Contents

- [Features](#-features)
- [Installation](#-installation)
- [Configuration](#-configuration)
- [Usage](#-usage)
- [Folder Structure](#-folder-structure)
- [Dependencies](#-dependencies)
- [License](#-license)

---

## Installation

1. **Clone the repository**:

```bash
git clone https://github.com/yourusername/telegram-tools.git
cd telegram-tools
```

2. **Install dependencies**:

```bash
pip install -r requirements.txt
```

---

## Configuration

Before running any tool:

1. Get your Telegram API credentials:
   - Go to [Telegram API](https://my.telegram.org)
   - Create a new application.
   - Save your `api_id` and `api_hash`.

2. Open the file:

```
utils/telegram_client.py
```

And update these lines with your real credentials:

```python
api_id = YOUR_API_ID
api_hash = 'YOUR_API_HASH'
```

You only need to set this up once.

---

## Usage

Each tool has its own directory and script.

### 1. Export Group Messages

```bash
cd message_exporter
python3 export_messages.py
```
Exports all group messages to `group_messages.csv`.

---

### 2. Download Media (Photos/Videos)

```bash
cd media_downloader
python3 download_media.py
```
Downloads all media into a `downloads/` folder.

---

### 3. Download Files/Documents

```bash
cd file_downloader
python3 download_files.py
```
Downloads all files shared in the group.

---

## 📁 Folder Structure

```plaintext
telegram-tools/
├── README.md
├── requirements.txt
├── .gitignore
├── message_exporter/
│   ├── export_messages.py
│   └── README.md
├── media_downloader/
│   ├── download_media.py
│   └── README.md
├── file_downloader/
│   ├── download_files.py
│   └── README.md
└── utils/
    ├── telegram_client.py
```

---

## Dependencies

- [Telethon](https://github.com/LonamiWebs/Telethon) — Python Telegram client library.

Install dependencies with:

```bash
pip install -r requirements.txt
```

---

## License

This project is licensed under the [MIT License](LICENSE).

---
