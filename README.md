# NARROWVINE  
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/) [![Github All Releases](https://img.shields.io/github/downloads/WHTJEON/narrowvine/total.svg)]() [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## (2021.8.26) New Version Released: https://github.com/WHTJEON/narrowvine-reborn
## (2021.6.1) Widevine revoked every exploit used in this script. It's dead.<br>It is reported to still work in some sites, but most of them are revoked.

The Ultimate Widevine Content Ripper (KEY Extract + Download + Decrypt)<br>
**Extracting decryption keys only supports Windows.** 
- If you are using a different platform, you would need to extract decryption keys using Widevine L3 decryptor from a Windows Machine first and paste them into the script. 
- This is a combination of widevine-dl and widevineclient3 in my repo. 
- This exploit will be patched by Widevine in May 31st, 2021.

## Requirements
- ffmpeg, yt-dlp, aria2 (These must be in PATH. If you want to skip this procedure, download from [Releases](https://github.com/WHTJEON/narrowvine/releases))
- pycryptodome

```
$ pip install ffmpeg yt-dlp aria2p pycryptodome
```
or just simply
```
$ pip install -r requirements.txt
```
## Instructions For Windows
1. Clone or Download the Repo (It is more recommended to download a compiled version from [Releases](https://github.com/WHTJEON/narrowvine/releases))
2. Run narrowvine.py
  ```
  $ python3 narrowvine.py
  ```
3. Enter `MPD_URL` and `LICENSE_URL` of Widevine Content 
4. Enter `VIDEO_ID` and `AUDIO_ID` to download encrypted content. 
5. Once you are done downloading, the script will extract the keys and decrypt the contents.<br> 

  ![2](https://user-images.githubusercontent.com/57805304/117309054-0c19c700-aebd-11eb-93b4-230af77e83a1.PNG)

6. Enter `FILENAME` with extension! (ex. `final.mp4`)
7. Your decrypted contents will be merged and saved to /output directory. 

## Inputs
- `MPD_URL` - MPD URL of Widevine Content
- `LICENSE_URL` - LICENSE URL of Widevine Content
- `VIDEO_ID` - Video Track ID Shown in Stream Info *(Leave blank for best)*
- `AUDIO_ID` - Audio Track ID Shown in Stream Info *(Leave blank for best)*
- `FILENAME` - Desired File Name of Final Decrypted File *(with extension!)*

## Arguments
- You can also run the python script in a single line command
```
$ python3 narrowvine.py -mpd "https://bitmovin-a.akamaihd.net/content/art-of-motion_drm/mpds/11331.mpd" -license "https://widevine-proxy.appspot.com/proxy"
```
## DLL Dependencies
If you get `ucrtbased.dll` and `vcruntime140d.dll` missing error when running `license_proxy.exe`, download and unzip [32bit.zip](https://github.com/WHTJEON/narrowvine/files/6438020/32bit.zip) to `..\Windows\System32` and download and unzip [64bit.zip](https://github.com/WHTJEON/narrowvine/files/6438018/64bit.zip) to `..\Windows\SysWOW64`.

## Legal Notice
Educational purposes only. Downloading DRM'ed materials may violate their Terms of Service. DO NOT USE THIS FOR PIRACY.

## HEROKU DEPLOY 
[![Deploy To Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/Sawai12/narrowvinedrm)


If you enjoyed using the script, a star or a follow will be highly appreciated! 😎
