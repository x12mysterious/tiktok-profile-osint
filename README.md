# TikTok Profile OSINT

TikTok Social Media Open Source Intelligence Tool — updated to work with TikTok's current page structure.

> Originally based on [TikTok-OSINT](https://github.com/Omicron166/TikTok-OSINT) by Omicron166 (MIT License)

## What's New
- Fixed broken scraper — TikTok replaced `SIGI_STATE` with `__UNIVERSAL_DATA_FOR_REHYDRATION__`
- Updated JSON extraction path from `props.pageProps.userInfo` to `__DEFAULT_SCOPE__.webapp.user-detail.userInfo`
- Remapped user and stats objects from `UserModule.users/stats` to `webapp.user-detail.userInfo.user/stats`
- Replaced hardcoded `[ ]` key access with `.get()` chains to prevent `KeyError` crashes
- Switched URL from `http://` to `https://`

## Requirements
- Python 3
- pip
- git (optional, just for git installation method)
- wget (optional, just for zip method)
- unzip (optional, just for zip method)

## Installation

### Git method
```bash
git clone https://github.com/x12mysterious/tiktok-profile-osint
cd tiktok-profile-osint
pip3 install -r requirements.txt
```

### Zip method
```bash
wget https://github.com/x12mysterious/tiktok-profile-osint/archive/refs/heads/main.zip
unzip main.zip
cd tiktok-profile-osint-main
pip3 install -r requirements.txt
```

## Usage
```bash
python3 tiktokOSINT.py --username USERNAMEHERE --downloadProfilePic
```
- Replace `USERNAMEHERE` with the username, the `@` is optional.
- `--downloadProfilePic` downloads the profile picture. This argument is optional.

## Data
TikTok Profile OSINT retrieves the following metadata about a user:

1. User ID
2. Username
3. Nickname
4. Bio
5. Profile Image
6. Following count
7. Followers count
8. Likes count
9. Video count
10. Verified status

## Disclaimer
This tool is for educational and research purposes only.
Only use it on public profiles. The author is not responsible for any misuse.

## License
MIT — see [LICENSE](LICENSE)
