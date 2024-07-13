# Simple setout for RMTP to HLS test

## Usage
To use this server you need `ffmpeg` and OBS installed.

Replace `USE_YOUR_OWN_FFMPEG` with your `ffmpeg` executed path in `app.js`. You can run `which` command.
```
trans: {
    ffmpeg: 'USE_YOUR_OWN_FFMPEG',
    // ...
}
```
Start the server.
```
npm install
npm run start
```

## How to test live stream on local machine
Use OBS to push RTMP stream to this server with URI like this
```
rtmp://localhost/live
```
and get HLS output from this URI
```
http://localhost:8000/live/index.m3u8
```

`live` is the app name, you can change it in `config` object in `app.js`.