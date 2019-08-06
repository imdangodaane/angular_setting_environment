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
yarn add @nebular/theme @angular/cdk @angular/animations
# Install eva-icons for Nebular
yarn add @nebular/eva-icons@next
# Add NbThemeModule to AppModule
# Install styles for Nebular -> config angular.json as follow:
"styles": [
  "node_modules/@nebular/theme/styles/prebuilt/default.css", // or dark.css
],
# Install bootstrap
yarn add bootstrap
# Add bootstrap.scss to angular.json
"styles": [
    "./node_modules/bootstrap/scss/bootstrap.scss",
    "src/styles.scss"
],
```
