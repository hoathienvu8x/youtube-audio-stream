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

Response is `JSON` object type if has key `error` that mean
youtube audio parsed is not ok, return `JSON` object struct like:

**Full JSON**

```json
{
  "title":"the title",
  "description":"the description",
  "formats":[
    {
      "mimetype":"mimetype",
      "tag": "tag id",
      "url":"url stream"
    }
  ]
}
```

The `title`, `description` sometime is not responded

To using UI please visit url `http://127.0.0.1:9600/stream` allow `GET` method, param `id` not required if using that `id` is Youtube ID
