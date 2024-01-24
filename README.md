<h1 align="center">
  <br>
  <a href=""><img src="https://raw.githubusercontent.com/gemini0x2/Javvy/main/icon.png" alt="Markdownify" width="200"></a>
  <br>
  Javvy
  <br>
</h1>

<h4 align="center">A self-hosted movie organization web app designed for JAV enthusiasts</h4>
<h6 align="center">Note: This repository is only for Issue tracking, Instructions, and Releases</h6>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-install">How To Install</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#support">Support</a> •
  <a href="#license">License</a>
</p>

![screenshot](https://raw.githubusercontent.com/gemini0x2/Javvy/main/screenshot.jpg)

## Key Features
* Clean simple gallery design
* Filter movies by Year, Studio, Code, Actor
* Order by title, release date, import date, size, resolution, duration, bitrate
* In-app Media Player
* Custom number of columns
* Cross platform using Docker
  - Windows, macOS and Linux ready.
* Reads nfo files, and poster images.
* Does not modify any of your files!

## How To Install

Javvy can currently be installed as a Docker container. Docker, similar to a "virtual machine," enables users to install apps in containers managed by Docker, separate from their local machines. Containers can be easily removed and installed.

1. Download and Install [docker](https://www.docker.com/products/docker-desktop/) in your machine. [systems supported mac,win,linux](https://docs.docker.com/get-docker/#supported-platforms)
2. Download [Javyy.zip](https://github.com/gemini0x2/Javvy/releases/tag/v0.1.0-alpha)
3. Unzip Javyy.zip and edit the `compose.yaml` file to set your configurations (instructions inside file)
4. Open terminal inside Javvy folder and run the folowing commands

**Mac, Linux, or Windown Git bash console:**
```shell
docker load < javvyserver.tar && docker load < javvyapp.tar
```
```shell
docker compose up -d
```
**Windows cmd:**
```
docker load -i javvyserver.tar && docker load -i javvyapp.tar
```
```cmd
docker-compose up -d
```
5. Done! Open up your browser and enter [http://localhost:3000](http://localhost:3000)

## Download

You can [download](https://github.com/gemini0x2/Javvy/releases/tag/v0.1.0-alpha) the latest installable version of Javvy for Windows, macOS and Linux.

## How To Use

### Naming and organizing your Movie files for Javvy.
Movies in Their Own Folders: Javvy will **only** read your movies if they are organized in their own folders with their corresponding nfo and poster files. If any of the files are missing the movie will be skipped. To correctly display your movies they must be named based on their Jav Codes. 

- Name the folder the same as the movie file (Note: The movie filename should be it's corresponding Jav Code)
- Name the poster image file the same as the movies file, but you **MUST** add the "-poster" suffix (only .jpg type supported for now)
- Name the nfo file the same as the movie file

```bash
IPX-623/
├── IPX-623-poster.jpg
├── IPX-623.mp4
└── IPX-623.nfo
```
As long as each movie file is in it's corresponding folder with a poster file and nfo file, you can organize the movie folders however you want.
```bash
JAV_collection/
├── IPX/
│   ├── IPX-623
│   ├── IPX-580
│   └── ..
├── STARS/
│   ├── STARS-361
│   ├── STARS-386
│   └── ...
├── SSIS/
│   ├── SSIS-179
│   ├── SSIS-211
│   └── ..
└── Favorites/
    ├── Top/
    │   ├── DASD-785
    │   ├── JUL-779
    │   └── MDON-016/
    │       └── New/
    │           └── MIDE-925
    └── Old/
        ├── MIDE-975
        └── MIDE-976
```
In the above example if you pass `JAV_collection` as the path to your media Javvy will scan the complete folder and import all your movies.

### Format of nfo files
Javvy reads the nfo file of each movie to extract information about the movie.
The tags that Javvy currently extract are the following
- `<originaltitle>` for movie Jav title
- `<num>` for movie Jav Code
- `<studio>` for movie Studio
- `<actor>` for movie actors (can be more than one)
- `<genre>` for movie genres (can be more than one)
- `<premiered>` for movie release date

Basic nfo file example:
```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<movie>
<premiered>2021-03-13</premiered>
<num>IPX-623</num>
<originaltitle>IPX-623 Teacher Who Sucks D*ck with A Smile (Blu-ray Disc)</originaltitle>
<actor>
  <name>Hikaru Gatsu Mina</name>
  <type>actors</type>
</actor>
<actor>
  <name>Kana Minami Ryou</name>
  <type>actors</type>
</actor>
<studio>IDEA POCKET</studio>
<genre>sister</genre>
<genre>tutor</genre>
<genre>4K</genre>
</movie>
```
Notes
- your nfo files may have additional tags, the above example only contains the tags that Javvy extracts for now. <br/>
- if the nfo file is corrupted or contains unsupported characters, such as ampersand (&), the movie file will be skipped!
- if `<num>` is missing, then the code will be extracted from the movie filename, hence the importance of naming your movies by their respective Jav Codes.
- if `<originaltitle>` is missing from nfo, `<num>` will be used instead.
- if `<premiered>` is missing `<releasedate>` will be used instead, but if `<releasedate>` is missing too then `<release>` will be used.


## Credits

The application leverages the following technologies:
- FFmpeg
- MongoDB
- Flask
- Next.js
- Docker

## Support

<a href="https://patreon.com/user?u=104827587">
	<img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## License

MIT

---

> GitHub [gemini0x2](https://github.com/gemini0x2) &nbsp;&middot;&nbsp;
> Discord [Javvy](https://discord.gg/RKpBguas) &nbsp;&middot;&nbsp;
> Email gemini0x2@gmail.com

