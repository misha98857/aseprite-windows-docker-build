# Aseprite :space_invader: Windows :computer: Docker :whale2: Build :gear:

This repository aims to make the complicated process of compiling [Aseprite](https://github.com/aseprite/aseprite) more simple.

Consider buying Aseprite to support the devs: https://www.aseprite.org/

## Usage

Download this repo and run `start.bat`.

Now you should see a folder called `bin/` and in it the Aseprite binaries!

### Prerequisites

- OS: Windows 10 (Version 2004 or newer)
- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
  - Use Windows containers: Right click on the tray icon -> Switch to Windows containers...

### Known issue

if you get error like this:

```
Dockerfile:3
--------------------
   1 |     # escape=`
   2 |
   3 | >>> FROM abrarov/msvc-2019
   4 |
   5 |     COPY build.bat C:\
--------------------
```

You should enable support for a windows containers:

1. Run this command in powershell with administrative rules:

`Enable-WindowsOptionalFeature -Online -FeatureName $("Microsoft-Hyper-V", "Containers") -All`

2. and if you still getting the error, run command:

`"C:\Program Files\Docker\Docker\DockerCli.exe" -SwitchWindowsEngine`