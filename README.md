# Mad Pterodactyl 1.0 Themes
## (Forked from OreoKitten)
 Themes for Pterodactyl 1.x

## Will this break my panel? (IMPORTANT)
This will not break your panel unless you use a diffrent theme version for a diffrent panel version, if it for some reason does break your panel it is simple to remove the theme.

## Panel Versioning
Make sure you use this theme only for 1.x, support will not be given for any other versions (e.g 0.7)

How do I install these themes?
Simple! Just follow the instructions below, mainly consisting of two or three changes you need to make before you build your panel (more on that below).

# Installing the Theme
# User Side
Create a file called `main.css` in `/var/www/pterodactyl/resources/scripts` by doing 

```js
nano /var/www/pterodactyl/resources/scripts/main.css
```

In that file put this text
```css
@import url(https://raw.githubusercontent.com/MadDoesGithub/PteroThemes/main/latest/Dark-n-Purple/user.css);
```
After that edit the file `index.tsx` in `/var/www/pterodactyl/resources/scripts`

On line 6 at the end of the imports section, add this:
```js
import './main.css';
```
After this build the pterodactyl panel (READ BELOW) and reload.

# Admin Side
In the file `admin.blade.php` in `/var/www/pterodactyl/resources/views/layouts/`, on line 36 put the text:

```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/MadDoesGithub/PteroThemes/main/latest/Dark-n-Purple/admin.css">
```
After this build the panel, read below.
After that just reload your panel and the theme is applied.

# Building Panel
## Install Dependencies
The following commands will install the necessary dependencies for building your panel.

# Install NodeJS
TIP:
You may have to add `sudo` to the following commands if you're not a root user.

## Using Nodesource
## Ubuntu/Debian
```bash
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
apt install -y nodejs
```

## CentOS
(Run these commands separately)
```bash
curl -sL https://rpm.nodesource.com/setup_12.x | sudo -E bash -
yum install -y nodejs # CentOS 7
dnf install -y nodejs # CentOS 8
```

By now, you should have NodeJS 12 installed. Make sure this is the case by checking `node -v`

## Using Node Version Manager (opens new window)
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
```
```bash
nvm install node
nvm alias default node
nvm use node
```
node -v should say 12.20.0 or newer else it will not work!

## Install Yarn and Panel Dependencies
### Install yarn

```bash
npm i -g yarn
```

## Now you need to make sure you are inside the pterodactyl panel directory
`cd /var/www/pterodactyl`

## Installs Pterodactyl Panel dependancies

```bash
yarn install
````
Run this inside your panel directory to apply changes (usually `/var/www/pterodactyl`)

# Build the Panel!
```bash
yarn build:production
```

## Enola - 1.2.0, 1.2.1, and 1.2.2
Instructions to install the theme Enola are here
[Enola 1.2.2(Latest Panel Version)](https://github.com/MadDoesGithub/PteroThemes/tree/main/latest/Enola)
![Preview](./preview/enola.png)


## Twilight - 1.1.3, 1.2.0, 1.2.1, 1.2.2
Instructions to install the theme Twilight are here
[Enola 1.2.2(Latest Panel Version)](https://github.com/MadDoesGithub/PteroThemes/tree/main/latest/Twilight)
![Preview](./preview/twilight.png)

## Recolor - 1.2.0, 1.2.1, 1.2.2
This theme is a recolor of the panel that you can edit, more information here
[Recolor](https://github.com/MadDoesGithub/PteroThemes/tree/main/latest/Recolor)

## Dracula - 1.2.0, 1.2.1, 1.2.2
This theme is a recolor of the panel that you can edit, more information here
[Dracula 1.2.2(Latest Panel Version)](https://github.com/MadDoesGithub/PteroThemes/tree/main/latest/Dracula)
![Preview](./preview/Dracula.png)
![Preview](./preview/Dracula2.png)

## If you have suggestions, DM me at Mad#7010
