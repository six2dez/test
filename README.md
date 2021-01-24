<h1 align="center">
  <br>
  <a href="https://github.com/six2dez/reconftw"><img src="https://i.ibb.co/cYXL58B/banner.png" alt="Photon"></a>
  <br>
  ReconFTW
  <br>
</h1>

<h4 align="center">Automated framework for performing recon</h4>

<p align="center">
  <a href="https://github.com/six2dez/reconftw/releases/tag/0.9-beta1">
    <img src="https://img.shields.io/badge/release-0.9--beta1-green">
  </a>
   </a>
  <a href="https://www.gnu.org/licenses/gpl-3.0.en.html">
      <img src="https://img.shields.io/badge/license-GPL3-_red.svg">
  </a>
  <a href="/">
    <img src="https://img.shields.io/badge/forks-2k%2B-yellow"
         alt="pypi">
  </a>
  <a href="https://twitter.com/Six2dez1">
    <img src="https://img.shields.io/badge/twitter-%40Six2dez1-blue">
  </a>
</p>

:warning: ***Warning*** :warning:

This is a live development project, until the first stable release (1.0) it will be constantly updated in master branch, so if you have detected any bug, you can open an issue or ping me over Telegram (@six2dez) or Twitter (@six2dez1) and I will try to do my best :)

# Table of Contents
-   [Summary](#summary)
-   [Installation](#installation)
-   [Usage](#usage)
-   [Mindmap](#mindmapworkflow)
-   [Requirements](#requirements)
-   [Usage examples](#usage-examples)
-   [Improvement plan](#improvement-plan)
-   [Thanks](#thanks)



## Summary

ReconFTW performs automated enumeration of subdomains via various techniques and futher scanning for vulnerabilties, to give you a potential vulns.


## Installation
- Requires [Golang](https://golang.org/dl/) > 1.14 installed and env vars correctly set ($GOPATH,$GOROOT)
Run ./install.sh before first run (apt, rpm, pacman compatible)

```bash
git clone https://github.com/six2dez/reconftw
cd reconftw
chmod +x *.sh
./install.sh
./reconftw.sh -d target.com -a
```

## Usage
```
ReconFTW 0.91-beta1

TARGET OPTIONS
-d DOMAIN        Target domain
-l list.txt      Targets list, one per line

MODE OPTIONS
-a               Perform all checks
-s               Full subdomains scan (Subs, tko and probe)
-g               Google dorks searchs
-w               Perform web checks only without subs (-l required)
-t               Check subdomain takeover(-l required)
-i               Check all needed tools
-v               Debug/verbose mode, no file descriptor redir
-h               Show this help

SUBDOMAIN OPTIONS
--sp             Passive subdomain scans
--sb             Bruteforce subdomain resolution
--sr             Subdomain permutations and resolution (-l required)
--ss             Subdomain scan by scraping (-l required)

OUTPUT OPTIONS
-o output/path   Define output folder


```


<p align="center">
  <a href="https://github.com/s0md3v/Photon/wiki">Photon Wiki</a> •
  <a href="https://github.com/s0md3v/Photon/wiki/Usage">How To Use</a> •
  <a href="https://github.com/s0md3v/Photon/wiki/Compatibility-&-Dependencies">Compatibility</a> •
  <a href="https://github.com/s0md3v/Photon/wiki/Photon-Library">Photon Library</a> •
  <a href="#contribution--license">Contribution</a> •
  <a href="https://github.com/s0md3v/Photon/projects/1">Roadmap</a>
</p>
