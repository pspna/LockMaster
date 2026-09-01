# LockMaster

LockMaster is a Windows desktop application that allows you to lock, unlock, encrypt, and decrypt files or folders. It features a matrix rain background and supports both permission-based locking and strong encryption.

## Features

- **Lock / Unlock:** Basic locking mechanism using Windows ACL permissions.
- **Encrypt / Decrypt:** Secure files with AES encryption via Fernet.
- **Progress Bar:** Visual indicator for encryption and decryption progress.
- **Matrix Rain Effect:** A hacker-style animated background.
- **Windows Executable:** Ready-to-run `LockMaster.exe` included in `dist/`.

## Requirements

- Windows 10 / 11
- Python 3.8+ (for running from source)

## Installation

### Option 1: Run the EXE

1. Go to the `dist` folder.
2. Double-click `LockMaster.exe`.

### Option 2: Run from Source

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the app:
   ```bash
   python LockMaster.py
   ```

## Build EXE

To rebuild the executable yourself:

```bash
pyinstaller --onefile --noconsole --icon=icon.ico LockMaster.py
```

The output will be in the `dist` folder.

## Usage

1. Click **Browse** to select a file or folder.
2. Use **Lock / Unlock** to change Windows permissions.
3. Use **Encrypt / Decrypt** to secure content with encryption.

## Notes

- Lock/Unlock uses Windows `icacls` under the hood.
- Encryption uses a local `secret.key` file. Keep it safe to decrypt later.
- The app is Windows-only because it relies on Windows permission tools and `winsound`.

## License

Open source for personal and educational use.
