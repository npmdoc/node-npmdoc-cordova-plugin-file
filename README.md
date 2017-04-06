# api documentation for  [cordova-plugin-file (v4.3.2)](https://github.com/apache/cordova-plugin-file#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-cordova-plugin-file.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-cordova-plugin-file) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-cordova-plugin-file.svg)](https://travis-ci.org/npmdoc/node-npmdoc-cordova-plugin-file)
#### Cordova File Plugin

[![NPM](https://nodei.co/npm/cordova-plugin-file.png?downloads=true)](https://www.npmjs.com/package/cordova-plugin-file)

[![apidoc](https://npmdoc.github.io/node-npmdoc-cordova-plugin-file/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-cordova-plugin-file_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-cordova-plugin-file/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-cordova-plugin-file/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-cordova-plugin-file/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Apache Software Foundation"
    },
    "bugs": {
        "url": "https://github.com/apache/cordova-plugin-file/issues"
    },
    "cordova": {
        "id": "cordova-plugin-file",
        "platforms": [
            "android",
            "amazon-fireos",
            "ubuntu",
            "ios",
            "osx",
            "wp7",
            "wp8",
            "blackberry10",
            "windows8",
            "windows",
            "firefoxos"
        ]
    },
    "dependencies": {},
    "description": "Cordova File Plugin",
    "devDependencies": {
        "jshint": "^2.6.0"
    },
    "directories": {},
    "dist": {
        "shasum": "d2d213f340e3a41915006f4dab91d44b76ccc3f1",
        "tarball": "https://registry.npmjs.org/cordova-plugin-file/-/cordova-plugin-file-4.3.2.tgz"
    },
    "engines": {
        "cordovaDependencies": {
            "5.0.0": {
                "cordova": ">100"
            }
        }
    },
    "homepage": "https://github.com/apache/cordova-plugin-file#readme",
    "keywords": [
        "cordova",
        "file",
        "ecosystem:cordova",
        "cordova-android",
        "cordova-amazon-fireos",
        "cordova-ubuntu",
        "cordova-ios",
        "cordova-osx",
        "cordova-wp7",
        "cordova-wp8",
        "cordova-blackberry10",
        "cordova-windows8",
        "cordova-windows",
        "cordova-firefoxos"
    ],
    "license": "Apache-2.0",
    "maintainers": [
        {
            "name": "bowserj",
            "email": "bowserj@apache.org"
        },
        {
            "name": "csantanapr",
            "email": "csantana23@gmail.com"
        },
        {
            "name": "filmaj",
            "email": "maj.fil@gmail.com"
        },
        {
            "name": "kotikov.vladimir",
            "email": "kotikov.vladimir@gmail.com"
        },
        {
            "name": "purplecabbage",
            "email": "purplecabbage@gmail.com"
        },
        {
            "name": "shazron",
            "email": "shazron@gmail.com"
        },
        {
            "name": "stevegill",
            "email": "stevengill97@gmail.com"
        }
    ],
    "name": "cordova-plugin-file",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/apache/cordova-plugin-file.git"
    },
    "scripts": {
        "jshint": "node node_modules/jshint/bin/jshint www && node node_modules/jshint/bin/jshint src && node node_modules/jshint/bin/jshint tests",
        "test": "npm run jshint"
    },
    "types": "./types/index.d.ts",
    "version": "4.3.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module cordova-plugin-file](#apidoc.module.cordova-plugin-file)
1.  [function <span class="apidocSignatureSpan">cordova-plugin-file.</span>File (name, localURL, type, lastModifiedDate, size)](#apidoc.element.cordova-plugin-file.File)
1.  object <span class="apidocSignatureSpan">cordova-plugin-file.</span>File.prototype
1.  object <span class="apidocSignatureSpan">cordova-plugin-file.</span>fileSystems

#### [module cordova-plugin-file.File](#apidoc.module.cordova-plugin-file.File)
1.  [function <span class="apidocSignatureSpan">cordova-plugin-file.</span>File (name, localURL, type, lastModifiedDate, size)](#apidoc.element.cordova-plugin-file.File.File)

#### [module cordova-plugin-file.File.prototype](#apidoc.module.cordova-plugin-file.File.prototype)
1.  [function <span class="apidocSignatureSpan">cordova-plugin-file.File.prototype.</span>slice (start, end)](#apidoc.element.cordova-plugin-file.File.prototype.slice)

#### [module cordova-plugin-file.fileSystems](#apidoc.module.cordova-plugin-file.fileSystems)
1.  [function <span class="apidocSignatureSpan">cordova-plugin-file.fileSystems.</span>getFs (name, callback)](#apidoc.element.cordova-plugin-file.fileSystems.getFs)



# <a name="apidoc.module.cordova-plugin-file"></a>[module cordova-plugin-file](#apidoc.module.cordova-plugin-file)

#### <a name="apidoc.element.cordova-plugin-file.File"></a>[function <span class="apidocSignatureSpan">cordova-plugin-file.</span>File (name, localURL, type, lastModifiedDate, size)](#apidoc.element.cordova-plugin-file.File)
- description and source-code
```javascript
File = function (name, localURL, type, lastModifiedDate, size){
    this.name = name || '';
    this.localURL = localURL || null;
    this.type = type || null;
    this.lastModified = lastModifiedDate || null;
    // For backwards compatibility, store the timestamp in lastModifiedDate as well
    this.lastModifiedDate = lastModifiedDate || null;
    this.size = size || 0;

    // These store the absolute start and end for slicing the file.
    this.start = 0;
    this.end = this.size;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cordova-plugin-file.File"></a>[module cordova-plugin-file.File](#apidoc.module.cordova-plugin-file.File)

#### <a name="apidoc.element.cordova-plugin-file.File.File"></a>[function <span class="apidocSignatureSpan">cordova-plugin-file.</span>File (name, localURL, type, lastModifiedDate, size)](#apidoc.element.cordova-plugin-file.File.File)
- description and source-code
```javascript
File = function (name, localURL, type, lastModifiedDate, size){
    this.name = name || '';
    this.localURL = localURL || null;
    this.type = type || null;
    this.lastModified = lastModifiedDate || null;
    // For backwards compatibility, store the timestamp in lastModifiedDate as well
    this.lastModifiedDate = lastModifiedDate || null;
    this.size = size || 0;

    // These store the absolute start and end for slicing the file.
    this.start = 0;
    this.end = this.size;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cordova-plugin-file.File.prototype"></a>[module cordova-plugin-file.File.prototype](#apidoc.module.cordova-plugin-file.File.prototype)

#### <a name="apidoc.element.cordova-plugin-file.File.prototype.slice"></a>[function <span class="apidocSignatureSpan">cordova-plugin-file.File.prototype.</span>slice (start, end)](#apidoc.element.cordova-plugin-file.File.prototype.slice)
- description and source-code
```javascript
slice = function (start, end) {
    var size = this.end - this.start;
    var newStart = 0;
    var newEnd = size;
    if (arguments.length) {
        if (start < 0) {
            newStart = Math.max(size + start, 0);
        } else {
            newStart = Math.min(size, start);
        }
    }

    if (arguments.length >= 2) {
        if (end < 0) {
            newEnd = Math.max(size + end, 0);
        } else {
            newEnd = Math.min(end, size);
        }
    }

    var newFile = new File(this.name, this.localURL, this.type, this.lastModified, this.size);
    newFile.start = this.start + newStart;
    newFile.end = this.start + newEnd;
    return newFile;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.cordova-plugin-file.fileSystems"></a>[module cordova-plugin-file.fileSystems](#apidoc.module.cordova-plugin-file.fileSystems)

#### <a name="apidoc.element.cordova-plugin-file.fileSystems.getFs"></a>[function <span class="apidocSignatureSpan">cordova-plugin-file.fileSystems.</span>getFs (name, callback)](#apidoc.element.cordova-plugin-file.fileSystems.getFs)
- description and source-code
```javascript
getFs = function (name, callback) {
    callback(null);
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
