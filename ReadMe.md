# Images Galleries for D-Day, Inc
Some things for making the iamge galleries at D-Day, Inc.

## Deployment
Eventually creates `siteContents/` folder with gallery contents for publishing to \<hosting destination>.

Currently done using the [thumbsup](https://thumbsup.github.io/) static gallery generator.

Examples of generating the gallery output:
```powershell
## using Node.js (with npm install of thumbsup)
Set-Location -Path src
## <do the npm install in this dir>
node node_modules/thumbsup/bin/thumbsup.js --config thumbsup_config.json

## or, using docker from the root of this repository
docker run --tty --volume "$(pwd):/work" --workdir /work/src ghcr.io/thumbsup/thumbsup thumbsup --config ./thumbsup_config.json
```

These result in said `/siteContents/` folder full of gallery things, which can then be used for subsequent deployment actions, like a GitHub Action GitHub Pages deployment