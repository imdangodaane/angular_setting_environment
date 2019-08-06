Install Yarn on Ubuntu
```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt update
sudo apt install yarn
# Below command will install Yarn without nodejs package
sudo apt install --no-install-recommends yarn
# Verify version
yarn --version
```

Install Angular CLI
```bash
yarn add -g @angular/cli
```

Config Angular CLI using Yarn
```bash
ng config -g cli.packageManager yarn
# Turn back to npm anytime with:
ng config -g cli.packageManager npm
# Check angular-config.json:
cat ~/.angular-config.json
{
  "version": 1,
  "cli": {
    "packageManager": "yarn"
  }
}
```

Create new Angular project
```bash
ng new <new-project-name> --style=scss
# Install nebular
ng add @nebular/theme
# Install bootstrap
ng add bootstrap
ng add rxjs
ng add jquery
ng add popper.js
# Add bootstrap.scss to angular.json
"styles": [
    "./node_modules/bootstrap/scss/bootstrap.scss",
    "src/styles.scss"
],
```
