# npmdoc-hapi-swagger

#### api documentation for  [hapi-swagger (v7.7.0)](https://github.com/glennjones/hapi-swagger#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-hapi-swagger.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-hapi-swagger) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-hapi-swagger.svg)](https://travis-ci.org/npmdoc/node-npmdoc-hapi-swagger)

#### A swagger documentation UI generator plugin for hapi

[![NPM](https://nodei.co/npm/hapi-swagger.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/hapi-swagger)

- [https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Glenn Jones"
    },
    "bugs": {
        "url": "https://github.com/glennjones/hapi-swagger/issues"
    },
    "dependencies": {
        "boom": "^4.0.0",
        "handlebars": "^4.0.5",
        "hoek": "^4.0.1",
        "http-status": "^1.0.1",
        "joi": "10.2.2",
        "json-schema-ref-parser": "^3.1.2",
        "swagger-parser": "^3.4.1"
    },
    "description": "A swagger documentation UI generator plugin for hapi",
    "devDependencies": {
        "blipp": "^2.3.0",
        "chalk": "^1.1.3",
        "code": "^4.0.0",
        "coveralls": "^2.11.11",
        "good": "^7.0.1",
        "good-console": "^6.1.2",
        "good-squeeze": "^5.0.1",
        "h2o2": "^5.1.0",
        "hapi": "^16.1.0",
        "hapi-api-version": "^1.1.0",
        "hapi-auth-basic": "^4.2.0",
        "hapi-auth-bearer-token": "^4.0.2",
        "hapi-auth-jwt2": "^7.0.1",
        "inert": "^4.0.1",
        "js2xmlparser": "^2.0.2",
        "jsonwebtoken": "^7.1.9",
        "lab": "^12.1.0",
        "swagger-client": "^2.1.14",
        "vision": "^4.0.1",
        "wreck": "^10.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "86b79ff50a0900110a9e83595941a9edbc7b6ad6",
        "tarball": "https://registry.npmjs.org/hapi-swagger/-/hapi-swagger-7.7.0.tgz"
    },
    "engines": {
        "node": ">=4.0.0"
    },
    "gitHead": "f32d6e4a5f8e0c533fef825fc37e4c56378db2fc",
    "homepage": "https://github.com/glennjones/hapi-swagger#readme",
    "keywords": [
        "api",
        "docs",
        "swagger",
        "hapi",
        "joi"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "glennjones"
        }
    ],
    "name": "hapi-swagger",
    "optionalDependencies": {},
    "peerDependencies": {
        "hapi": "^14.0.0 || ^15.0.0 || ^16.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/glennjones/hapi-swagger.git"
    },
    "scripts": {
        "start": "node ./bin/test-server.js",
        "test": "lab -L -t 100",
        "test-cov-coveralls": "lab -r lcov | ./node_modules/.bin/coveralls",
        "test-cov-html": "lab -r html -o coverage.html"
    },
    "version": "7.7.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
