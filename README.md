# youtube audio stream

Simple Audio Stream on local, work on low network connection

> This code works on python 3 that's not tested on python version less than 3

# Requirements

1. Flask
2. youtube-dl

# Clone & Usaged

```
git clone https://github.com/hoathienvu8x/youtube-audio-stream
cd youtube-audio-stream
chmod +x stream
pip3 install -r requirements.txt
./stream
```

To Restful using url `http://127.0.0.1:9600/fetch` methods allowed `[POST, GET]` param required `vid`

`vid`: Youtube ID like this `https://www.youtube.com/watch?v=wGY81Ms6OLs` then so `vid` is `wGY81Ms6OLs`

Response is `JSON` object type with key container `error` or `data` if has key `error` that mean
youtube audio parsed is not ok, else key `data` store `url` of audio

To using UI please visit url `http://127.0.0.1:9600/stream` allow `GET` method, param `is` not required if using that `id` is Youtube ID
