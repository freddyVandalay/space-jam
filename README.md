# SpaceJam - the Spotify playlist generator

[SpaceJam](https://open.spotify.com/playlist/5O5R4Tgb8Q92tlsZAKWuyG) - Open playlist in Spotify

This program creates a Spotify playlist called SpaceJam.
Tracks are added to the playlist based on the geolocation of the ISS (International Space Station).

The idea is to get the coordinates of the current ISS position
and use this to create a keyword to search for a track on Spotify.
The track is then added to the SpaceJam playlist.

The program creates the playlist if it doesn't already exists.

Note: ISS is mainly over water.

## How To Setup This Project

### Creating a virtual environment

```bash
python3 -m venv .venv
```

### Activating the newly created virtual environment

You always want your virtual environment to be active when working on this project.

```bash
source ./.venv/bin/activate
```

### Installing Python requirements

This will install some of the packages you might find useful:

```bash
pip3 install -r ./requirements.txt
```

### Configure API Credentials

1. Copy config.template.py
`cp sample.env .env`
2. and update with your credentials

### Configure Playlist and API details

1. Copy config.template.py and update variables with angled brackets
`cp sample.config.py config.py`
2. and add required credentials

## Resources

ISS API:
<http://open-notify.org/Open-Notify-API/ISS-Location-Now/>

Spotify API:
<https://developer.spotify.com/documentation/web-api/>

Google Geocoding API:
<https://developers.google.com/maps/documentation/geocoding/intro>

## Future Improvements

- Add lambda handler

- Current state doesn't consider if a track is already in the playlist.

- implement pydantic model

- refactor: use api client

- Add tests
