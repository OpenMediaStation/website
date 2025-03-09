+++
title = 'Getting started'
weight = 2
+++

> **WARNING:** The software is in a early stage of development. Please use it with care.

## Server installation

1. At first get the Docker image for the server.

```sh
docker pull ghcr.io/openmediastation/openmediaserver:latest
```

2. Use the following environment variables.

```env
DOMAIN=example.com
AUTH_CLIENTID=AAAAAAAAAAAAAAAAAA
AUTH_CONFIGURATION_URL=https://auth.example.com/application/o/open-media-station/.well-known/openid-configuration
TMDB_KEY=aaaaaaaaaaaaaaaaaaaaaaa
```

3. Map the port `8080` of the container to your https port.

4. Make sure to mount your media directory to `/media` and provide a empty directory for the server files at `/config`.

## Get the clients

### Movie & TV

You can obtain the client from the artifacts of the latest [release](https://github.com/OpenMediaStation/OpenMediaStation.FE.MovieTV/releases) or from one of the stores listed below.

- [Apple AppStore](https://testflight.apple.com/join/DmCy5QfP)
- [Amazon Tablet and Fire TV](https://www.amazon.com/Open-Media-Station-Shows-TV/dp/B0DY468FCZ)
- [Microsoft Store](https://apps.microsoft.com/detail/9nrfn2m3695g?hl=en-us&gl=US)
