Allows you to modify the resolve section of webpack config.  
see https://webpack.js.org/configuration/resolve/ for all config options.

In `craco.config.js` file
```js
import webpackResolve from "craco-webpack-resolve"

//for example, if we need to add the zlib fallback
export default {
    plugins: [
        { 
            plugin: webpackResolve, 
            resolve: {
                fallback: {
                    zlib: require.resolve('browserify-zlib')
                }
            } 
        }
    ]
};
```