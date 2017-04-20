# npmdoc-webpack-visualizer-plugin

#### api documentation for  webpack-visualizer-plugin (v0.1.11)  [![npm package](https://img.shields.io/npm/v/npmdoc-webpack-visualizer-plugin.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webpack-visualizer-plugin) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webpack-visualizer-plugin.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webpack-visualizer-plugin)

####

[![NPM](https://nodei.co/npm/webpack-visualizer-plugin.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/webpack-visualizer-plugin)

- [https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "webpack-visualizer-plugin",
    "version": "0.1.11",
    "main": "lib/plugin.js",
    "author": "Chris Bateman (http://cbateman.com/)",
    "license": "MIT",
    "files": [
        "lib",
        "README.md"
    ],
    "repository": {
        "type": "git",
        "url": "git@github.com:chrisbateman/webpack-visualizer.git"
    },
    "scripts": {
        "build": "npm run buildsite && npm run buildplugin",
        "prebuildplugin": "rm -rf lib && mkdir lib",
        "buildplugin": "webpack src/plugin/main.jsx lib/pluginmain.js --config webpack.prod.js",
        "postbuildplugin": "babel src/plugin/plugin.js --out-file lib/plugin.js && cp src/shared/style.css lib",
        "prebuildsite": "rm -rf dist-site && mkdir dist-site",
        "buildsite": "webpack src/site/main.jsx dist-site/build.js --config webpack.prod.js && babel-node src/site/serverRender.js",
        "postbuildsite": "cp src/shared/style.css test/stats-demo.json dist-site",
        "dev": "webpack-dev-server --config webpack.dev.js",
        "lint": "eslint src --ext .js,.jsx",
        "preversion": "npm run lint && npm run build",
        "publishSite": "git checkout gh-pages && cp dist-site/* . && git add . && git commit -m 'release' && git push origin gh-pages && git checkout master"
    },
    "dependencies": {
        "d3": "^3.5.6",
        "mkdirp": "^0.5.1",
        "react": "^0.14.0",
        "react-dom": "^0.14.0"
    },
    "devDependencies": {
        "babel": "^5.8.23",
        "babel-core": "^5.8.25",
        "babel-loader": "^5.3.2",
        "eslint": "^1.6.0",
        "eslint-plugin-react": "^3.5.1",
        "merge": "^1.2.0",
        "webpack": "^1.12.2",
        "webpack-dev-server": "^1.12.0"
    },
    "engines": {
        "npm": ">=2.13.0"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
