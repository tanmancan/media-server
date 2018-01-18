# A streaming server using OBS, node and FLV.js

## Requirements

**Open Broadcaster Software:** https://obsproject.com/

**Node Media Server:** https://www.npmjs.com/package/node-media-server

## Install and configure

### Install dependencies

```shell
$ npm install
```

### Configure OBS

```
Settings -> Stream

Stream Type : Custom Streaming Server

URL : rtmp://localhost/live

Stream key : STREAM_NAME
```

### Update config

In index.html, update the `url` property in `playerConfig` to point to the IP address of where the streaming server will be located.

## Stream media and serve via http

To just launch the streaming server without a front end interface, launch OBS, strat a stream and then run

```shell
$ npm run serve
```

To run a webserver showing the video, a node server module is included. Run it  from the root project directory.

```
$ npm run serve
```

Or you can use your own preferred server.
