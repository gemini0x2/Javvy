<h1 align="center">
  <br>
  <a href="http://www.amitmerchant.com/electron-markdownify"><img src="https://raw.githubusercontent.com/gemini0x2/Javvy/main/icon.png" alt="Markdownify" width="200"></a>
  <br>
  Javvy
  <br>
</h1>

<h4 align="center">A self-hosted movie organization web app designed for JAV enthusiasts</h4>
<h6 align="center">Note: This repository is only for Issue tracking, Instructions, and Releases</h6>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-install">How To install</a> •
  <a href="#download">Download</a> •
  <a href="#credits">Credits</a> •
  <a href="#support">Support</a> •
  <a href="#license">License</a>
</p>

![screenshot](https://raw.githubusercontent.com/gemini0x2/Javvy/main/screenshot.jpg)

## Key Features

* Filter movies by Year, Studio, Code, Actor
* Order by title, release date, import date, size, resolution, duration, bitrate
* In-app Media Player
* Custom number of columns
* Cross platform using Docker
  - Windows, macOS and Linux ready.

## How To install

Javvy can currently be installed as a Docker container. Docker, similar to a "virtual machine," enables users to install apps in containers managed by Docker, separate from their local machines. Containers can be easily removed and installed.

1. Download and Install [docker](https://www.docker.com/products/docker-desktop/) in your machine. [systems supported mac,win,linux](https://docs.docker.com/get-docker/#supported-platforms)
2. Download Javyy.zip
3. Unzip Javyy.zip and edit the compose.yaml file to set your configurations (instructions inside file)
4. Open terminal inside Javvy folder and run the folowing commands
```shell
docker load < javvyserver.tar && docker load < javvyapp.tar
```
```shell
docker compose up -d
```
5. Done! Open up your browser and enter [http://localhost:3000](http://localhost:3000)

## Download

You can [download](https://github.com/gemini0x2/Javvy/releases/tag/v0.1.0-alpha) the latest installable version of Javvy for Windows, macOS and Linux.

## Credits

The application leverages the following technologies:
- FFmpeg
- MongoDB
- Flask
- Next.js
- Docker

## Support

<a href="patreon.com/user?u=104827587">
	<img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>

## License

MIT

---

> GitHub [gemini0x2](https://github.com/gemini0x2) &nbsp;&middot;&nbsp;

