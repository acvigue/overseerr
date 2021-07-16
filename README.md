<p align="center">
<img src="https://i.imgur.com/TMoEG7g.png" alt="Overseerr">
</p>
<p align="center">
<img src="https://github.com/sct/overseerr/workflows/Overseerr%20Release/badge.svg?branch=master" alt="Overseerr Release" />
<img src="https://github.com/sct/overseerr/workflows/Overseerr%20CI/badge.svg" alt="Overseerr CI">
</p>
<p align="center">
<a href="https://discord.gg/PkCWJSeCk7"><img src="https://img.shields.io/discord/783137440809746482" alt="Discord"></a>
<a href="https://hub.docker.com/r/sctx/overseerr"><img src="https://img.shields.io/docker/pulls/sctx/overseerr" alt="Docker pulls"></a>
<a href="https://hosted.weblate.org/engage/overseerr/"><img src="https://hosted.weblate.org/widgets/overseerr/-/overseerr-frontend/svg-badge.svg" alt="Translation status" /></a>
<a href="https://lgtm.com/projects/g/sct/overseerr/context:javascript"><img alt="Language grade: JavaScript" src="https://img.shields.io/lgtm/grade/javascript/g/sct/overseerr.svg?logo=lgtm&logoWidth=18"/></a>
<a href="https://github.com/sct/overseerr/blob/develop/LICENSE"><img alt="GitHub" src="https://img.shields.io/github/license/sct/overseerr"></a>
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
<a href="#contributors-"><img alt="All Contributors" src="https://img.shields.io/badge/all_contributors-33-orange.svg"/></a>
<!-- ALL-CONTRIBUTORS-BADGE:END -->
</p>

