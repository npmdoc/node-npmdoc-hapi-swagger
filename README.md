# api documentation for  [hapi-swagger (v7.7.0)](https://github.com/glennjones/hapi-swagger#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-hapi-swagger.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-hapi-swagger) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-hapi-swagger.svg)](https://travis-ci.org/npmdoc/node-npmdoc-hapi-swagger)
#### A swagger documentation UI generator plugin for hapi

[![NPM](https://nodei.co/npm/hapi-swagger.png?downloads=true)](https://www.npmjs.com/package/hapi-swagger)

[![apidoc](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-hapi-swagger_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-hapi-swagger/build/apidoc.html)

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
            "name": "glennjones",
            "email": "glennjonesnet@gmail.com"
        }
    ],
    "name": "hapi-swagger",
    "optionalDependencies": {},
    "peerDependencies": {
        "hapi": "^14.0.0 || ^15.0.0 || ^16.0.0"
    },
    "readme": "ERROR: No README data found!",
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



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module hapi-swagger](#apidoc.module.hapi-swagger)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>definitions (settings)](#apidoc.element.hapi-swagger.definitions)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>paths (settings)](#apidoc.element.hapi-swagger.paths)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>properties (settings, definitionCollection, altDefinitionCollection, definitionCache )](#apidoc.element.hapi-swagger.properties)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>register (plugin, options, next)](#apidoc.element.hapi-swagger.register)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>responses (settings, definitionCollection, altDefinitionCollection, definitionCache)](#apidoc.element.hapi-swagger.responses)
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>builder
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>definitions.prototype
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>filter
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>group
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>info
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>parameters
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>paths.prototype
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>properties.prototype
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>responses.prototype
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>sort
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>tags
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>utilities
1.  object <span class="apidocSignatureSpan">hapi-swagger.</span>validate

#### [module hapi-swagger.builder](#apidoc.module.hapi-swagger.builder)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.builder.</span>dereference (schema, callback)](#apidoc.element.hapi-swagger.builder.dereference)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.builder.</span>getSwaggerJSON (settings, request, callback)](#apidoc.element.hapi-swagger.builder.getSwaggerJSON)
1.  object <span class="apidocSignatureSpan">hapi-swagger.builder.</span>default
1.  object <span class="apidocSignatureSpan">hapi-swagger.builder.</span>schema

#### [module hapi-swagger.definitions](#apidoc.module.hapi-swagger.definitions)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>definitions (settings)](#apidoc.element.hapi-swagger.definitions.definitions)

#### [module hapi-swagger.definitions.prototype](#apidoc.module.hapi-swagger.definitions.prototype)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.definitions.prototype.</span>append (definitionName, definition, currentCollection, settings)](#apidoc.element.hapi-swagger.definitions.prototype.append)

#### [module hapi-swagger.filter](#apidoc.module.hapi-swagger.filter)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.filter.</span>byTags (tags, routes)](#apidoc.element.hapi-swagger.filter.byTags)

#### [module hapi-swagger.group](#apidoc.module.hapi-swagger.group)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.group.</span>appendGroupByPath (pathPrefixSize, basePath, routes, pathReplacements)](#apidoc.element.hapi-swagger.group.appendGroupByPath)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.group.</span>getNameByPath (pathPrefixSize, basePath, path, pathReplacements)](#apidoc.element.hapi-swagger.group.getNameByPath)

#### [module hapi-swagger.info](#apidoc.module.hapi-swagger.info)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.info.</span>build (options)](#apidoc.element.hapi-swagger.info.build)
1.  object <span class="apidocSignatureSpan">hapi-swagger.info.</span>defaults
1.  object <span class="apidocSignatureSpan">hapi-swagger.info.</span>schema

#### [module hapi-swagger.parameters](#apidoc.module.hapi-swagger.parameters)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.parameters.</span>fromProperties (schemaObj, parameterType)](#apidoc.element.hapi-swagger.parameters.fromProperties)
1.  object <span class="apidocSignatureSpan">hapi-swagger.parameters.</span>allowedProps

#### [module hapi-swagger.paths](#apidoc.module.hapi-swagger.paths)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>paths (settings)](#apidoc.element.hapi-swagger.paths.paths)

#### [module hapi-swagger.paths.prototype](#apidoc.module.hapi-swagger.paths.prototype)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>build (routes)](#apidoc.element.hapi-swagger.paths.prototype.build)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>buildRoutes (routes)](#apidoc.element.hapi-swagger.paths.prototype.buildRoutes)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>getDefaultStructures ()](#apidoc.element.hapi-swagger.paths.prototype.getDefaultStructures)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>getSwaggerStructures (joiObj, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.paths.prototype.getSwaggerStructures)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>testParameterError (joiObj, parameterType, path)](#apidoc.element.hapi-swagger.paths.prototype.testParameterError)

#### [module hapi-swagger.properties](#apidoc.module.hapi-swagger.properties)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>properties (settings, definitionCollection, altDefinitionCollection, definitionCache )](#apidoc.element.hapi-swagger.properties.properties)

#### [module hapi-swagger.properties.prototype](#apidoc.module.hapi-swagger.properties.prototype)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>getDefinitionCollection (isAlt)](#apidoc.element.hapi-swagger.properties.prototype.getDefinitionCollection)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>getDefinitionRef (isAlt)](#apidoc.element.hapi-swagger.properties.prototype.getDefinitionRef)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseAlternatives (property, joiObj, name, parameterType, useDefinitions)](#apidoc.element.hapi-swagger.properties.prototype.parseAlternatives)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseArray (property, joiObj, name, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseArray)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseDate (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseDate)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseNumber (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseNumber)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseObject (property, joiObj, name, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseObject)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseProperty (name, joiObj, parent, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseProperty)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parsePropertyMetadata (property, name, parent, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parsePropertyMetadata)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseString (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseString)

#### [module hapi-swagger.responses](#apidoc.module.hapi-swagger.responses)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.</span>responses (settings, definitionCollection, altDefinitionCollection, definitionCache)](#apidoc.element.hapi-swagger.responses.responses)

#### [module hapi-swagger.responses.prototype](#apidoc.module.hapi-swagger.responses.prototype)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>build (userDefindedSchemas, defaultSchema, statusSchemas, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.responses.prototype.build)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>getResponse (statusCode, joiObj, useDefinitions)](#apidoc.element.hapi-swagger.responses.prototype.getResponse)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>optionOverride (discoveredSchemas, userDefindedSchemas, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.responses.prototype.optionOverride)

#### [module hapi-swagger.sort](#apidoc.module.hapi-swagger.sort)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.sort.</span>paths (sortType, routes)](#apidoc.element.hapi-swagger.sort.paths)

#### [module hapi-swagger.tags](#apidoc.module.hapi-swagger.tags)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.tags.</span>build (settings)](#apidoc.element.hapi-swagger.tags.build)
1.  object <span class="apidocSignatureSpan">hapi-swagger.tags.</span>schema

#### [module hapi-swagger.utilities](#apidoc.module.hapi-swagger.utilities)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>createId (method, path)](#apidoc.element.hapi-swagger.utilities.createId)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>deleteEmptyProperties (obj)](#apidoc.element.hapi-swagger.utilities.deleteEmptyProperties)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>findAndRenameKey (obj, findKey, replaceKey)](#apidoc.element.hapi-swagger.utilities.findAndRenameKey)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>first (array)](#apidoc.element.hapi-swagger.utilities.first)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>firstBy (f, d)](#apidoc.element.hapi-swagger.utilities.firstBy)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>geJoiLabel (joiObj)](#apidoc.element.hapi-swagger.utilities.geJoiLabel)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>getJoiMetaProperty (joiObj, propertyName)](#apidoc.element.hapi-swagger.utilities.getJoiMetaProperty)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasJoiChildren (joiObj)](#apidoc.element.hapi-swagger.utilities.hasJoiChildren)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasJoiMeta (joiObj)](#apidoc.element.hapi-swagger.utilities.hasJoiMeta)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasKey (obj, findKey)](#apidoc.element.hapi-swagger.utilities.hasKey)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasProperties (obj)](#apidoc.element.hapi-swagger.utilities.hasProperties)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isFunction (obj)](#apidoc.element.hapi-swagger.utilities.isFunction)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isJoi (joiObj)](#apidoc.element.hapi-swagger.utilities.isJoi)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isObject (obj)](#apidoc.element.hapi-swagger.utilities.isObject)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isRegex (obj)](#apidoc.element.hapi-swagger.utilities.isRegex)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>removeProps (obj, listOfProps)](#apidoc.element.hapi-swagger.utilities.removeProps)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>removeTrailingSlash (str)](#apidoc.element.hapi-swagger.utilities.removeTrailingSlash)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>replaceInPath (path, applyTo, options)](#apidoc.element.hapi-swagger.utilities.replaceInPath)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>replaceValue (array, current, replacement)](#apidoc.element.hapi-swagger.utilities.replaceValue)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>sortFirstItem (array, firstItem)](#apidoc.element.hapi-swagger.utilities.sortFirstItem)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>startsWith (str, test)](#apidoc.element.hapi-swagger.utilities.startsWith)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>toJoiObject (obj)](#apidoc.element.hapi-swagger.utilities.toJoiObject)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>toTitleCase (word)](#apidoc.element.hapi-swagger.utilities.toTitleCase)

#### [module hapi-swagger.validate](#apidoc.module.hapi-swagger.validate)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.validate.</span>log (doc, logFnc)](#apidoc.element.hapi-swagger.validate.log)
1.  [function <span class="apidocSignatureSpan">hapi-swagger.validate.</span>test (doc, next)](#apidoc.element.hapi-swagger.validate.test)



# <a name="apidoc.module.hapi-swagger"></a>[module hapi-swagger](#apidoc.module.hapi-swagger)

#### <a name="apidoc.element.hapi-swagger.definitions"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>definitions (settings)](#apidoc.element.hapi-swagger.definitions)
- description and source-code
```javascript
definitions = function (settings) {

    this.settings = settings;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.hapi-swagger.paths"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>paths (settings)](#apidoc.element.hapi-swagger.paths)
- description and source-code
```javascript
paths = function (settings) {

    this.settings = settings;
    this.definitions = new Definitions(settings);
    this.properties = new Properties(settings, {}, {});
    this.responses = new Responses(settings, {}, {});


    this.defaults = {
        responses: {}
    };

    this.schema = Joi.object({
        tags: Joi.array().items(Joi.string()),
        summary: Joi.string(),
        description: Joi.string(),
        externalDocs: Joi.object({
            description: Joi.string(),
            url: Joi.string().uri()
        }),
        operationId: Joi.string(),
        consumes: Joi.array().items(Joi.string()),
        produces: Joi.array().items(Joi.string()),
        parameters: Joi.array().items(Joi.object()),
        responses: Joi.object().required(),
        schemes: Joi.array().items(Joi.string().valid(['http', 'https', 'ws', 'wss'])),
        deprecated: Joi.boolean(),
        security: Joi.array().items(Joi.object())
    });
}
```
- example usage
```shell
...

out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);

// filter routes displayed based on tags passed in query string
if (request.query.tags) {
    let filterTags = request.query.tags.split(',');
    routes = Filter.byTags(filterTags, routes);
}
...
```

#### <a name="apidoc.element.hapi-swagger.properties"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>properties (settings, definitionCollection, altDefinitionCollection, definitionCache )](#apidoc.element.hapi-swagger.properties)
- description and source-code
```javascript
properties = function (settings, definitionCollection, altDefinitionCollection, definitionCache ) {

    this.settings = settings;
    this.definitionCollection = definitionCollection;
    this.altDefinitionCollection = altDefinitionCollection;
    // definitionCache has to be an array of two WeakMaps
    this.definitionCache = definitionCache;

    this.definitions = new Definitions(settings);


    // swagger type can be 'string', 'number', 'integer', 'boolean', 'array' or 'file'
    this.simpleTypePropertyMap = {
        'boolean': { 'type': 'boolean' },
        'binary': { 'type': 'string', 'format': 'binary' },
        'date': { 'type': 'string', 'format': 'date' },
        'number': { 'type': 'number' },
        'string': { 'type': 'string' }
    };

    this.complexTypePropertyMap = {
        'any': { 'type': 'string' },
        'array': { 'type': 'array' },
        'func': { 'type': 'string' },
        'object': { 'type': 'object' },
        'alternatives': { 'type': 'alternatives' }
    };

    // merge
    this.propertyMap = Hoek.applyToDefaults(this.simpleTypePropertyMap, this.complexTypePropertyMap);

    //this.allowedProps = ['$ref','format','title','description','default','multipleOf','maximum','exclusiveMaximum','minimum','
exclusiveMinimum','maxLength','minLength','pattern','maxItems','minItems','uniqueItems','maxProperties','minProperties','required
','enum','type','items','allOf','properties','additionalProperties','discriminator','readOnly','xml','externalDocs','example'];
    // add none swagger property needed to flag touched state of required property
    //this.allowedProps.push('optional');
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.hapi-swagger.register"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>register (plugin, options, next)](#apidoc.element.hapi-swagger.register)
- description and source-code
```javascript
register = function (plugin, options, next) {


    let settings = Hoek.applyToDefaults(Defaults, options, true);
    const publicDirPath = Path.resolve(__dirname, '..', 'public');
    const swaggerDirPath = Path.join(publicDirPath, 'swaggerui');

    settings.log = (tags, data) => {

        tags.unshift('hapi-swagger');
        if (settings.debug) {
            plugin.log(tags, data);
        }
    };
    settings.log(['info'], 'Started');

    // add server method for caching
    if (settings.cache) {
        // set default
        settings.cache.segment = 'hapi-swagger';
        if (!settings.cache.generateTimeout) {
            settings.cache.generateTimeout = 30 * 1000;
        }

        plugin.method('getSwaggerJSON', Builder.getSwaggerJSON, {
            cache: settings.cache,
            generateKey: () => {

                return 'hapi-swagger';
            }
        });
    }


    // add routing swagger json
    plugin.route([{
        method: 'GET',
        path: settings.jsonPath,
        config: {
            auth: settings.auth,
            cors: settings.cors,
            handler: (request, reply) => {

                Joi.assert(settings, schema);

                if (settings.cache) {
<span class="apidocCodeCommentSpan">                    /*eslint no-unused-vars:0 */
</span>                    plugin.methods.getSwaggerJSON(settings, request, (err, json, cached, report) => {

                        /* $lab:coverage:off$ */
                        if (err) {
                            reply(err);
                            /* $lab:coverage:on$ */
                        } else {
                            //console.log(JSON.stringify(report));
                            const lastModified = cached ? new Date(cached.stored) : new Date();
                            reply(json).header('last-modified', lastModified.toUTCString());
                        }
                    });
                } else {
                    Joi.assert(settings, schema);
                    Builder.getSwaggerJSON(settings, request, (err, json) => {

                        reply(json);
                    });
                }
            },
            plugins: {
                'hapi-swagger': false
            }
        }
    }]);


    // only add 'inert' and 'vision' based routes if needed
    if (settings.documentationPage === true || settings.swaggerUI === true) {

        // make sure we have other plug-in dependencies
        plugin.dependency(['inert', 'vision'], (pluginWithDependencies, nextWithDependencies) => {

            // add routing for swaggerui static assets /swaggerui/
            pluginWithDependencies.views({
                engines: {
                    html: {
                        module: require('handlebars')
                    }
                },
                path: swaggerDirPath
            });

            // add documentation page
            if (settings.documentationPage === true) {
                pluginWithDependencies.route([{
                    method: 'GET',
                    path: settings.documentationPath,
                    config: {
                        auth: settings.auth
                    },
                    handler: (request, reply) => {

                        reply.view('index.html', {});
                    }
                }]);
            }

            // add swagger UI if asked for or need by documentation page
            if (settings.documentationPage === true || settings.swaggerUI === true) {
                pluginWithDependencies.route([{
                    method: 'GET',
                    path: settings.swaggerUIPath + '{path*}',
                    config: {
                        auth: settings.auth
                    },
                    handler: {
                        directory: {
                            path: swaggerDirPath + Path.sep,
                            listing: true,
                            index: false
                        }
                    }
                }, {
                    method: 'GET',
                    path: settings.swaggerUIPath + ' ...
```
- example usage
```shell
...
const options = {
info: {
        'title': 'Test API Documentation',
        'version': Pack.version,
    }
};

server.register([
Inert,
Vision,
{
    'register': HapiSwagger,
    'options': options
}], (err) => {
    server.start( (err) => {
...
```

#### <a name="apidoc.element.hapi-swagger.responses"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>responses (settings, definitionCollection, altDefinitionCollection, definitionCache)](#apidoc.element.hapi-swagger.responses)
- description and source-code
```javascript
responses = function (settings, definitionCollection, altDefinitionCollection, definitionCache) {

    this.settings = settings;
    this.definitionCollection = definitionCollection;
    this.altDefinitionCollection = altDefinitionCollection;

    this.definitions = new Definitions(settings);
    this.properties = new Properties(settings, this.definitionCollection, this.altDefinitionCollection, definitionCache);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.hapi-swagger.builder"></a>[module hapi-swagger.builder](#apidoc.module.hapi-swagger.builder)

#### <a name="apidoc.element.hapi-swagger.builder.dereference"></a>[function <span class="apidocSignatureSpan">hapi-swagger.builder.</span>dereference (schema, callback)](#apidoc.element.hapi-swagger.builder.dereference)
- description and source-code
```javascript
dereference = function (schema, callback) {

    JSONDeRef.dereference(schema, function (err, json) {

        if (!err) {
            delete json.definitions;
            delete json['x-alt-definitions'];
        } else {
            err = { 'error': 'fail to dereference schema' };
        }
        callback(err, json);
    });
}
```
- example usage
```shell
...
    out = internals.removeNoneSchemaOptions(out);

    if (settings.debug) {
        Validate.log(out, settings.log);
    }

    if (settings.deReference === true) {
        builder.dereference(out, callback);
    } else {
        callback(null, out);
    }
};


/**
...
```

#### <a name="apidoc.element.hapi-swagger.builder.getSwaggerJSON"></a>[function <span class="apidocSignatureSpan">hapi-swagger.builder.</span>getSwaggerJSON (settings, request, callback)](#apidoc.element.hapi-swagger.builder.getSwaggerJSON)
- description and source-code
```javascript
getSwaggerJSON = function (settings, request, callback) {

    // remove items that cannot be changed by user
    delete settings.swagger;
    let connection = request.connection;
    let namedConnection = null;

    if (settings.connectionLabel) {
        connection = namedConnection = request.server.select(settings.connectionLabel).connections[0];
        if (request.server.select(settings.connectionLabel).connections.length === 1) {
            request.server.log(['error'], 'connectionLabel should only define one connection to document');
        }
    }

    // collect root information
    builder.default.host = internals.getHost(request, namedConnection);
    builder.default.schemes = [internals.getSchema(request, connection)];

    settings = Hoek.applyToDefaults(builder.default, settings);
    if (settings.basePath !== '/') {
        settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
    }
    let out = internals.removeNoneSchemaOptions(settings);
    Joi.assert(out, builder.schema);


    out.info = Info.build(settings);
    out.tags = Tags.build(settings);

    let routes = connection.table();

    routes = Filter.byTags(['api'], routes);
    Sort.paths(settings.sortPaths, routes);

    // filter routes displayed based on tags passed in query string
    if (request.query.tags) {
        let filterTags = request.query.tags.split(',');
        routes = Filter.byTags(filterTags, routes);
    }

    // append group property - by path
    Group.appendGroupByPath(settings.pathPrefixSize, settings.basePath, routes, settings.pathReplacements);

    let paths = new Paths(settings);
    let pathData = paths.build(routes);
    out.paths = pathData.paths;
    out.definitions = pathData.definitions;
    if (Utilities.hasProperties(pathData['x-alt-definitions'])) {
        out['x-alt-definitions'] = pathData['x-alt-definitions'];
    }
    out = internals.removeNoneSchemaOptions(out);

    if (settings.debug) {
        Validate.log(out, settings.log);
    }

    if (settings.deReference === true) {
        builder.dereference(out, callback);
    } else {
        callback(null, out);
    }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.hapi-swagger.definitions"></a>[module hapi-swagger.definitions](#apidoc.module.hapi-swagger.definitions)

#### <a name="apidoc.element.hapi-swagger.definitions.definitions"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>definitions (settings)](#apidoc.element.hapi-swagger.definitions.definitions)
- description and source-code
```javascript
definitions = function (settings) {

    this.settings = settings;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.hapi-swagger.definitions.prototype"></a>[module hapi-swagger.definitions.prototype](#apidoc.module.hapi-swagger.definitions.prototype)

#### <a name="apidoc.element.hapi-swagger.definitions.prototype.append"></a>[function <span class="apidocSignatureSpan">hapi-swagger.definitions.prototype.</span>append (definitionName, definition, currentCollection, settings)](#apidoc.element.hapi-swagger.definitions.prototype.append)
- description and source-code
```javascript
append = function (definitionName, definition, currentCollection, settings) {

    let out = null;

    definition = internals.formatProperty(definition);

    // remove required if its not an array
    //if (definition.required && !Array.isArray(definition.required)) {
    //    delete definition.required;
    //}

    // remove unneeded properties
    delete definition.name;

    // find existing definition by this definitionName
    let foundDefinition = currentCollection[definitionName];
    if (foundDefinition) {
        // deep compare objects
        if (Hoek.deepEqual(foundDefinition, definition)) {
            // return existing definitionName if existing object is exactly the same
            out = definitionName;
        } else {
            // create new definition
            out = internals.append(null, definition, currentCollection, settings);
        }
    } else {
        // create new definition
        out = internals.append(definitionName, definition, currentCollection, settings);
    }

    return out;
}
```
- example usage
```shell
...
if (foundDefinition) {
    // deep compare objects
    if (Hoek.deepEqual(foundDefinition, definition)) {
        // return existing definitionName if existing object is exactly the same
        out = definitionName;
    } else {
        // create new definition
        out = internals.append(null, definition, currentCollection, settings);
    }
} else {
    // create new definition
    out = internals.append(definitionName, definition, currentCollection, settings);
}

return out;
...
```



# <a name="apidoc.module.hapi-swagger.filter"></a>[module hapi-swagger.filter](#apidoc.module.hapi-swagger.filter)

#### <a name="apidoc.element.hapi-swagger.filter.byTags"></a>[function <span class="apidocSignatureSpan">hapi-swagger.filter.</span>byTags (tags, routes)](#apidoc.element.hapi-swagger.filter.byTags)
- description and source-code
```javascript
byTags = function (tags, routes) {

    let tag;

    return routes.filter((route) => {

        let exit;
        for (let i = 0; i < tags.length; i++) {
            switch (tags[i].substring(0, 1)) {
                case '-': // exclude tags that match this case
                    tag = tags[i].substring(1, tags[i].length);
                    if (Hoek.intersect(route.settings.tags, [tag]).length > 0) {
                        exit = true;
                    }
                    break;
                case '+': // (+) filter out tagged paths that do not have this tag!
                    tag = tags[i].substring(1, tags[i].length);
                    if (Hoek.intersect(route.settings.tags, [tag]).length === 0) {
                        exit = true;
                    }
                    break;
            }
        }

        // if we have reason to exit, then do so!
        if (exit === true) {
            return false;
        }

        // default behavior for tags is additive
        if (Hoek.intersect(route.settings.tags, tags).length > 0) {
            return true;
        }

        // fallback or no tag defined
        return false;
    });
}
```
- example usage
```shell
...


out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);

// filter routes displayed based on tags passed in query string
if (request.query.tags) {
    let filterTags = request.query.tags.split(',');
    routes = Filter.byTags(filterTags, routes);
}
...
```



# <a name="apidoc.module.hapi-swagger.group"></a>[module hapi-swagger.group](#apidoc.module.hapi-swagger.group)

#### <a name="apidoc.element.hapi-swagger.group.appendGroupByPath"></a>[function <span class="apidocSignatureSpan">hapi-swagger.group.</span>appendGroupByPath (pathPrefixSize, basePath, routes, pathReplacements)](#apidoc.element.hapi-swagger.group.appendGroupByPath)
- description and source-code
```javascript
appendGroupByPath = function (pathPrefixSize, basePath, routes, pathReplacements) {

    let out = [];

    routes.forEach((route) => {
        let prefix = group.getNameByPath(pathPrefixSize, basePath, route.path, pathReplacements);
        // append tag reference to route
        route.group = [prefix];
        if (out.indexOf(prefix) === -1) {
            out.push(prefix);
        }
    });

    return out;
}
```
- example usage
```shell
...
// filter routes displayed based on tags passed in query string
if (request.query.tags) {
    let filterTags = request.query.tags.split(',');
    routes = Filter.byTags(filterTags, routes);
}

// append group property - by path
Group.appendGroupByPath(settings.pathPrefixSize, settings.basePath, routes, settings.pathReplacements);

let paths = new Paths(settings);
let pathData = paths.build(routes);
out.paths = pathData.paths;
out.definitions = pathData.definitions;
if (Utilities.hasProperties(pathData['x-alt-definitions'])) {
    out['x-alt-definitions'] = pathData['x-alt-definitions'];
...
```

#### <a name="apidoc.element.hapi-swagger.group.getNameByPath"></a>[function <span class="apidocSignatureSpan">hapi-swagger.group.</span>getNameByPath (pathPrefixSize, basePath, path, pathReplacements)](#apidoc.element.hapi-swagger.group.getNameByPath)
- description and source-code
```javascript
getNameByPath = function (pathPrefixSize, basePath, path, pathReplacements) {


    if (pathReplacements) {
        path = Utilities.replaceInPath(path, ['groups'], pathReplacements);
    }

    let i = 0;
    let pathHead = [];
    let parts = path.split('/');

    while (parts.length > 0) {
        let item = parts.shift();

        if (item !== '') {
            pathHead.push(item);
            i++;
        }
        if (i >= pathPrefixSize) {
            break;
        }
    }
    let name = pathHead.join('/');

    if (basePath !== '/' && Utilities.startsWith('/' + name, basePath)) {

        name = ('/' + name).replace(basePath, '');

        if (Utilities.startsWith(name, '/')) {
            name = name.replace('/', '');
        }
    }
    return name;
}
```
- example usage
```shell
...
 * @return {Array}
 */
group.appendGroupByPath = function (pathPrefixSize, basePath, routes, pathReplacements) {

let out = [];

routes.forEach((route) => {
    let prefix = group.getNameByPath(pathPrefixSize, basePath, route.path, pathReplacements);
    // append tag reference to route
    route.group = [prefix];
    if (out.indexOf(prefix) === -1) {
        out.push(prefix);
    }
});
...
```



# <a name="apidoc.module.hapi-swagger.info"></a>[module hapi-swagger.info](#apidoc.module.hapi-swagger.info)

#### <a name="apidoc.element.hapi-swagger.info.build"></a>[function <span class="apidocSignatureSpan">hapi-swagger.info.</span>build (options)](#apidoc.element.hapi-swagger.info.build)
- description and source-code
```javascript
build = function (options) {

    var out = (options.info) ? Hoek.applyToDefaults(info.defaults, options.info) : info.defaults;
    Joi.assert(out, info.schema);
    return out;
}
```
- example usage
```shell
...
if (settings.basePath !== '/') {
    settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
}
let out = internals.removeNoneSchemaOptions(settings);
Joi.assert(out, builder.schema);


out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);
...
```



# <a name="apidoc.module.hapi-swagger.parameters"></a>[module hapi-swagger.parameters](#apidoc.module.hapi-swagger.parameters)

#### <a name="apidoc.element.hapi-swagger.parameters.fromProperties"></a>[function <span class="apidocSignatureSpan">hapi-swagger.parameters.</span>fromProperties (schemaObj, parameterType)](#apidoc.element.hapi-swagger.parameters.fromProperties)
- description and source-code
```javascript
fromProperties = function (schemaObj, parameterType) {



    let out = [];
   // if (this.allowedParameterTypes.indexOf(parameterType) === -1) {
   //     return out;
   // }

    // if its a single parameter
    if (schemaObj.properties === undefined) {

        // console.log('a', JSON.stringify(schemaObj) + '\n');

        let item = Hoek.clone(schemaObj);
        item.in = parameterType;
        item.name = parameterType;
        item.schema = {};
        item.schema.type = item.type;
        delete item.type;

        // convert an object definition
        if (item.$ref) {
            item.schema.$ref = item.$ref;
            // item.schema.type = 'object'; // should have to do this but causes validations issues
            delete item.$ref;
        }

        // reinstate x-alternatives at parameter level
        if (schemaObj['x-alternatives']) {
            item['x-alternatives'] = schemaObj['x-alternatives'];
            delete item.schema['x-alternatives'];
        }

        item = Utilities.removeProps(item, this.allowedProps);
        if (!Hoek.deepEqual(item.schema, { 'type': 'object' }, { prototype: false })) {
            out.push(Utilities.deleteEmptyProperties(item));
        }

    // if its an array of parameters
    } else {

        //console.log('b', JSON.stringify(schemaObj) + '\n');

        // object to array
        const keys = Object.keys(schemaObj.properties);
        keys.forEach((element, index) => {

            let key = keys[index];
            let item = schemaObj.properties[key];
            item.name = key;
            item.in = parameterType;

            // reinstate required at parameter level
            if (schemaObj.required && schemaObj.required.indexOf(key) > -1) {
                item.required = true;
            }
            if (schemaObj.optional && schemaObj.optional.indexOf(key) > -1) {
                item.required = false;
            }

            item = Utilities.removeProps(item, this.allowedProps);
            out.push(item);
        });

    }
    return out;
}
```
- example usage
```shell
...

    let outProperties;
    let outParameters;

    if (joiObj) {
        // name, joiObj, parent, parameterType, useDefinitions, isAlt
        outProperties = this.properties.parseProperty(null, joiObj, null, parameterType, useDefinitions, isAlt);
        outParameters = Parameters.fromProperties(outProperties, parameterType);
    }
    let out = {
        properties: outProperties || {},
        parameters: outParameters || []
    };
    return out;
};
...
```



# <a name="apidoc.module.hapi-swagger.paths"></a>[module hapi-swagger.paths](#apidoc.module.hapi-swagger.paths)

#### <a name="apidoc.element.hapi-swagger.paths.paths"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>paths (settings)](#apidoc.element.hapi-swagger.paths.paths)
- description and source-code
```javascript
paths = function (settings) {

    this.settings = settings;
    this.definitions = new Definitions(settings);
    this.properties = new Properties(settings, {}, {});
    this.responses = new Responses(settings, {}, {});


    this.defaults = {
        responses: {}
    };

    this.schema = Joi.object({
        tags: Joi.array().items(Joi.string()),
        summary: Joi.string(),
        description: Joi.string(),
        externalDocs: Joi.object({
            description: Joi.string(),
            url: Joi.string().uri()
        }),
        operationId: Joi.string(),
        consumes: Joi.array().items(Joi.string()),
        produces: Joi.array().items(Joi.string()),
        parameters: Joi.array().items(Joi.object()),
        responses: Joi.object().required(),
        schemes: Joi.array().items(Joi.string().valid(['http', 'https', 'ws', 'wss'])),
        deprecated: Joi.boolean(),
        security: Joi.array().items(Joi.object())
    });
}
```
- example usage
```shell
...

