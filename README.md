# psgsreactprogrxjs
##2. Observers and Observables
###2 Reactive Programming
```
var result = movies.filter(function(movie){
  return movie.fitle[0] ==='4';
});
```

###3 Installing RxJS with npm
```
npm install rxjs --save
npm install webpack webpack-dev-server typescript typings ts-loader --save-dev
node_modules\.bin\typings install dt~es6-shim --global --save 
```

###4 Configuration and Setup
```
touch tsconfig.json
```
edit
```
{
  "compilerOptions":{
    "target":"es5",
    "module":"commonjs",
    "sourceMap":true
  }
}
```
then
```
touch webpack.config.js
```
```
module.exports = {
  entry:"./main",
  output:{filename:'app.js'},
  module:{
    loaders:[
      {
        test: /.ts$/,
        loader: "ts-loader"
      }
    ]
  },
  resolve:{
    extension:["",".ts",".js"]
  }
}
```


##3. Working with Observables
###6 Set up to Use the New Fetch Standard
```
node_modules\.bin\typings uninstall dt~es6-shim --global --save 
node_modules\.bin\typings install dt~whatwg-streams --global --save 
node_modules\.bin\typings install dt~whatwg-fetch --global --save 
```
tsconfig.json
edit
```
{
  "compilerOptions":{
    "target":"es6",
    "module":"commonjs",
    "sourceMap":true
  }
}
```