**Overseerr** is a free and open source software application for managing requests for your media library. It integrates with your existing services, such as **[Sonarr](https://sonarr.tv/)**, **[Radarr](https://radarr.video/)**, and **[Jellyfin](https://www.jellyfin.org/)**, **[Plex](https://www.plex.tv/)**! 

## Current Features

- Full Plex integration. Authenticate and manage user access with Plex!
- Full Jellyfin integration. Authenticate and manage user access with Jellyfin!
- Easy integration with your existing services. Currently, Overseerr supports Sonarr and Radarr. More to come!
- Jellyfin library sync, to keep track of the titles which are already available.
- Customizable request system, which allows users to request individual seasons or movies in a friendly, easy-to-use interface.
- Incredibly simple request management UI. Don't dig through the app to simply approve recent requests!
- Granular permission system.
- Support for various notification agents.
- Mobile-friendly design, for when you need to approve requests on the go!

## Planned Features

- Additional notification types.
- Issues system. This will allow users to report issues with content on your media server.
- And a ton more! Check out our [issue tracker](https://github.com/sct/overseerr/issues) to see the features which have already been requested.

## Getting Started

## Requirments
1. Git Bash **[Git Direct Downoad](https://git-scm.com/download/win)**
2. NodeJs [NodeJS Direct x64 Download](https://nodejs.org/dist/v14.17.3/node-v14.17.3-x64.msi)** **[NodeJS Direct x86 Download](https://nodejs.org/dist/v14.17.3/node-v14.17.3-x86.msi)**

**NOTE IMPORTANT**
MAKE SURE YOU HAVE ALL WINDWOS UPDATE PENDED AND AFTER INSTALLING THE PROGRAMS ABOVE RESTART THE OS BEFORE CONTINUE FOR GOOD MEASURES.

## Running on Windows

1. Open Powershell with administrative rights.
2. Get yarn by typing in powershell `npm install --global yarn`
3. Now run in powershell `npm install -g win-node-env` so it can correctly build for windows.
4. Once yarn is installed close powershell and open a new powershell with adminstrative privelages.
5. Go to a directory where you want your app to run. I normally run all binaries in `C:\Tools\(appname)` so mine is C:\Tools
6. Then run `git clone https://github.com/sct/overseerr.git`
7. Then once cloned youll see it ripped a new folder in `C:\Tools` its a folder called `overseerr`
8. Now open the folder overseerr directory in powershell by running `cd C:\Tools\overseerr`
9. once in the directory `C:\Tools\overseerr` run `yarn`
10. Then once finished (it will take a bit of a long time) run `yarn build`
11. If it built with no errors then run `yarn start` which will run the overseerr and load up localhost:5055 on your browser.
12. Watch the powershell and just wait for the webpage on your browser to run oveseerr you should see the homepage once it is loaded in powershell.

## Auto-Start at Windows Startup
 ### Requirmenets
 Install NSSM [NSSM Direct Download](https://nssm.cc/release/nssm-2.24.zip)

## Setup NSSM with Overserr
1. type in an administrative Powershell `nssm install Overseerr`
2. Then it should pull up with a UI. On the first page for the Path we want to put powershell `C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe`
3. For the Startup Directory if you have followed this tut word for word you need to put this as the startup path `C:\Tools\overseerr` if you havent it would be `C:\(Directory where you git cloned the repo)\overseerr`
4. Now put for the  Arguments `yarn start`
It should look like below


![Overseerr NSSM Demo](https://i.imgur.com/saK6nqc.png)


6. Click Install Service
7. Open up a powershell as administrator and run nssm start Overseerr or go to services.msc and find overseerr task and right click and select start

## Running Overseerr

Currently, Overseerr is primarily distributed as Docker images. If you have Docker installed, you can simply run Overseerr with:

```
docker run -d \
  -e LOG_LEVEL=info \
  -e TZ=Asia/Tokyo \
  -p 5055:5055 \
  -v /path/to/appdata/config:/app/config \
  --restart unless-stopped \
  sctx/overseerr
```

After running Overseerr for the first time, configure it by visiting the web UI at http://[address]:5055 and completing the setup steps

For more information or alternative installation methods, please see the [Overseerr documentation](https://docs.overseerr.dev/getting-started/installation).

⚠️ Overseerr is currently under very heavy, rapid development and things are likely to break often. We need all the help we can get to find bugs and get them fixed to hit a more stable release. If you would like to help test the bleeding edge, please use the `sctx/overseerr:develop` image instead! ⚠️

## Preview

<img src="./public/preview.jpg">

## Support

- Check out the [Overseerr Documentation](https://docs.overseerr.dev/) before asking for help. Your question might already be in the [FAQ](https://docs.overseerr.dev/support/faq).
- You can get support on [Discord](https://discord.gg/PkCWJSeCk7).
- You can ask questions in the Help category of our [GitHub Discussions](https://github.com/sct/overseerr/discussions).
- Bug reports and feature requests can be submitted via [GitHub Issues](https://github.com/sct/overseerr/issues).

## API Documentation

Our documentation is built on every commit and hosted at https://api-docs.overseerr.dev

You can also access the API documentation from your local Overseerr install at http://localhost:5055/api-docs

## Community

You can ask questions, share ideas, and more in [GitHub Discussions](https://github.com/sct/overseerr/discussions).

If you would like to chat with other members of our growing community, [join the Overseerr Discord server](https://discord.gg/PkCWJSeCk7)!

Our [Code of Conduct](https://github.com/sct/overseerr/blob/develop/CODE_OF_CONDUCT.md) applies to all Overseerr community channels.

## Contributing

You can help improve Overseerr too! Check out our [Contribution Guide](https://github.com/sct/overseerr/blob/develop/CONTRIBUTING.md) to get started.

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://sct.dev"><img src="https://avatars1.githubusercontent.com/u/234213?v=4?s=100" width="100px;" alt=""/><br /><sub><b>sct</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=sct" title="Code">💻</a> <a href="#design-sct" title="Design">🎨</a> <a href="#ideas-sct" title="Ideas, Planning, & Feedback">🤔</a></td>
    <td align="center"><a href="https://github.com/azoitos"><img src="https://avatars2.githubusercontent.com/u/26529049?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Alex Zoitos</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=azoitos" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/OwsleyJr"><img src="https://avatars3.githubusercontent.com/u/8635678?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Brandon Cohen</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=OwsleyJr" title="Code">💻</a> <a href="https://github.com/sct/overseerr/commits?author=OwsleyJr" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/Ahreluth"><img src="https://avatars2.githubusercontent.com/u/75682440?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Ahreluth</b></sub></a><br /><a href="#translation-Ahreluth" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/KovalevArtem"><img src="https://avatars0.githubusercontent.com/u/36500228?v=4?s=100" width="100px;" alt=""/><br /><sub><b>KovalevArtem</b></sub></a><br /><a href="#translation-KovalevArtem" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/GiyomuWeb"><img src="https://avatars0.githubusercontent.com/u/62489209?v=4?s=100" width="100px;" alt=""/><br /><sub><b>GiyomuWeb</b></sub></a><br /><a href="#translation-GiyomuWeb" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/angrycuban13"><img src="https://avatars3.githubusercontent.com/u/39564898?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Angry Cuban</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=angrycuban13" title="Documentation">📖</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/jvennik"><img src="https://avatars3.githubusercontent.com/u/6672637?v=4?s=100" width="100px;" alt=""/><br /><sub><b>jvennik</b></sub></a><br /><a href="#translation-jvennik" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/darknessgp"><img src="https://avatars0.githubusercontent.com/u/1521243?v=4?s=100" width="100px;" alt=""/><br /><sub><b>darknessgp</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=darknessgp" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/saltydk"><img src="https://avatars1.githubusercontent.com/u/6587950?v=4?s=100" width="100px;" alt=""/><br /><sub><b>salty</b></sub></a><br /><a href="#infra-saltydk" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
    <td align="center"><a href="https://github.com/Shutruk"><img src="https://avatars2.githubusercontent.com/u/9198633?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Shutruk</b></sub></a><br /><a href="#translation-Shutruk" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/krystiancharubin"><img src="https://avatars2.githubusercontent.com/u/17775600?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Krystian Charubin</b></sub></a><br /><a href="#design-krystiancharubin" title="Design">🎨</a></td>
    <td align="center"><a href="https://github.com/kieron"><img src="https://avatars2.githubusercontent.com/u/8655212?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Kieron Boswell</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=kieron" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/samwiseg0"><img src="https://avatars1.githubusercontent.com/u/2241731?v=4?s=100" width="100px;" alt=""/><br /><sub><b>samwiseg0</b></sub></a><br /><a href="#question-samwiseg0" title="Answering Questions">💬</a> <a href="#infra-samwiseg0" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/ecelebi29"><img src="https://avatars2.githubusercontent.com/u/8337120?v=4?s=100" width="100px;" alt=""/><br /><sub><b>ecelebi29</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=ecelebi29" title="Code">💻</a> <a href="https://github.com/sct/overseerr/commits?author=ecelebi29" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/mmozeiko"><img src="https://avatars3.githubusercontent.com/u/1665010?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Mārtiņš Možeiko</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=mmozeiko" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/mazzetta86"><img src="https://avatars2.githubusercontent.com/u/45591560?v=4?s=100" width="100px;" alt=""/><br /><sub><b>mazzetta86</b></sub></a><br /><a href="#translation-mazzetta86" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/Panzer1119"><img src="https://avatars1.githubusercontent.com/u/23016343?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Paul Hagedorn</b></sub></a><br /><a href="#translation-Panzer1119" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/Shagon94"><img src="https://avatars3.githubusercontent.com/u/9140783?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Shagon94</b></sub></a><br /><a href="#translation-Shagon94" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/sebstrgg"><img src="https://avatars3.githubusercontent.com/u/27026694?v=4?s=100" width="100px;" alt=""/><br /><sub><b>sebstrgg</b></sub></a><br /><a href="#translation-sebstrgg" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/danshilm"><img src="https://avatars2.githubusercontent.com/u/20923978?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Danshil Mungur</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=danshilm" title="Code">💻</a> <a href="https://github.com/sct/overseerr/commits?author=danshilm" title="Documentation">📖</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/doob187"><img src="https://avatars1.githubusercontent.com/u/60312740?v=4?s=100" width="100px;" alt=""/><br /><sub><b>doob187</b></sub></a><br /><a href="#infra-doob187" title="Infrastructure (Hosting, Build-Tools, etc)">🚇</a></td>
    <td align="center"><a href="https://github.com/johnpyp"><img src="https://avatars2.githubusercontent.com/u/20625636?v=4?s=100" width="100px;" alt=""/><br /><sub><b>johnpyp</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=johnpyp" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/ankarhem"><img src="https://avatars1.githubusercontent.com/u/14110063?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jakob Ankarhem</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=ankarhem" title="Documentation">📖</a> <a href="https://github.com/sct/overseerr/commits?author=ankarhem" title="Code">💻</a> <a href="#translation-ankarhem" title="Translation">🌍</a></td>
    <td align="center"><a href="https://github.com/jayesh100"><img src="https://avatars1.githubusercontent.com/u/8022175?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Jayesh</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=jayesh100" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/flying-sausages"><img src="https://avatars1.githubusercontent.com/u/23618693?v=4?s=100" width="100px;" alt=""/><br /><sub><b>flying-sausages</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=flying-sausages" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/hirenshah"><img src="https://avatars2.githubusercontent.com/u/418112?v=4?s=100" width="100px;" alt=""/><br /><sub><b>hirenshah</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=hirenshah" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/TheCatLady"><img src="https://avatars0.githubusercontent.com/u/52870424?v=4?s=100" width="100px;" alt=""/><br /><sub><b>TheCatLady</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=TheCatLady" title="Code">💻</a> <a href="#translation-TheCatLady" title="Translation">🌍</a> <a href="https://github.com/sct/overseerr/commits?author=TheCatLady" title="Documentation">📖</a></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/chriscpritchard"><img src="https://avatars1.githubusercontent.com/u/1839074?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Chris Pritchard</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=chriscpritchard" title="Code">💻</a> <a href="https://github.com/sct/overseerr/commits?author=chriscpritchard" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/Tamberlox"><img src="https://avatars3.githubusercontent.com/u/56069014?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Tamberlox</b></sub></a><br /><a href="#translation-Tamberlox" title="Translation">🌍</a></td>
    <td align="center"><a href="https://hmnd.io"><img src="https://avatars.githubusercontent.com/u/12853597?v=4?s=100" width="100px;" alt=""/><br /><sub><b>David</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=hmnd" title="Code">💻</a></td>
    <td align="center"><a href="https://www.douglas-parker.com"><img src="https://avatars.githubusercontent.com/u/18235822?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Douglas Parker</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=douglasparker" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/dancarter"><img src="https://avatars.githubusercontent.com/u/4387516?v=4?s=100" width="100px;" alt=""/><br /><sub><b>Daniel Carter</b></sub></a><br /><a href="https://github.com/sct/overseerr/commits?author=dancarter" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->
