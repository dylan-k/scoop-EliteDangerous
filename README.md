# Elite Dangerous scoop bucket

This [Scoop](https://scoop.sh) bucket holds manifests for companion apps and plugins for Elite Dangerous on PC. It's a fork of [nikkoura/scoop-bucket-elitedangerous](https://github.com/nikkoura/scoop-bucket-elitedangerous), with stalled version checks fixed and more apps added.

[![Tests](https://github.com/dylan-k/scoop-EliteDangerous/actions/workflows/ci.yml/badge.svg)](https://github.com/dylan-k/scoop-EliteDangerous/actions/workflows/ci.yml) [![Excavator](https://github.com/dylan-k/scoop-EliteDangerous/actions/workflows/excavator.yml/badge.svg)](https://github.com/dylan-k/scoop-EliteDangerous/actions/workflows/excavator.yml)


Install
-------

```powershell
scoop bucket add EliteDangerous https://github.com/dylan-k/scoop-EliteDangerous
scoop install EliteDangerous/<manifest>
```

Shortcuts go to the Start menu folder "Elite Dangerous Tools". EDMC plugins install into `%LocalAppData%\EDMarketConnector\plugins`, and Observatory plugins into Observatory's `plugins` folder.


Manifests
---------

Apps
: `edmc`, `eddi`, `eddiscovery`, `observatory-core`, `ed-materials-helper`, `ed-min-launcher`, `edjp`, `od-explorer`, `srvsurvey`

EDMC plugins
: `edmc-canonn`, `edmc-artemis-scanner-tracker`, `edmc-screenshot`, `edmc-edr`, `edmc-edsm-rse`, `edmc-spansh-router`

Observatory plugins
: `observatory-plugin-bioinsights`, `-boxelstats`, `-codexentries`, `-colliders`, `-evaluator`, `-signalmonitor`, `-telegram`


Notes
-----

- Version checks for GitHub-hosted apps read the release tag from the GitHub API (`checkver.url` plus `jsonpath`), because the older HTML scraping stopped matching GitHub's release pages.
- `eddi` extracts the per-user installer; it does not install EDDI's VoiceAttack plugin.
- The edjp page no longer lists `codexentries` and `signalmonitor`, so their version checks fail and they stay at their last versions.
