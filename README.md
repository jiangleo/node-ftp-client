fixed bug and can't use 'overwrite:older' mode.

```
0|www      | 2018-11-13-15:30:08: series error { Error: OOPS: vsf_sysutil_bind
0|www      |     at makeError (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:1067:13)
0|www      |     at Parser.<anonymous> (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:113:25)
0|www      |     at emitTwo (events.js:106:13)
0|www      |     at Parser.emit (events.js:194:7)
0|www      |     at Parser._write (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/parser.js:59:10)
0|www      |     at doWrite (_stream_writable.js:329:12)
0|www      |     at writeOrBuffer (_stream_writable.js:315:5)
0|www      |     at Parser.Writable.write (_stream_writable.js:241:11)
0|www      |     at Socket.ondata (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:273:20)
0|www      |     at emitOne (events.js:96:13)
0|www      |     at Socket.emit (events.js:191:7)
0|www      |     at readableAddChunk (_stream_readable.js:178:18)
0|www      |     at Socket.Readable.push (_stream_readable.js:136:10)
0|www      |     at TCP.onread (net.js:561:20) code: 500 }
0|www      | 2018-11-13-15:30:08: { Error: OOPS: vsf_sysutil_bind
0|www      |     at makeError (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:1067:13)
0|www      |     at Parser.<anonymous> (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:113:25)
0|www      |     at emitTwo (events.js:106:13)
0|www      |     at Parser.emit (events.js:194:7)
0|www      |     at Parser._write (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/parser.js:59:10)
0|www      |     at doWrite (_stream_writable.js:329:12)
0|www      |     at writeOrBuffer (_stream_writable.js:315:5)
0|www      |     at Parser.Writable.write (_stream_writable.js:241:11)
0|www      |     at Socket.ondata (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:273:20)
0|www      |     at emitOne (events.js:96:13)
0|www      |     at Socket.emit (events.js:191:7)
0|www      |     at readableAddChunk (_stream_readable.js:178:18)
0|www      |     at Socket.Readable.push (_stream_readable.js:136:10)
0|www      |     at TCP.onread (net.js:561:20) code: 500 }
0|www      | 2018-11-13-15:30:08: list error
0|www      | 2018-11-13-15:30:08: [ './upload/8a6ccd358503f72e9a66c23dc07c69e4.zip',
0|www      |   './upload/eaf9f0115a7ca78e9d0e051f447c713f.zip' ]
0|www      | 2018-11-13-15:30:08: FILES TO UPLOAD
0|www      | 2018-11-13-15:30:08: DIRS TO UPLOAD
0|www      | 2018-11-13-15:30:08: series error { Error: OOPS: priv_sock_get_int
0|www      |     at makeError (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:1067:13)
0|www      |     at Parser.<anonymous> (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:113:25)
0|www      |     at emitTwo (events.js:106:13)
0|www      |     at Parser.emit (events.js:194:7)
0|www      |     at Parser._write (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/parser.js:59:10)
0|www      |     at doWrite (_stream_writable.js:329:12)
0|www      |     at writeOrBuffer (_stream_writable.js:315:5)
0|www      |     at Parser.Writable.write (_stream_writable.js:241:11)
0|www      |     at Socket.ondata (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:273:20)
0|www      |     at emitOne (events.js:96:13)
0|www      |     at Socket.emit (events.js:191:7)
0|www      |     at readableAddChunk (_stream_readable.js:178:18)
0|www      |     at Socket.Readable.push (_stream_readable.js:136:10)
0|www      |     at TCP.onread (net.js:561:20) code: 500 }
0|www      | 2018-11-13-15:30:08: { Error: OOPS: priv_sock_get_int
0|www      |     at makeError (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:1067:13)
0|www      |     at Parser.<anonymous> (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:113:25)
0|www      |     at emitTwo (events.js:106:13)
0|www      |     at Parser.emit (events.js:194:7)
0|www      |     at Parser._write (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/parser.js:59:10)
0|www      |     at doWrite (_stream_writable.js:329:12)
0|www      |     at writeOrBuffer (_stream_writable.js:315:5)
0|www      |     at Parser.Writable.write (_stream_writable.js:241:11)
0|www      |     at Socket.ondata (/opt/web/wuba-rnplatform3/back-end/node_modules/ftp/lib/connection.js:273:20)
0|www      |     at emitOne (events.js:96:13)
0|www      |     at Socket.emit (events.js:191:7)
0|www      |     at readableAddChunk (_stream_readable.js:178:18)
0|www      |     at Socket.Readable.push (_stream_readable.js:136:10)
0|www      |     at TCP.onread (net.js:561:20) code: 500 }
```


