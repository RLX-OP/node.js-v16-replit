# Node.js 16 on replit

Steps:

1. Execute this script **on the shell** to install node (you can choose the version by editing the number 16) and configure npm.
```sh
npm init -y && npm i --save-dev node@16 && npm config set prefix=$(pwd)/node_modules/node && export PATH=$(pwd)/node_modules/node/bin:$PATH
```
Or if this does not work try:
```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.2/install.sh | bash && export NVM_DIR=\"$([ -z \"${XDG_CONFIG_HOME-}\" ] && printf %s \"${HOME}/.nvm\" || printf %s \"${XDG_CONFIG_HOME}/nvm\")\" && [ -s \"$NVM_DIR/nvm.sh\" ] && \\. \"$NVM_DIR/nvm.sh\" && nvm install 16 && nvm use 16
```

2. Create the [`.replit`](https://docs.repl.it/repls/dot-replit) to execute node from the shell instead of the console.
```
run = "npm start"
```

3. Make sure to add the start script in your package.json file
```js
  "scripts": {
    "start": "node ."
  }
```

4. (Optional) If you had packages like discord.js or sqlite before, you need to re-install those packages
```
npm uninstall discord.js && npm i discord.js
```
