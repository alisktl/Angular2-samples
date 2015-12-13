# Hello World

## Overview
Hello World improved sample.

## Install npm packages (in terminal)
1. ```npm init```
2. ```npm i angular2@2.0.0-alpha.44 systemjs@0.19.2 --save --save-exact```
3. ```npm i typescript live-server --save-dev```

## package.json

### ```package.json```
```package.json``` should look something like this:
```
{
  "name": "hello",
  "version": "1.0.0",
  "description": "Hello World improved sample.",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "alisher",
  "license": "ISC",
  "dependencies": {
    "angular2": "2.0.0-alpha.44",
    "systemjs": "0.19.2"
  },
  "devDependencies": {
    "live-server": "^0.9.0",
    "typescript": "^1.7.3"
  }
}
```

### ```script``` section
Find and replace ```script``` section with the following:
```
{
  "scripts": {
    "tsc": "tsc -p src -w",
    "start": "live-server --open=src"
  }
}
```

## ```tsconfig.json```
Change to the ```src``` folder and create a ```tsconfig.json``` file with the following content:
```
{
  "compilerOptions": {
    "target": "ES5",
    "module": "commonjs",
    "sourceMap": true,
    "emitDecoratorMetadata": true,
    "experimentalDecorators": true,
    "removeComments": false,
    "noImplicitAny": false
  }
}
```

## Compile the TypeScript to JavaScript
Type in terminal: ```npm run tsc```

## Run the app
Type in terminal: ```npm start```

## Result
Open link: ```http://127.0.0.1:8080/src/```

## Error
If your browser shows ```loading...```, you should install ```Browser ES6 support```

1. Type in terminal: ```npm install es6-shim --save```
2. It will create ```node_modules/``` directory
3. Add ```<script src="../node_modules/es6-shim/es6-shim.js"></script>``` in your ```index.html``` before other scripts
4. Open link: ```http://127.0.0.1:8080/src/```