# Description
node-ftp-client is a wrapper for the popular FTP client module for [node.js](http://nodejs.org/) - node-ftp, which
provides an easy way of manipulating FTP transfers.


# Requirements

* [node.js](http://nodejs.org/) -- v0.8.0 or newer


# Dependencies

* [node-ftp](https://github.com/mscdex/node-ftp) -- v0.3.6
* [glob](https://github.com/isaacs/node-glob) -- v3.2.9
* [lodash](https://github.com/lodash/lodash-node) -- v2.4.1
* [async](https://github.com/caolan/async) -- v0.8.0

# Installation

    npm install ftp-client

# Usage

## Initialization
To crate an instance of the wrapper use the following code:

```javascript
var ftpClient = require('ftp-client'),
client = new ftpClient(config, options);
```

where `config` contains the ftp server configuration (these are the default values):
```javascript
{
    host: 'localhost',
    port: 21,
    user: 'anonymous',
    password: 'anonymous@'
}
```

and the `options` object may contain the following keys:

* *logging* (String): 'none', 'basic', 'debug' - level of logging for all the tasks - use 'debug' in case of any issues
* *overwrite* (String): 'none', 'older', 'all' - determines which files should be overwritten when downloading/uploading - 'older' compares the date of modification of local and remote files

### Connecting
After creating the new object you have to manually connect to the server by using the `connect` method:
```javascript
client.connect(callback);
```
And passing the callback which should be executed when the client is ready.

## Methods
* **download**(< String > remoteDir, < String > localDir, < Object > options, < Function > callback) - downloads the contents
of `remoteDir` to `localDir` if both exist, and executes the `callback` if one is supplied with the following object as a parameter:
```javascript
{
    downloadedFiles: [(filename)],
    errors: {
        (filename): (error)
    }
}
```
`options` is an object with the following possible keys
    * *overwrite* (String): 'none', 'older', 'all' - determines which files should be overwritten

* **upload**(< mixed > source, < String > remoteDir, < Object > options, < Function > callback) - expands the `source` paths
using the glob module, uploads all found files and directories to the specified `remoteDir` , and executes the `callback`
if one is supplied with the following object as a parameter:
```javascript
{
    uploadedFiles: [(filename)],
    uploadedDirectories: [(dirname)],
    errors: {
        (filename/dirname): (error)
    }
}
```
`source` can be a string or an array of strings, and
`options` is an object with the following possible keys
    * *overwrite* (String): 'none', 'older', 'all' - determines which files should be overwritten
    * *baseDir* (String) - local base path relative to the remote directory, e.g. if you want to upload file
    `uploads/sample.js` to `public_html/uploads`, *baseDir* has to be set to `uploads`

# Examples
In this example we connect to a server, and simultaneously upload all files from the `test` directory, overwriting only
older files found on the server, and download files from `/public_html/test` directory.

```javascript
var ftpClient = require('./lib/client.js'),
    config = {
        host: 'localhost',
        port: 21,
        user: 'anonymous',
        password: 'anonymous@'
    },
    options = {
        logging: 'basic'
    },
    client = new ftpClient(config, options);

client.connect(function () {

    client.upload(['test/**'], '/public_html/test', {
        baseDir: 'test',
        overwrite: 'older'
    }, function (result) {
        console.log(result);
    });

    client.download('/public_html/test2', 'test2/', {
        overwrite: 'all'
    }, function (result) {
        console.log(result);
    });

});
```

TODO
====
* Methods chaining
* Queuing downloads/uploads with async in a single session
* Connecting in constructor, with possibility to end the connection manually