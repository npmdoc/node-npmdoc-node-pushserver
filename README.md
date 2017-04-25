# npmdoc-node-pushserver

#### basic api documentation for  [node-pushserver (v0.5.4)](https://github.com/Smile-SA/node-pushserver)  [![npm package](https://img.shields.io/npm/v/npmdoc-node-pushserver.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-node-pushserver) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-pushserver.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-pushserver)

#### Cross-platform Push Notifications. A project providing a generic API to push messages using Apple's APN and Google's GCM services.

[![NPM](https://nodei.co/npm/node-pushserver.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/node-pushserver)

- [https://npmdoc.github.io/node-npmdoc-node-pushserver/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-node-pushserver/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "bin": {
        "pushserver": "./bin/pushserver.js"
    },
    "bugs": {
        "url": "https://github.com/Smile-SA/node-pushserver/issues"
    },
    "dependencies": {
        "apn": "~1.3.4",
        "commander": "2.7.1",
        "express": "~3.2.6",
        "lodash": "~1.3.1",
        "mongoose": "~3.6.11",
        "node-gcm": "~0.9.6"
    },
    "description": "Cross-platform Push Notifications. A project providing a generic API to push messages using Apple's APN and Google's GCM services.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "5a1de6131c55f5e3e897c1c130e58e1fbf99e603",
        "tarball": "https://registry.npmjs.org/node-pushserver/-/node-pushserver-0.5.4.tgz"
    },
    "gitHead": "19b7c37d4ca23a1d2782faa5bc0ed4b6c80051c9",
    "homepage": "https://github.com/Smile-SA/node-pushserver",
    "keywords": [
        "push",
        "gcm",
        "apn",
        "mongodb"
    ],
    "main": "./lib/PushController.js",
    "maintainers": [
        {
            "name": "smile"
        }
    ],
    "name": "node-pushserver",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/Smile-SA/node-pushserver.git"
    },
    "scripts": {
        "start": "node ./bin/pushserver.js",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "version": "0.5.4"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
