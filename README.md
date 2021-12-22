# ScoreSaber replays

[![Netlify Status](https://api.netlify.com/api/v1/badges/08ead0d0-ade4-4f38-8af4-9b6c3c679234/deploy-status)](https://app.netlify.com/sites/musing-aryabhata-6ae6ea/deploys)

[A-Frame]: https://aframe.io
[visit]: https://replay.beatleader.xyz/

Web-based viewer for ScoreSaber replays, built with [A-Frame] and JavaScript.

**[CLICK TO VIEW][visit]**

![https://replay.beatleader.xyz/](https://raw.githubusercontent.com/supermedium/beatsaver-viewer/master/assets/img/sshot.jpg)

## Usage

Go to the ![BeatLeader](https://beatleader.xyz) and click on any ranked play higher than top 500 on leaderboard.

Or if you have a site, you can I-Frame the viewer and pass a query parameter
containing the song ID, difficulty and playerID:

`https://www.replay.beatleader.xyz/?id=c32d&difficulty=ExpertPlus&playerID=76561198333869741`

id - BeatSaver song ID. ("Ov Sacrament" in this case)
difficulty - Easy, Normal, Hard, Expert, ExpertPlus
playerID - player's Steam or Oculus ID (cerret in this case)

To directly link to a seeked time, use the `?time` parameter in the URL (milliseconds):

`https://www.replay.beatleader.xyz/?id=c32d&difficulty=ExpertPlus&playerID=76561198333869741&time=15000` - 15 sec

To specify replay speed use the `?speed` paramater in the URL (thousands of percent):

`https://www.replay.beatleader.xyz/?id=c32d&difficulty=ExpertPlus&playerID=76561198333869741&speed=50000` - 50% speed

## Roadmap

- Safari support (BeatSaver currently serves OGGs which are not supported)
- Custom saber viewer

## Community

*The ScoreSaber replays is an unofficial community project and not officially
affiliated with Beat Saber.*

- [BeatLeader Discord](https://discord.gg/RpXagakZ)

## Development

Built with [A-Frame](https://aframe.io), a web framework that we created for
building VR experiences. And JavaScript.

```
npm install
```

### Configure Netlify account 

Create a new Netlify project and link it to the forked repo. 

#### Install netlify dev CLI

```bash
npm install netlify-cli -g
```

Then start Netlify dev environment

```bash
netlify dev
```

Navigate to [localhost:8888](http://localhost:9999). You should see app running.

### Building and running in production mode

By default, Netlify builds the app after every change to this branch in the repository, so all you need is push to git.