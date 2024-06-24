# Fake RTSP Stream

## Requirements:

- docker installed
- docker-compose installed

## Features:

- stream as many RTSP streams from local files as you want;
- streams are translated in a loop;
- source is FFmpeg, so you can utilize its power to implement extra transformations, transcoding, etc.

To understand what to do next, look at [docker-compose.yml](docker-compose.yml); it provides all the necessary
information to understand what to do to add additional RTSP sources.

## Steps

- Step01: At ./samples folder, create folders, each folder contains videos, example:

```
  ./samples
  ├──CAM_001
  │   ├── XeVao.mp4
  └───CAM_002
      ├── XeRa1.mp4
      └── XeRa2.mp4
```

- Step02:

```
  docker-compose up
```

Now, test results: rtsp://machine-ip:8554/<'stream-name'>
Example: rtsp://localhost:8554/CAM_002
