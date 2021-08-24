# Node.js 16/14 on replit

Steps:

1. Execute this script **on the shell** to install node (you can choose the version by editing the number 16) and configure npm.
```sh
npm init -y && npm i --save-dev node@16 && npm config set prefix=$(pwd)/node_modules/node && export PATH=$(pwd)/node_modules/node/bin:$PATH
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
