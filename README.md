# api documentation for  [webpack-visualizer-plugin (v0.1.11)](https://github.com/chrisbateman/webpack-visualizer#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-webpack-visualizer-plugin.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-webpack-visualizer-plugin) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-webpack-visualizer-plugin.svg)](https://travis-ci.org/npmdoc/node-npmdoc-webpack-visualizer-plugin)
#### Visualize and analyze your Webpack bundle to see which modules are taking up space and which might be duplicates.

[![NPM](https://nodei.co/npm/webpack-visualizer-plugin.png?downloads=true)](https://www.npmjs.com/package/webpack-visualizer-plugin)

[![apidoc](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-webpack-visualizer-plugin_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-webpack-visualizer-plugin/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Chris Bateman",
        "url": "http://cbateman.com/"
    },
    "bugs": {
        "url": "https://github.com/chrisbateman/webpack-visualizer/issues"
    },
    "dependencies": {
        "d3": "^3.5.6",
        "mkdirp": "^0.5.1",
        "react": "^0.14.0",
        "react-dom": "^0.14.0"
    },
    "description": "Visualize and analyze your Webpack bundle to see which modules are taking up space and which might be duplicates.",
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
    "directories": {},
    "dist": {
        "shasum": "b8770ad86b4f652612c68b1b782253faf9f8a34e",
        "tarball": "https://registry.npmjs.org/webpack-visualizer-plugin/-/webpack-visualizer-plugin-0.1.11.tgz"
    },
    "engines": {
        "npm": ">=2.13.0"
    },
    "files": [
        "lib",
        "README.md"
    ],
    "gitHead": "ea9ed0b8e8c83b45c398aa7605f9d8478f031f23",
    "homepage": "https://github.com/chrisbateman/webpack-visualizer#readme",
    "license": "MIT",
    "main": "lib/plugin.js",
    "maintainers": [
        {
            "name": "chrisbateman",
            "email": "chris@cbateman.com"
        }
    ],
    "name": "webpack-visualizer-plugin",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/chrisbateman/webpack-visualizer.git"
    },
    "scripts": {
        "build": "npm run buildsite && npm run buildplugin",
        "buildplugin": "webpack src/plugin/main.jsx lib/pluginmain.js --config webpack.prod.js",
        "buildsite": "webpack src/site/main.jsx dist-site/build.js --config webpack.prod.js && babel-node src/site/serverRender.js",
        "dev": "webpack-dev-server --config webpack.dev.js",
        "lint": "eslint src --ext .js,.jsx",
        "postbuildplugin": "babel src/plugin/plugin.js --out-file lib/plugin.js && cp src/shared/style.css lib",
        "postbuildsite": "cp src/shared/style.css test/stats-demo.json dist-site",
        "prebuildplugin": "rm -rf lib && mkdir lib",
        "prebuildsite": "rm -rf dist-site && mkdir dist-site",
        "preversion": "npm run lint && npm run build",
        "publishSite": "git checkout gh-pages && cp dist-site/* . && git add . && git commit -m 'release' && git push origin gh-pages && git checkout master"
    },
    "version": "0.1.11"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module webpack-visualizer-plugin](#apidoc.module.webpack-visualizer-plugin)



# <a name="apidoc.module.webpack-visualizer-plugin"></a>[module webpack-visualizer-plugin](#apidoc.module.webpack-visualizer-plugin)



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
