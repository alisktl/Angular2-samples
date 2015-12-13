# Hello World

## Overview
Hello World sample.

## Install live-server
```npm install -g live-server```

## Run live-server
Type in terminal: ```live-server```

## Result
Open link: ```http://127.0.0.1:8080```

## Error
If your browser shows ```loading...```, you should install ```Browser ES6 support```

1. Type in terminal: ```npm install es6-shim --save```
2. It will create ```node_modules/``` directory
3. Add ```<script src="../node_modules/es6-shim/es6-shim.js"></script>``` in your ```index.html``` before other scripts
4. Open link: ```http://127.0.0.1:8080```