out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);

// filter routes displayed based on tags passed in query string
if (request.query.tags) {
    let filterTags = request.query.tags.split(',');
    routes = Filter.byTags(filterTags, routes);
}
...
```



# <a name="apidoc.module.hapi-swagger.paths.prototype"></a>[module hapi-swagger.paths.prototype](#apidoc.module.hapi-swagger.paths.prototype)

#### <a name="apidoc.element.hapi-swagger.paths.prototype.build"></a>[function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>build (routes)](#apidoc.element.hapi-swagger.paths.prototype.build)
- description and source-code
```javascript
build = function (routes) {

    let self = this;


    let routesData = [];

    // loop each route
    routes.forEach((route) => {

        let routeOptions = Hoek.reach(route, 'settings.plugins.hapi-swagger') || {};
        let routeData = {
            path: route.path,
            method: route.method.toUpperCase(),
            description: route.settings.description,
            notes: route.settings.notes,
            tags: Hoek.reach(route, 'settings.tags'),
            queryParams: Hoek.reach(route, 'settings.validate.query'),
            pathParams: Hoek.reach(route, 'settings.validate.params'),
            payloadParams: Hoek.reach(route, 'settings.validate.payload'),
            responseSchema: Hoek.reach(route, 'settings.response.schema'),
            responseStatus: Hoek.reach(route, 'settings.response.status'),
            headerParams: Hoek.reach(route, 'settings.validate.headers'),
            consumes: Hoek.reach(routeOptions, 'consumes') || null,
            produces: Hoek.reach(routeOptions, 'produces') || null,
            responses: Hoek.reach(routeOptions, 'responses') || null,
            payloadType: Hoek.reach(routeOptions, 'payloadType') || null,
            security: Hoek.reach(routeOptions, 'security') || null,
            order: Hoek.reach(routeOptions, 'order') || null,
            deprecated: Hoek.reach(routeOptions, 'deprecated') || null,
            id: Hoek.reach(routeOptions, 'id') || null,
            groups: route.group
        };


        routeData.path = Utilities.replaceInPath(routeData.path, ['endpoints'], this.settings.pathReplacements);


        // user configured interface through route plugin options
        if (Hoek.reach(routeOptions, 'validate.query')) {
            routeData.queryParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.query'));
        }
        if (Hoek.reach(routeOptions, 'validate.params')) {
            routeData.pathParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.params'));
        }
        if (Hoek.reach(routeOptions, 'validate.headers')) {
            routeData.headerParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.headers'));
        }
        if (Hoek.reach(routeOptions, 'validate.payload')) {
            // has different structure, just pass straight through
            routeData.payloadParams = Hoek.reach(routeOptions, 'validate.payload');
            // if its a native javascript object convert it to JOI
            if (!routeData.payloadParams.isJoi) {
                routeData.payloadParams = Joi.object(routeData.payloadParams);
            }
        }

        // swap out any custom validation function for Joi object/string
        [
            'queryParams',
            'pathParams',
            'headerParams',
            'payloadParams'
        ].forEach(function (property) {

            // swap out any custom validation function for Joi object/string
            if (Utilities.isFunction(routeData[property])) {
                if (property !== 'pathParams') {
                    self.settings.log(['vaildation', 'warning'], 'Using a Joi.function for a query, header or payload is not supported
.');
                    if (property === 'payloadParams') {
                        routeData[property] = Joi.object().label('Hidden Model');
                    } else {
                        routeData[property] = Joi.object({ 'Hidden Model': Joi.string() });
                    }
                } else {
                    self.settings.log(['vaildation', 'error'], 'Using a Joi.function for a params is not supported and has been
removed.');
                    routeData[property] = null;
                }
            }
        });




        // hapi wildcard method support
        if (routeData.method === '*') {
            // OPTIONS not supported by Swagger and HEAD not support by HAPI
            ['GET', 'POST', 'PUT', 'PATCH', 'DELETE'].forEach((method) => {

                var newRoute = Hoek.clone(routeData);
                newRoute.method = method.toUpperCase();
                routesData.pus ...
```
- example usage
```shell
...
if (settings.basePath !== '/') {
    settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
}
let out = internals.removeNoneSchemaOptions(settings);
Joi.assert(out, builder.schema);


out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);
...
```

#### <a name="apidoc.element.hapi-swagger.paths.prototype.buildRoutes"></a>[function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>buildRoutes (routes)](#apidoc.element.hapi-swagger.paths.prototype.buildRoutes)
- description and source-code
```javascript
buildRoutes = function (routes) {

    let self = this;
    let pathObj = {};
    let swagger = {
        'definitions': {},
        'x-alt-definitions': {}
    };
    let definitionCache = [
        new WeakMap(),
        new WeakMap()
    ];

    // reset properties
    this.properties = new Properties(this.settings, swagger.definitions, swagger['x-alt-definitions'], definitionCache);
    this.responses = new Responses(this.settings, swagger.definitions, swagger['x-alt-definitions'], definitionCache);

    routes.forEach((route) => {

        let method = route.method;
        let path = internals.removeBasePath(route.path, this.settings.basePath, this.settings.pathReplacements);
        let out = {
            'summary': route.description,
            'operationId': route.id || Utilities.createId(route.method, path),
            'description': route.notes,
            'parameters': [],
            'consumes': [],
            'produces': []
        };

        // tags in swagger are used for grouping
        if (this.settings.grouping === 'tags') {
            out.tags = route.tags.slice(0);
            while (out.tags.indexOf('api') !== -1) {
                out.tags.splice(out.tags.indexOf('api'), 1);
            }
        }
        else {
            out.tags = route.groups;
        }

        out.description = Array.isArray(route.notes) ? route.notes.join('<br/><br/>') : route.notes;

        if (route.security) {
            out.security = route.security;
        }

        // set from plugin options or from route options
        let payloadType = internals.overload(this.settings.payloadType, route.payloadType);

        // build payload either with JSON or form input
        let payloadStructures = this.getDefaultStructures();
        let payloadJoi = internals.getJOIObj(route, 'payloadParams');
        if (payloadType.toLowerCase() === 'json') {
            // set as json
            payloadStructures = this.getSwaggerStructures(payloadJoi, 'body', true, false);
        } else {
            // set as formData
            if (Utilities.hasJoiChildren(payloadJoi)) {
                payloadStructures = this.getSwaggerStructures(payloadJoi, 'formData', false, false);
            } else {
                self.testParameterError(payloadJoi, 'payload form-urlencoded', path);
            }
            // add form data mimetype
            out.consumes = ['application/x-www-form-urlencoded'];
        }


        // change form mimetype based on meta property 'swaggerType'
        if (internals.hasFileType(route)) {
            out.consumes = ['multipart/form-data'];
        }

        // add user defined over automaticlly discovered
        if (this.settings.consumes || route.consumes) {
            out.consumes = internals.overload(this.settings.consumes, route.consumes);
        }

        if (this.settings.produces || route.produces) {
            out.produces = internals.overload(this.settings.produces, route.produces);
        }


        // set required true/false for each path params
        //var pathParams = this.properties.toParameters (internals.getJOIObj(route, 'pathParams'), 'path', false);
        let pathStructures = this.getDefaultStructures();
        let pathJoi = internals.getJOIObj(route, 'pathParams');
        if (Utilities.hasJoiChildren(pathJoi)) {
            pathStructures = this.getSwaggerStructures(pathJoi, 'path', false, false);
            pathStructures.parameters.forEach(function (item) {

                // add required based on path pattern {prama} and {prama?}
                if (item.required === undefined) {
                    if (path.indexOf('{' + item.name + '}') > -1) {
                        item.required = true;
                    }
                    if (path.indexOf('{' + item.name + '?}') > -1) {
                        delete item.required;
                    }
                }
                if (item.required === false) {
                    delete item.required;
                }
                if (!item.required) {
                    self.settings.log(['validation', 'warning'], ...
```
- example usage
```shell
...
           });
       } else {
           routesData.push(routeData);
       }
   });


   return this.buildRoutes(routesData);
};


/**
* build the swagger path section from hapi routes data
*
* @param  {Object} setting
...
```

#### <a name="apidoc.element.hapi-swagger.paths.prototype.getDefaultStructures"></a>[function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>getDefaultStructures ()](#apidoc.element.hapi-swagger.paths.prototype.getDefaultStructures)
- description and source-code
```javascript
getDefaultStructures = function () {

    return {
        'properties': {},
        'parameters': []
    };
}
```
- example usage
```shell
...
    out.security = route.security;
}

// set from plugin options or from route options
let payloadType = internals.overload(this.settings.payloadType, route.payloadType);

// build payload either with JSON or form input
let payloadStructures = this.getDefaultStructures();
let payloadJoi = internals.getJOIObj(route, 'payloadParams');
if (payloadType.toLowerCase() === 'json') {
    // set as json
    payloadStructures = this.getSwaggerStructures(payloadJoi, 'body', true, false);
} else {
    // set as formData
    if (Utilities.hasJoiChildren(payloadJoi)) {
...
```

#### <a name="apidoc.element.hapi-swagger.paths.prototype.getSwaggerStructures"></a>[function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>getSwaggerStructures (joiObj, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.paths.prototype.getSwaggerStructures)
- description and source-code
```javascript
getSwaggerStructures = function (joiObj, parameterType, useDefinitions, isAlt) {

    let outProperties;
    let outParameters;

    if (joiObj) {
        // name, joiObj, parent, parameterType, useDefinitions, isAlt
        outProperties = this.properties.parseProperty(null, joiObj, null, parameterType, useDefinitions, isAlt);
        outParameters = Parameters.fromProperties(outProperties, parameterType);
    }
    let out = {
        properties: outProperties || {},
        parameters: outParameters || []
    };
    return out;
}
```
- example usage
```shell
...
let payloadType = internals.overload(this.settings.payloadType, route.payloadType);

// build payload either with JSON or form input
let payloadStructures = this.getDefaultStructures();
let payloadJoi = internals.getJOIObj(route, 'payloadParams');
if (payloadType.toLowerCase() === 'json') {
    // set as json
    payloadStructures = this.getSwaggerStructures(payloadJoi, 'body', true, false);
} else {
    // set as formData
    if (Utilities.hasJoiChildren(payloadJoi)) {
        payloadStructures = this.getSwaggerStructures(payloadJoi, 'formData', false, false);
    } else {
        self.testParameterError(payloadJoi, 'payload form-urlencoded', path);
    }
...
```

#### <a name="apidoc.element.hapi-swagger.paths.prototype.testParameterError"></a>[function <span class="apidocSignatureSpan">hapi-swagger.paths.prototype.</span>testParameterError (joiObj, parameterType, path)](#apidoc.element.hapi-swagger.paths.prototype.testParameterError)
- description and source-code
```javascript
testParameterError = function (joiObj, parameterType, path) {

    if (joiObj && !Utilities.hasJoiChildren(joiObj)) {
        this.settings.log(['validation', 'error'], 'The ' + path  + ' route ' + parameterType + ' parameter was set, but not as
a Joi.object() with child properties');
    }
}
```
- example usage
```shell
...
    // set as json
    payloadStructures = this.getSwaggerStructures(payloadJoi, 'body', true, false);
} else {
    // set as formData
    if (Utilities.hasJoiChildren(payloadJoi)) {
        payloadStructures = this.getSwaggerStructures(payloadJoi, 'formData', false, false);
    } else {
        self.testParameterError(payloadJoi, 'payload form-urlencoded', path);
    }
    // add form data mimetype
    out.consumes = ['application/x-www-form-urlencoded'];
}


// change form mimetype based on meta property 'swaggerType'
...
```



# <a name="apidoc.module.hapi-swagger.properties"></a>[module hapi-swagger.properties](#apidoc.module.hapi-swagger.properties)

#### <a name="apidoc.element.hapi-swagger.properties.properties"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>properties (settings, definitionCollection, altDefinitionCollection, definitionCache )](#apidoc.element.hapi-swagger.properties.properties)
- description and source-code
```javascript
properties = function (settings, definitionCollection, altDefinitionCollection, definitionCache ) {

    this.settings = settings;
    this.definitionCollection = definitionCollection;
    this.altDefinitionCollection = altDefinitionCollection;
    // definitionCache has to be an array of two WeakMaps
    this.definitionCache = definitionCache;

    this.definitions = new Definitions(settings);


    // swagger type can be 'string', 'number', 'integer', 'boolean', 'array' or 'file'
    this.simpleTypePropertyMap = {
        'boolean': { 'type': 'boolean' },
        'binary': { 'type': 'string', 'format': 'binary' },
        'date': { 'type': 'string', 'format': 'date' },
        'number': { 'type': 'number' },
        'string': { 'type': 'string' }
    };

    this.complexTypePropertyMap = {
        'any': { 'type': 'string' },
        'array': { 'type': 'array' },
        'func': { 'type': 'string' },
        'object': { 'type': 'object' },
        'alternatives': { 'type': 'alternatives' }
    };

    // merge
    this.propertyMap = Hoek.applyToDefaults(this.simpleTypePropertyMap, this.complexTypePropertyMap);

    //this.allowedProps = ['$ref','format','title','description','default','multipleOf','maximum','exclusiveMaximum','minimum','
exclusiveMinimum','maxLength','minLength','pattern','maxItems','minItems','uniqueItems','maxProperties','minProperties','required
','enum','type','items','allOf','properties','additionalProperties','discriminator','readOnly','xml','externalDocs','example'];
    // add none swagger property needed to flag touched state of required property
    //this.allowedProps.push('optional');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.hapi-swagger.properties.prototype"></a>[module hapi-swagger.properties.prototype](#apidoc.module.hapi-swagger.properties.prototype)

#### <a name="apidoc.element.hapi-swagger.properties.prototype.getDefinitionCollection"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>getDefinitionCollection (isAlt)](#apidoc.element.hapi-swagger.properties.prototype.getDefinitionCollection)
- description and source-code
```javascript
getDefinitionCollection = function (isAlt) {

    return (isAlt === true) ? this.altDefinitionCollection : this.definitionCollection;
}
```
- example usage
```shell
...

    // add object child properties
    if (property.type === 'object') {
if (Utilities.hasJoiChildren(joiObj)) {

    property = this.parseObject(property, joiObj, name, parameterType, useDefinitions, isAlt);
    if (useDefinitions === true) {
        let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
        property = {
            '$ref': this.getDefinitionRef(isAlt) + refName,
            'type': 'object'
        };
    }

} else {
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.getDefinitionRef"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>getDefinitionRef (isAlt)](#apidoc.element.hapi-swagger.properties.prototype.getDefinitionRef)
- description and source-code
```javascript
getDefinitionRef = function (isAlt) {

    return (isAlt === true) ? '#/x-alt-definitions/' : '#/definitions/';
}
```
- example usage
```shell
...
    if (property.type === 'object') {
if (Utilities.hasJoiChildren(joiObj)) {

    property = this.parseObject(property, joiObj, name, parameterType, useDefinitions, isAlt);
    if (useDefinitions === true) {
        let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
        property = {
            '$ref': this.getDefinitionRef(isAlt) + refName,
            'type': 'object'
        };
    }

} else {
    // default empty object
    property.properties = {};
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseAlternatives"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseAlternatives (property, joiObj, name, parameterType, useDefinitions)](#apidoc.element.hapi-swagger.properties.prototype.parseAlternatives)
- description and source-code
```javascript
parseAlternatives = function (property, joiObj, name, parameterType, useDefinitions) {

    // convert .try() alternatives structures
    if (Hoek.reach(joiObj, '_inner.matches.0.schema')) {
        // add first into definitionCollection
        let child = joiObj._inner.matches[0].schema;
        let childName = Utilities.geJoiLabel(joiObj);
        //name, joiObj, parent, parameterType, useDefinitions, isAlt
        property = this.parseProperty(childName, child, property, parameterType, useDefinitions, false);

        // create the alternatives without appending to the definitionCollection
        if (this.settings.xProperties === true) {
            let altArray = joiObj._inner.matches.map((obj) => {
                let altName = (Utilities.geJoiLabel(obj.schema) || name);
                //name, joiObj, parent, parameterType, useDefinitions, isAlt
                return this.parseProperty(altName, obj.schema, property, parameterType, useDefinitions, true);
            });
            property['x-alternatives'] = Hoek.clone(altArray);
        }
    }

    // convert .when() alternatives structures
    else {
        // add first into definitionCollection
        let child = joiObj._inner.matches[0].then;
        let childName = (Utilities.geJoiLabel(child) || name);
        //name, joiObj, parent, parameterType, useDefinitions, isAlt
        property = this.parseProperty(childName, child, property, parameterType, useDefinitions, false);

        // create the alternatives without appending to the definitionCollection
        if (this.settings.xProperties === true) {
            let altArray = joiObj._inner.matches
                .reduce((res, obj) => {
                    obj.then && res.push(obj.then);
                    obj.otherwise && res.push(obj.otherwise);
                    return res;
                }, [])
                .map((joiNewObj) => {
                    let altName = (Utilities.geJoiLabel(joiNewObj) || name);
                    return this.parseProperty(altName, joiNewObj, property, parameterType, useDefinitions, true);
                })
                .filter((obj) => obj);
            property['x-alternatives'] = Hoek.clone(altArray);
        }
    }

    //if (!property.$ref && Utilities.geJoiLabel(joiObj)) {
    //    property.name = Utilities.geJoiLabel(joiObj);
    //}

    return property;
}
```
- example usage
```shell
...
        };
    }
}


// add alternatives properties
if (property.type === 'alternatives') {
    property = this.parseAlternatives(property, joiObj, name, parameterType, useDefinitions);
}

// convert property to file upload, if indicated by meta property
if (Utilities.getJoiMetaProperty(joiObj, 'swaggerType') === 'file') {
    property.type = 'file';
    property.in = 'formData';
}
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseArray"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseArray (property, joiObj, name, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseArray)
- description and source-code
```javascript
parseArray = function (property, joiObj, name, parameterType, useDefinitions, isAlt) {

    const describe = joiObj.describe();
    property.minItems = internals.getArgByName(describe.rules, 'min');
    property.maxItems = internals.getArgByName(describe.rules, 'max');


    // add extended properties not part of openAPI spec
    if (this.settings.xProperties === true) {
        internals.convertRules(property, describe.rules, [
            'length',
            'unique'
        ], 'x-constraint');

        if (describe.flags.sparse) {
            internals.addToPropertyObject(property, 'x-constraint', 'sparse', true);
        }
        if (describe.flags.single) {
            internals.addToPropertyObject(property, 'x-constraint', 'single', true);
        }
    }


    // default the items with type:string
    property.items = {
        'type': 'string'
    };

    // set swaggers collectionFormat to one that works with hapi
    if (parameterType === 'query' || parameterType === 'formData') {
        property.collectionFormat = 'multi';
    }

    // swagger appears to only support one array item type at a time, so grab the first one
    let arrayItemTypes = joiObj._inner.items; // joiObj._inner.inclusions;
    let arrayItem = Utilities.first(arrayItemTypes);

    if (arrayItem) {
        // get name of item if it has one
        let itemName;
        if (Utilities.geJoiLabel(arrayItem)) {
            itemName = Utilities.geJoiLabel(arrayItem);
        }

        //name, joiObj, parent, parameterType, useDefinitions, isAlt
        let arrayItemProperty = this.parseProperty(itemName, arrayItem, property, parameterType, useDefinitions, isAlt);
        if (this.simpleTypePropertyMap[arrayItem._type.toLowerCase()]) {
            // map simple types directly
            property.items = {};
            for (let key in arrayItemProperty) {
                property.items[key] = arrayItemProperty[key];
            }
        } else {
            property.items = arrayItemProperty;
        }

    }

    property.name = name;
    return property;
}
```
- example usage
```shell
...

}
    }


    // add array properties
    if (property.type === 'array') {
property = this.parseArray(property, joiObj, name, parameterType, useDefinitions, isAlt);

if (useDefinitions === true) {
    let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
    property = {
        '$ref': this.getDefinitionRef(isAlt) + refName,
        'type': 'array'
    };
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseDate"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseDate (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseDate)
- description and source-code
```javascript
parseDate = function (property, joiObj) {

    if (joiObj._flags.timestamp) {
        property.type = 'number';
        delete property.format;
    }

    return property;
}
```
- example usage
```shell
...
    // add number properties
    if (property.type === 'number') {
        property = this.parseNumber(property, joiObj);
    }

    // add date properties
    if (property.type === 'string' && property.format === 'date') {
        property = this.parseDate(property, joiObj);
    }

    // add object child properties
    if (property.type === 'object') {
        if (Utilities.hasJoiChildren(joiObj)) {

property = this.parseObject(property, joiObj, name, parameterType, useDefinitions, isAlt);
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseNumber"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseNumber (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseNumber)
- description and source-code
```javascript
parseNumber = function (property, joiObj) {

    const describe = joiObj.describe();
    property.minimum = internals.getArgByName(describe.rules, 'min');
    property.maximum = internals.getArgByName(describe.rules, 'max');
    if (internals.hasPropertyByName(describe.rules, 'integer')) {
        property.type = 'integer';
    }

    // add extended properties not part of openAPI spec
    if (this.settings.xProperties === true) {
        internals.convertRules(property, describe.rules, [
            'greater',
            'less',
            'precision',
            'multiple',
            'positive',
            'negative'
        ], 'x-constraint');
    }

    return property;
}
```
- example usage
```shell
...
// add number properties
if (property.type === 'string') {
    property = this.parseString(property, joiObj);
}

// add number properties
if (property.type === 'number') {
    property = this.parseNumber(property, joiObj);
}

// add date properties
if (property.type === 'string' && property.format === 'date') {
    property = this.parseDate(property, joiObj);
}
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseObject"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseObject (property, joiObj, name, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseObject)
- description and source-code
```javascript
parseObject = function (property, joiObj, name, parameterType, useDefinitions, isAlt) {

    property.properties = {};
    joiObj = joiObj._inner.children;
    joiObj.forEach((obj) => {

        let keyName = obj.key;
        let itemName = obj.key;
        let joiChildObj = obj.schema;
        // get name form label if set
        if (Utilities.geJoiLabel(joiChildObj)) {
            itemName = Utilities.geJoiLabel(joiChildObj);
        }
        //name, joiObj, parent, parameterType, useDefinitions, isAlt
        property.properties[keyName] = this.parseProperty(itemName, joiChildObj, property, parameterType, useDefinitions, isAlt);
        // switch references if naming has changed
        if (keyName !== itemName) {
            property.required = Utilities.replaceValue(property.required, itemName, keyName);
            property.optional = Utilities.replaceValue(property.optional, itemName, keyName);
        }
    });
    property.name = name;
    return property;
}
```
- example usage
```shell
...
        property = this.parseDate(property, joiObj);
    }

    // add object child properties
    if (property.type === 'object') {
        if (Utilities.hasJoiChildren(joiObj)) {

property = this.parseObject(property, joiObj, name, parameterType, useDefinitions, isAlt);
if (useDefinitions === true) {
    let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
    property = {
        '$ref': this.getDefinitionRef(isAlt) + refName,
        'type': 'object'
    };
}
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseProperty"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseProperty (name, joiObj, parent, parameterType, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.properties.prototype.parseProperty)
- description and source-code
```javascript
parseProperty = function (name, joiObj, parent, parameterType, useDefinitions, isAlt) {

    let property = { type: 'void' };

    // if wrong format or forbidden - return undefined
    if (!Utilities.isJoi(joiObj)) {
        return undefined;
    }
    if (Hoek.reach(joiObj, '_flags.presence') === 'forbidden') {
        return undefined;
    }

    // default the use of definitions to true
    if (useDefinitions === undefined || useDefinitions === null) {
        useDefinitions = true;
    }

    // get name from joi label if its not a path
    if (!name && Utilities.geJoiLabel(joiObj) && parameterType !== 'path') {
        name = Utilities.geJoiLabel(joiObj);
    }

    // add correct type and format by mapping
    let joiType = joiObj._type.toLowerCase();
    // for Joi extension, use the any type
    if (!(joiType in this.propertyMap)){
        joiType = 'any';
    }
    let map = this.propertyMap[joiType];
    property.type = map.type;
    if (map.format) {
        property.format = map.format;
    }

    // Joi object caching - speeds up parsing
    let joiCache;
    if (useDefinitions && Array.isArray(this.definitionCache) && property.type === 'object') {
        // select WeakMap for current definition collection
        joiCache = (isAlt === true) ? this.definitionCache[1] : this.definitionCache[0];
        if (joiCache.has(joiObj)) {
            return joiCache.get(joiObj);
        }
    }


    property = this.parsePropertyMetadata(property, name, parent, joiObj);

    // add enum
    let describe = joiObj.describe();
    if (Array.isArray(describe.valids) && describe.valids.length) {
        // fliter out empty values and arrays
        var enums = describe.valids.filter((item) => {

            return item !== '' && item !== null;
        });
        if (enums.length > 0) {
            property.enum = enums;
        }
    }

    // add number properties
    if (property.type === 'string') {
        property = this.parseString(property, joiObj);
    }

    // add number properties
    if (property.type === 'number') {
        property = this.parseNumber(property, joiObj);
    }

    // add date properties
    if (property.type === 'string' && property.format === 'date') {
        property = this.parseDate(property, joiObj);
    }

    // add object child properties
    if (property.type === 'object') {
        if (Utilities.hasJoiChildren(joiObj)) {

            property = this.parseObject(property, joiObj, name, parameterType, useDefinitions, isAlt);
            if (useDefinitions === true) {
                let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
                property = {
                    '$ref': this.getDefinitionRef(isAlt) + refName,
                    'type': 'object'
                };
            }

        } else {
            // default empty object
            property.properties = {};
            if (useDefinitions === true) {
                let objectSchema = { 'type': 'object', 'properties': {} };
                let refName = this.definitions.append(name, objectSchema, this.getDefinitionCollection(isAlt), this.settings);
                property = {
                    '$ref': this.getDefinitionRef(isAlt) + refName,
                    'type': 'object'
                };
            }

        }
    }


    // add array properties
    if (property.type === 'array') {
        property = this.parseArray(property, joiObj, name, parameterType, useDefinitions, isAlt);

        if (useDefinitions === true) {
            let refName = this.definitions.append(name, property, this.getDefinitionCollection(isAlt), this.settings);
            property = {
                '$ref': this.getDefinitionRef(isAlt) + refName,
                'type': 'array'
            };
        }
    }


    // add alternatives properties
    if (property.type === 'alternatives') {
        property = this.parseAlternatives(property, joiObj, name, parameterType, useDefinitions);
    }

    // convert property to file upload, if indicated by meta property
    if (Utilities. ...
```
- example usage
```shell
...
internals.paths.prototype.getSwaggerStructures = function (joiObj, parameterType, useDefinitions, isAlt) {

let outProperties;
let outParameters;

if (joiObj) {
    // name, joiObj, parent, parameterType, useDefinitions, isAlt
    outProperties = this.properties.parseProperty(null, joiObj, null, parameterType, useDefinitions, isAlt);
    outParameters = Parameters.fromProperties(outProperties, parameterType);
}
let out = {
    properties: outProperties || {},
    parameters: outParameters || []
};
return out;
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parsePropertyMetadata"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parsePropertyMetadata (property, name, parent, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parsePropertyMetadata)
- description and source-code
```javascript
parsePropertyMetadata = function (property, name, parent, joiObj) {

    const describe = joiObj.describe();

    // add common properties
    property.description = Hoek.reach(joiObj, '_description');
    property.notes = Hoek.reach(joiObj, '_notes');
    property.tags = Hoek.reach(joiObj, '_tags');

    // add extended properties not part of openAPI spec
    if (this.settings.xProperties === true) {
        internals.convertRules(property, describe.rules, [
            'unit'
        ], 'x-format');
        property.example = Hoek.reach(joiObj, '_examples.0');
        property['x-meta'] = Hoek.reach(joiObj, '_meta.0');
    }

    // add required/optional state only if present
    if (parent && name) {
        if (Hoek.reach(joiObj, '_flags.presence')) {
            if (parent.required === undefined) {
                parent.required = [];
            }
            if (parent.optional === undefined) {
                parent.optional = [];
            }
            if (Hoek.reach(joiObj, '_flags.presence') === 'required') {
                parent.required.push(name);
            }
            if (Hoek.reach(joiObj, '_flags.presence') === 'optional') {
                parent.optional.push(name);
            }
        }
    }

    property.default = Hoek.reach(joiObj, '_flags.default');

    // allow for function calls
    if (Utilities.isFunction(property.default)) {
        property.default = property.default();
    }

    return property;
}
```
- example usage
```shell
...
    joiCache = (isAlt === true) ? this.definitionCache[1] : this.definitionCache[0];
    if (joiCache.has(joiObj)) {
        return joiCache.get(joiObj);
    }
}


property = this.parsePropertyMetadata(property, name, parent, joiObj);

// add enum
let describe = joiObj.describe();
if (Array.isArray(describe.valids) && describe.valids.length) {
    // fliter out empty values and arrays
    var enums = describe.valids.filter((item) => {
...
```

#### <a name="apidoc.element.hapi-swagger.properties.prototype.parseString"></a>[function <span class="apidocSignatureSpan">hapi-swagger.properties.prototype.</span>parseString (property, joiObj)](#apidoc.element.hapi-swagger.properties.prototype.parseString)
- description and source-code
```javascript
parseString = function (property, joiObj) {

    const describe = joiObj.describe();

    property.minLength = internals.getArgByName(describe.rules, 'min');
    property.maxLength = internals.getArgByName(describe.rules, 'max');

    // add regex
    joiObj._tests.forEach((test) => {
        // Joi post v10
        if (Utilities.isObject(test.arg) && test.arg.pattern) {
            property.pattern = test.arg.pattern.toString();
        }
        // Joi pre v10
<span class="apidocCodeCommentSpan">        /* $lab:coverage:off$ */
</span>        if (Utilities.isRegex(test.arg)) {
            property.pattern = test.arg.toString();
        }
        /* $lab:coverage:on$ */
    });


    // add extended properties not part of openAPI spec
    if (this.settings.xProperties === true) {
        internals.convertRules(property, describe.rules, [
            'insensitive',
            'length'
        ], 'x-constraint');

        internals.convertRules(property, describe.rules, [
            'creditCard',
            'alphanum',
            'token',
            'email',
            'ip',
            'uri',
            'guid',
            'hex',
            'hostname',
            'isoDate'
        ], 'x-format');

        internals.convertRules(property, describe.rules, [
            'lowercase',
            'uppercase',
            'trim'
        ], 'x-convert');
    }

    return property;
}
```
- example usage
```shell
...
    if (enums.length > 0) {
        property.enum = enums;
    }
}

// add number properties
if (property.type === 'string') {
    property = this.parseString(property, joiObj);
}

// add number properties
if (property.type === 'number') {
    property = this.parseNumber(property, joiObj);
}
...
```



# <a name="apidoc.module.hapi-swagger.responses"></a>[module hapi-swagger.responses](#apidoc.module.hapi-swagger.responses)

#### <a name="apidoc.element.hapi-swagger.responses.responses"></a>[function <span class="apidocSignatureSpan">hapi-swagger.</span>responses (settings, definitionCollection, altDefinitionCollection, definitionCache)](#apidoc.element.hapi-swagger.responses.responses)
- description and source-code
```javascript
responses = function (settings, definitionCollection, altDefinitionCollection, definitionCache) {

    this.settings = settings;
    this.definitionCollection = definitionCollection;
    this.altDefinitionCollection = altDefinitionCollection;

    this.definitions = new Definitions(settings);
    this.properties = new Properties(settings, this.definitionCollection, this.altDefinitionCollection, definitionCache);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.hapi-swagger.responses.prototype"></a>[module hapi-swagger.responses.prototype](#apidoc.module.hapi-swagger.responses.prototype)

#### <a name="apidoc.element.hapi-swagger.responses.prototype.build"></a>[function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>build (userDefindedSchemas, defaultSchema, statusSchemas, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.responses.prototype.build)
- description and source-code
```javascript
build = function (userDefindedSchemas, defaultSchema, statusSchemas, useDefinitions, isAlt) {

    let out = {};


    // add defaultSchema to statusSchemas if needed
    if (Utilities.hasProperties(defaultSchema) && (Hoek.reach(statusSchemas, '200') === undefined)) {
        statusSchemas[200] = defaultSchema;
    }

    // loop for each status and convert schema into a definition
    if (Utilities.hasProperties(statusSchemas)) {
        for (let key in statusSchemas) {
            // name, joiObj, parameterType, useDefinitions, isAlt
            let response = this.getResponse(key, statusSchemas[key], null, useDefinitions, isAlt);
            out[key] = response;
        }
    }

    // use plug-in options overrides to enchance hapi objects and properties
    if (Utilities.hasProperties(userDefindedSchemas) === true) {
        out = this.optionOverride(out, userDefindedSchemas, useDefinitions, isAlt);
    }

    // make sure 200 status always has a schema #237
    if (out[200] && out[200].schema === undefined) {
        out[200].schema = {
            'type': 'string'
        };
    }

    // make sure there is a default if no other responses are found
    if (Utilities.hasProperties(out) === false) {
        out.default = {
            'schema': {
                'type': 'string'
            },
            'description': 'Successful'
        };
    }

    return Utilities.deleteEmptyProperties(out);
}
```
- example usage
```shell
...
if (settings.basePath !== '/') {
    settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
}
let out = internals.removeNoneSchemaOptions(settings);
Joi.assert(out, builder.schema);


out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);
...
```

#### <a name="apidoc.element.hapi-swagger.responses.prototype.getResponse"></a>[function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>getResponse (statusCode, joiObj, useDefinitions)](#apidoc.element.hapi-swagger.responses.prototype.getResponse)
- description and source-code
```javascript
getResponse = function (statusCode, joiObj, useDefinitions) {

    let out;
    //name, joiObj, parent, parameterType, useDefinitions, isAlt
    let outProperties = this.properties.parseProperty(null, joiObj, null, 'body', useDefinitions, false);
    out = {
        'description': Hoek.reach(joiObj, '_description'),
        'schema': outProperties
    };

    out.headers = Utilities.getJoiMetaProperty(joiObj, 'headers');
    out.examples = Utilities.getJoiMetaProperty(joiObj, 'examples');
    delete out.schema['x-meta'];
    out = Utilities.deleteEmptyProperties(out);

    // default description if not given
    if (!out.description) {
        out.description = HTTPStatus[statusCode].replace('OK', 'Successful');
    }

    return out;
}
```
- example usage
```shell
...
    statusSchemas[200] = defaultSchema;
}

// loop for each status and convert schema into a definition
if (Utilities.hasProperties(statusSchemas)) {
    for (let key in statusSchemas) {
        // name, joiObj, parameterType, useDefinitions, isAlt
        let response = this.getResponse(key, statusSchemas[key], null, useDefinitions, isAlt);
        out[key] = response;
    }
}

// use plug-in options overrides to enchance hapi objects and properties
if (Utilities.hasProperties(userDefindedSchemas) === true) {
    out = this.optionOverride(out, userDefindedSchemas, useDefinitions, isAlt);
...
```

#### <a name="apidoc.element.hapi-swagger.responses.prototype.optionOverride"></a>[function <span class="apidocSignatureSpan">hapi-swagger.responses.prototype.</span>optionOverride (discoveredSchemas, userDefindedSchemas, useDefinitions, isAlt)](#apidoc.element.hapi-swagger.responses.prototype.optionOverride)
- description and source-code
```javascript
optionOverride = function (discoveredSchemas, userDefindedSchemas, useDefinitions, isAlt) {

    for (let key in userDefindedSchemas) {

        // create a new object by cloning - dont modify user definded objects
        let out = Hoek.clone(userDefindedSchemas[key]);

        // test for any JOI objects
        if (Hoek.reach(userDefindedSchemas[key], 'schema.isJoi') && userDefindedSchemas[key].schema.isJoi === true) {
            out = this.getResponse(key, userDefindedSchemas[key].schema, useDefinitions, isAlt);
            out.description = userDefindedSchemas[key].description;
        }


        // overwrite discovery with user definded
        if (!discoveredSchemas[key] && out) {
            // if it does not exist create it
            discoveredSchemas[key] = out;
        } else {
            // add description to schema
            if (out.description) {
                discoveredSchemas[key].description = out.description;
            }
            // overwrite schema
            if (out.schema) {
                discoveredSchemas[key].schema = out.schema;
            }
        }
        discoveredSchemas[key] = Utilities.deleteEmptyProperties(discoveredSchemas[key]);

    }
    return discoveredSchemas;
}
```
- example usage
```shell
...
        let response = this.getResponse(key, statusSchemas[key], null, useDefinitions, isAlt);
        out[key] = response;
    }
}

// use plug-in options overrides to enchance hapi objects and properties
if (Utilities.hasProperties(userDefindedSchemas) === true) {
    out = this.optionOverride(out, userDefindedSchemas, useDefinitions, isAlt);
}

// make sure 200 status always has a schema #237
if (out[200] && out[200].schema === undefined) {
    out[200].schema = {
        'type': 'string'
    };
...
```



# <a name="apidoc.module.hapi-swagger.sort"></a>[module hapi-swagger.sort](#apidoc.module.hapi-swagger.sort)

#### <a name="apidoc.element.hapi-swagger.sort.paths"></a>[function <span class="apidocSignatureSpan">hapi-swagger.sort.</span>paths (sortType, routes)](#apidoc.element.hapi-swagger.sort.paths)
- description and source-code
```javascript
paths = function (sortType, routes) {


    if (sortType === 'path-method') {
        //console.log('path-method')
        routes.sort(
            Utilities.firstBy('path').thenBy('method')
        );
    }

    return routes;
}
```
- example usage
```shell
...

out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);

// filter routes displayed based on tags passed in query string
if (request.query.tags) {
    let filterTags = request.query.tags.split(',');
    routes = Filter.byTags(filterTags, routes);
}
...
```



# <a name="apidoc.module.hapi-swagger.tags"></a>[module hapi-swagger.tags](#apidoc.module.hapi-swagger.tags)

#### <a name="apidoc.element.hapi-swagger.tags.build"></a>[function <span class="apidocSignatureSpan">hapi-swagger.tags.</span>build (settings)](#apidoc.element.hapi-swagger.tags.build)
- description and source-code
```javascript
build = function (settings) {

    let out = [];

    if (settings.tags) {
        Joi.assert(settings.tags, tags.schema);
        out = settings.tags;
    }
    return out;
}
```
- example usage
```shell
...
if (settings.basePath !== '/') {
    settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
}
let out = internals.removeNoneSchemaOptions(settings);
Joi.assert(out, builder.schema);


out.info = Info.build(settings);
out.tags = Tags.build(settings);

let routes = connection.table();

routes = Filter.byTags(['api'], routes);
Sort.paths(settings.sortPaths, routes);
...
```



# <a name="apidoc.module.hapi-swagger.utilities"></a>[module hapi-swagger.utilities](#apidoc.module.hapi-swagger.utilities)

#### <a name="apidoc.element.hapi-swagger.utilities.createId"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>createId (method, path)](#apidoc.element.hapi-swagger.utilities.createId)
- description and source-code
```javascript
createId = function (method, path) {

    const self = this;
    if (path.indexOf('/') > -1) {
        let items = path.split('/');
        items = items.map(function (item) {
            // replace chars such as '{'
            item = item.replace(/[^\w\s]/gi, '');
            return self.toTitleCase(item);
        });
        path = items.join('');
    } else {
        path = self.toTitleCase(path);
    }
    return method.toLowerCase() + path;
}
```
- example usage
```shell
...

    routes.forEach((route) => {

let method = route.method;
let path = internals.removeBasePath(route.path, this.settings.basePath, this.settings.pathReplacements);
let out = {
    'summary': route.description,
    'operationId': route.id || Utilities.createId(route.method, path),
    'description': route.notes,
    'parameters': [],
    'consumes': [],
    'produces': []
};

// tags in swagger are used for grouping
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.deleteEmptyProperties"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>deleteEmptyProperties (obj)](#apidoc.element.hapi-swagger.utilities.deleteEmptyProperties)
- description and source-code
```javascript
deleteEmptyProperties = function (obj) {

    let key;
    for (key in obj) {
        if (obj.hasOwnProperty(key)) {
            // delete properties undefined values
            if (obj[key] === undefined || obj[key] === null) {
                delete obj[key];
            }
            // allow blank objects for example or default properties
            if (['default', 'example'].indexOf(key) === -1) {
                // delete array with no values
                if (Array.isArray(obj[key]) && obj[key].length === 0) {
                    delete obj[key];
                }
                // delete object which does not have its own properties
                if (utilities.isObject(obj[key]) && utilities.hasProperties(obj[key]) === false) {
                    delete obj[key];
                }
            }
        }
    }
    return obj;
}
```
- example usage
```shell
...
    // add $ref directly to parent and delete schema
//    if (obj.schema) {
//        obj.$ref = obj.schema.$ref;
//        delete obj.schema;
//    }

    // remove emtpy properties
    obj = Utilities.deleteEmptyProperties(obj);

    // remove unneeded properties
    delete obj.name;

    return obj;
};
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.findAndRenameKey"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>findAndRenameKey (obj, findKey, replaceKey)](#apidoc.element.hapi-swagger.utilities.findAndRenameKey)
- description and source-code
```javascript
findAndRenameKey = function (obj, findKey, replaceKey) {

    for (var key in obj) {
        if (obj.hasOwnProperty(key)) {
            if (typeof obj[key] === 'object') {
                this.findAndRenameKey(obj[key], findKey, replaceKey);
            }
            if (key === findKey) {
                if (replaceKey) {
                    obj[replaceKey] = obj[findKey];
                }
                delete obj[findKey];
            }
        }
    }
    return obj;
}
```
- example usage
```shell
...
 * @return {Object}
 */
utilities.findAndRenameKey = function (obj, findKey, replaceKey) {

for (var key in obj) {
    if (obj.hasOwnProperty(key)) {
        if (typeof obj[key] === 'object') {
            this.findAndRenameKey(obj[key], findKey, replaceKey);
        }
        if (key === findKey) {
            if (replaceKey) {
                obj[replaceKey] = obj[findKey];
            }
            delete obj[findKey];
        }
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.first"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>first (array)](#apidoc.element.hapi-swagger.utilities.first)
- description and source-code
```javascript
first = function (array) {

    return Array.isArray(array) ? array[0] : undefined;
}
```
- example usage
```shell
...
// set swaggers collectionFormat to one that works with hapi
if (parameterType === 'query' || parameterType === 'formData') {
    property.collectionFormat = 'multi';
}

// swagger appears to only support one array item type at a time, so grab the first one
let arrayItemTypes = joiObj._inner.items; // joiObj._inner.inclusions;
let arrayItem = Utilities.first(arrayItemTypes);

if (arrayItem) {
    // get name of item if it has one
    let itemName;
    if (Utilities.geJoiLabel(arrayItem)) {
        itemName = Utilities.geJoiLabel(arrayItem);
    }
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.firstBy"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>firstBy (f, d)](#apidoc.element.hapi-swagger.utilities.firstBy)
- description and source-code
```javascript
firstBy = function (f, d) {

    f = makeCompareFunction(f, d);
    f.thenBy = tb;
    return f;
}
```
- example usage
```shell
...
 */
sort.paths = function (sortType, routes) {


    if (sortType === 'path-method') {
        //console.log('path-method')
        routes.sort(
            Utilities.firstBy('path').thenBy('method')
        );
    }

    return routes;
};
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.geJoiLabel"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>geJoiLabel (joiObj)](#apidoc.element.hapi-swagger.utilities.geJoiLabel)
- description and source-code
```javascript
geJoiLabel = function (joiObj) {

    // old version
<span class="apidocCodeCommentSpan">    /* $lab:coverage:off$ */
</span>    if (Hoek.reach(joiObj, '_settings.language.label')) {
        return Hoek.reach(joiObj, '_settings.language.label');
    }
    /* $lab:coverage:on$ */
    // Joi > 10.9
    if (Hoek.reach(joiObj, '_flags.label')) {
        return Hoek.reach(joiObj, '_flags.label');
    }

    return null;
}
```
- example usage
```shell
...

// default the use of definitions to true
if (useDefinitions === undefined || useDefinitions === null) {
    useDefinitions = true;
}

// get name from joi label if its not a path
if (!name && Utilities.geJoiLabel(joiObj) && parameterType !== 'path') {
    name = Utilities.geJoiLabel(joiObj);
}

// add correct type and format by mapping
let joiType = joiObj._type.toLowerCase();
// for Joi extension, use the any type
if (!(joiType in this.propertyMap)){
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.getJoiMetaProperty"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>getJoiMetaProperty (joiObj, propertyName)](#apidoc.element.hapi-swagger.utilities.getJoiMetaProperty)
- description and source-code
```javascript
getJoiMetaProperty = function (joiObj, propertyName) {

    // get headers added using meta function
    if (utilities.isJoi(joiObj) && utilities.hasJoiMeta(joiObj)) {

        const meta = joiObj._meta;
        let i = meta.length;
        while (i--) {
            if (meta[i][propertyName]) {
                return meta[i][propertyName];
            }
        }
    }
    return undefined;
}
```
- example usage
```shell
...

// add alternatives properties
if (property.type === 'alternatives') {
    property = this.parseAlternatives(property, joiObj, name, parameterType, useDefinitions);
}

// convert property to file upload, if indicated by meta property
if (Utilities.getJoiMetaProperty(joiObj, 'swaggerType') === 'file') {
    property.type = 'file';
    property.in = 'formData';
}

property = Utilities.deleteEmptyProperties(property);
if (joiCache && property.$ref) {
    joiCache.set(joiObj, property);
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.hasJoiChildren"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasJoiChildren (joiObj)](#apidoc.element.hapi-swagger.utilities.hasJoiChildren)
- description and source-code
```javascript
hasJoiChildren = function (joiObj) {

    return (utilities.isJoi(joiObj) && Hoek.reach(joiObj, '_inner.children')) ? true : false;
}
```
- example usage
```shell
...
let payloadStructures = this.getDefaultStructures();
let payloadJoi = internals.getJOIObj(route, 'payloadParams');
if (payloadType.toLowerCase() === 'json') {
    // set as json
    payloadStructures = this.getSwaggerStructures(payloadJoi, 'body', true, false);
} else {
    // set as formData
    if (Utilities.hasJoiChildren(payloadJoi)) {
        payloadStructures = this.getSwaggerStructures(payloadJoi, 'formData', false, false);
    } else {
        self.testParameterError(payloadJoi, 'payload form-urlencoded', path);
    }
    // add form data mimetype
    out.consumes = ['application/x-www-form-urlencoded'];
}
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.hasJoiMeta"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasJoiMeta (joiObj)](#apidoc.element.hapi-swagger.utilities.hasJoiMeta)
- description and source-code
```javascript
hasJoiMeta = function (joiObj) {

    return (utilities.isJoi(joiObj) && Array.isArray(joiObj._meta)) ? true : false;
}
```
- example usage
```shell
...
 * @param  {Object} joiObj
 * @param  {String} propertyName
 * @return {Object || Undefined}
 */
utilities.getJoiMetaProperty = function (joiObj, propertyName) {

    // get headers added using meta function
    if (utilities.isJoi(joiObj) && utilities.hasJoiMeta(joiObj)) {

const meta = joiObj._meta;
let i = meta.length;
while (i--) {
    if (meta[i][propertyName]) {
        return meta[i][propertyName];
    }
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.hasKey"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasKey (obj, findKey)](#apidoc.element.hapi-swagger.utilities.hasKey)
- description and source-code
```javascript
hasKey = function (obj, findKey) {

    for (var key in obj) {
        if (obj.hasOwnProperty(key)) {
            if (typeof obj[key] === 'object') {
                if (this.hasKey(obj[key], findKey) === true) {

                    return true;
                }
            }
            if (key === findKey) {
                return true;
            }
        }
    }
    return false;
}
```
- example usage
```shell
...
 * @return {Boolean}
 */
utilities.hasKey = function (obj, findKey) {

    for (var key in obj) {
        if (obj.hasOwnProperty(key)) {
if (typeof obj[key] === 'object') {
    if (this.hasKey(obj[key], findKey) === true) {

        return true;
    }
}
if (key === findKey) {
    return true;
}
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.hasProperties"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>hasProperties (obj)](#apidoc.element.hapi-swagger.utilities.hasProperties)
- description and source-code
```javascript
hasProperties = function (obj) {

    let key;
    for (key in obj) {
        if (obj.hasOwnProperty(key)) {
            return true;
        }
    }
    return false;
}
```
- example usage
```shell
...
// append group property - by path
Group.appendGroupByPath(settings.pathPrefixSize, settings.basePath, routes, settings.pathReplacements);

let paths = new Paths(settings);
let pathData = paths.build(routes);
out.paths = pathData.paths;
out.definitions = pathData.definitions;
if (Utilities.hasProperties(pathData['x-alt-definitions'])) {
    out['x-alt-definitions'] = pathData['x-alt-definitions'];
}
out = internals.removeNoneSchemaOptions(out);

if (settings.debug) {
    Validate.log(out, settings.log);
}
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.isFunction"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isFunction (obj)](#apidoc.element.hapi-swagger.utilities.isFunction)
- description and source-code
```javascript
isFunction = function (obj) {

    // remove 'obj.constructor' test as it was always true
    return !!(obj && obj.call && obj.apply);
}
```
- example usage
```shell
...
'queryParams',
'pathParams',
'headerParams',
'payloadParams'
        ].forEach(function (property) {

// swap out any custom validation function for Joi object/string
if (Utilities.isFunction(routeData[property])) {
    if (property !== 'pathParams') {
        self.settings.log(['vaildation', 'warning'], 'Using a Joi.function for a query, header or payload is not supported.');
        if (property === 'payloadParams') {
            routeData[property] = Joi.object().label('Hidden Model');
        } else {
            routeData[property] = Joi.object({ 'Hidden Model': Joi.string() });
        }
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.isJoi"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isJoi (joiObj)](#apidoc.element.hapi-swagger.utilities.isJoi)
- description and source-code
```javascript
isJoi = function (joiObj) {

    return (joiObj && joiObj.isJoi) ? true : false;
}
```
- example usage
```shell
...
 * @return {Object}
 */
internals.properties.prototype.parseProperty = function (name, joiObj, parent, parameterType, useDefinitions, isAlt) {

let property = { type: 'void' };

// if wrong format or forbidden - return undefined
if (!Utilities.isJoi(joiObj)) {
    return undefined;
}
if (Hoek.reach(joiObj, '_flags.presence') === 'forbidden') {
    return undefined;
}

// default the use of definitions to true
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.isObject"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isObject (obj)](#apidoc.element.hapi-swagger.utilities.isObject)
- description and source-code
```javascript
isObject = function (obj) {

    return obj !== null && obj !== undefined && typeof obj === 'object' && !Array.isArray(obj);
}
```
- example usage
```shell
...

property.minLength = internals.getArgByName(describe.rules, 'min');
property.maxLength = internals.getArgByName(describe.rules, 'max');

// add regex
joiObj._tests.forEach((test) => {
    // Joi post v10
    if (Utilities.isObject(test.arg) && test.arg.pattern) {
        property.pattern = test.arg.pattern.toString();
    }
    // Joi pre v10
    /* $lab:coverage:off$ */
    if (Utilities.isRegex(test.arg)) {
        property.pattern = test.arg.toString();
    }
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.isRegex"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>isRegex (obj)](#apidoc.element.hapi-swagger.utilities.isRegex)
- description and source-code
```javascript
isRegex = function (obj) {

    // base on https://github.com/ljharb/is-regex/
    // has a couple of edge use cases for different env  - hence coverage:off
<span class="apidocCodeCommentSpan">    /* $lab:coverage:off$ */
</span>    const regexExec = RegExp.prototype.exec;
    const tryRegexExec = function tryRegexExec (value) {

        try {
            regexExec.call(value);
            return true;
        } catch (e) {
            return false;
        }
    };
    const toStr = Object.prototype.toString;
    const regexClass = '[object RegExp]';
    const hasToStringTag = typeof Symbol === 'function' && typeof Symbol.toStringTag === 'symbol';

    if (typeof obj !== 'object') {
        return false;
    }
    return hasToStringTag ? tryRegexExec(obj) : toStr.call(obj) === regexClass;
    /* $lab:coverage:on$ */
}
```
- example usage
```shell
...
joiObj._tests.forEach((test) => {
    // Joi post v10
    if (Utilities.isObject(test.arg) && test.arg.pattern) {
        property.pattern = test.arg.pattern.toString();
    }
    // Joi pre v10
    /* $lab:coverage:off$ */
    if (Utilities.isRegex(test.arg)) {
        property.pattern = test.arg.toString();
    }
    /* $lab:coverage:on$ */
});


// add extended properties not part of openAPI spec
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.removeProps"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>removeProps (obj, listOfProps)](#apidoc.element.hapi-swagger.utilities.removeProps)
- description and source-code
```javascript
removeProps = function (obj, listOfProps) {

    for (let key in obj) {
        if (obj.hasOwnProperty(key)) {
            if (listOfProps.indexOf(key) === -1 && this.startsWith(key, 'x-') === false) {
                delete obj[key];
                //console.log('Removed property: ' + key + ' from object: ', JSON.stringify(obj));
            }
        }
    }
    return obj;
}
```
- example usage
```shell
...

    // reinstate x-alternatives at parameter level
    if (schemaObj['x-alternatives']) {
        item['x-alternatives'] = schemaObj['x-alternatives'];
        delete item.schema['x-alternatives'];
    }

    item = Utilities.removeProps(item, this.allowedProps);
    if (!Hoek.deepEqual(item.schema, { 'type': 'object' }, { prototype: false })) {
        out.push(Utilities.deleteEmptyProperties(item));
    }

// if its an array of parameters
} else {
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.removeTrailingSlash"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>removeTrailingSlash (str)](#apidoc.element.hapi-swagger.utilities.removeTrailingSlash)
- description and source-code
```javascript
removeTrailingSlash = function (str) {

    if (str.endsWith('/')) {
        return str.slice(0, -1);
    }
    return str;
}
```
- example usage
```shell
...

// collect root information
builder.default.host = internals.getHost(request, namedConnection);
builder.default.schemes = [internals.getSchema(request, connection)];

settings = Hoek.applyToDefaults(builder.default, settings);
if (settings.basePath !== '/') {
    settings.basePath = Utilities.removeTrailingSlash(settings.basePath);
}
let out = internals.removeNoneSchemaOptions(settings);
Joi.assert(out, builder.schema);


out.info = Info.build(settings);
out.tags = Tags.build(settings);
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.replaceInPath"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>replaceInPath (path, applyTo, options)](#apidoc.element.hapi-swagger.utilities.replaceInPath)
- description and source-code
```javascript
replaceInPath = function (path, applyTo, options) {

    options.forEach((option) => {
        if (applyTo.indexOf(option.replaceIn) > -1 || option.replaceIn === 'all') {
            path = path.replace(option.pattern, option.replacement);
        }
    });
    return path;
}
```
- example usage
```shell
...
 * @param  {Array} pathReplacements
 * @return {Array}
 */
group.getNameByPath = function (pathPrefixSize, basePath, path, pathReplacements) {


if (pathReplacements) {
    path = Utilities.replaceInPath(path, ['groups'], pathReplacements);
}

let i = 0;
let pathHead = [];
let parts = path.split('/');

while (parts.length > 0) {
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.replaceValue"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>replaceValue (array, current, replacement)](#apidoc.element.hapi-swagger.utilities.replaceValue)
- description and source-code
```javascript
replaceValue = function (array, current, replacement) {

    if (array && current && replacement) {
        array = Hoek.clone(array);
        if (array.indexOf(current) > -1) {
            array.splice(array.indexOf(current), 1);
            array.push(replacement);
        }
    }
    return array;
}
```
- example usage
```shell
...
        if (Utilities.geJoiLabel(joiChildObj)) {
            itemName = Utilities.geJoiLabel(joiChildObj);
        }
        //name, joiObj, parent, parameterType, useDefinitions, isAlt
        property.properties[keyName] = this.parseProperty(itemName, joiChildObj, property, parameterType, useDefinitions, isAlt);
        // switch references if naming has changed
        if (keyName !== itemName) {
            property.required = Utilities.replaceValue(property.required, itemName, keyName);
            property.optional = Utilities.replaceValue(property.optional, itemName, keyName);
        }
    });
    property.name = name;
    return property;
};
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.sortFirstItem"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>sortFirstItem (array, firstItem)](#apidoc.element.hapi-swagger.utilities.sortFirstItem)
- description and source-code
```javascript
sortFirstItem = function (array, firstItem) {

    let out = array;
    if (firstItem) {
        out = [firstItem];
        array.forEach(function (item) {

            if (item !== firstItem) {
                out.push(item);
            }
        });
    }
    return out;
}
```
- example usage
```shell
...
}
// if the API has a user set accept header with a enum convert into the produces array
if (this.settings.acceptToProduce === true) {
    headerStructures.parameters = headerStructures.parameters.filter(function (header) {

        if (header.name.toLowerCase() === 'accept') {
            if (header.enum) {
                out.produces = Utilities.sortFirstItem(header.enum, header.default);
                return false;
            }
        }
        return true;
    });
}
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.startsWith"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>startsWith (str, test)](#apidoc.element.hapi-swagger.utilities.startsWith)
- description and source-code
```javascript
startsWith = function (str, test) {

    return (str.indexOf(test) === 0);
}
```
- example usage
```shell
...
 * @return {String}
 */
internals.nextModelName = function (currentCollection) {

let highest = 0;
let key;
for (key in currentCollection) {
    if (Utilities.startsWith(key, 'Model')) {
        let num = parseInt(key.replace('Model', ''), 10);
        if (num && num > highest) {
            highest = num;
        }
    }
}
return 'Model ' + (highest + 1);
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.toJoiObject"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>toJoiObject (obj)](#apidoc.element.hapi-swagger.utilities.toJoiObject)
- description and source-code
```javascript
toJoiObject = function (obj) {

    if (utilities.isJoi(obj) === false && utilities.isObject(obj)) {
        return Joi.object(obj);
    }
    return obj;
}
```
- example usage
```shell
...


routeData.path = Utilities.replaceInPath(routeData.path, ['endpoints'], this.settings.pathReplacements);


// user configured interface through route plugin options
if (Hoek.reach(routeOptions, 'validate.query')) {
    routeData.queryParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.query'));
}
if (Hoek.reach(routeOptions, 'validate.params')) {
    routeData.pathParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.params'));
}
if (Hoek.reach(routeOptions, 'validate.headers')) {
    routeData.headerParams = Utilities.toJoiObject(Hoek.reach(routeOptions, 'validate.headers'));
}
...
```

#### <a name="apidoc.element.hapi-swagger.utilities.toTitleCase"></a>[function <span class="apidocSignatureSpan">hapi-swagger.utilities.</span>toTitleCase (word)](#apidoc.element.hapi-swagger.utilities.toTitleCase)
- description and source-code
```javascript
toTitleCase = function (word) {

    return word.replace(/\w\S*/g, (txt) => {
        return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase();
    });
}
```
- example usage
```shell
...

    const self = this;
    if (path.indexOf('/') > -1) {
        let items = path.split('/');
        items = items.map(function (item) {
            // replace chars such as '{'
            item = item.replace(/[^\w\s]/gi, '');
            return self.toTitleCase(item);
        });
        path = items.join('');
    } else {
        path = self.toTitleCase(path);
    }
    return method.toLowerCase() + path;
};
...
```



# <a name="apidoc.module.hapi-swagger.validate"></a>[module hapi-swagger.validate](#apidoc.module.hapi-swagger.validate)

#### <a name="apidoc.element.hapi-swagger.validate.log"></a>[function <span class="apidocSignatureSpan">hapi-swagger.validate.</span>log (doc, logFnc)](#apidoc.element.hapi-swagger.validate.log)
- description and source-code
```javascript
log = function (doc, logFnc) {

    SwaggerParser.validate(doc, (err) => {

        // use err.message so thrown error object is not passed into testing
        if (err) {
            logFnc(['validation', 'error'], 'FAILED - ' + err.message);
        } else {
            logFnc(['validation', 'info'], 'PASSED - The swagger.json validation passed.');
        }
    });
}
```
- example usage
```shell
...
    Vision,
    {
        'register': HapiSwagger,
        'options': options
    }], (err) => {
        server.start( (err) => {
           if (err) {
                console.log(err);
            } else {
                console.log('Server running at:', server.info.uri);
            }
        });
    });

server.route(Routes);
...
```

#### <a name="apidoc.element.hapi-swagger.validate.test"></a>[function <span class="apidocSignatureSpan">hapi-swagger.validate.</span>test (doc, next)](#apidoc.element.hapi-swagger.validate.test)
- description and source-code
```javascript
test = function (doc, next) {

    SwaggerParser.validate(doc, (err) => {
        // use err.message so thrown error object is not passed into testing
        if (err) {
            next(err.message, false);
        } else {
            next(null, true);
        }
    });

}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
