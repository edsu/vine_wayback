# vine_wayback

*vine_wayback* tries to retrieve a Vine video and its metadata from the Wayback Machine. If the Vine can be found in the Wayback Machine it will be written to disk as an MP4, JSON and standalone HTML file which you can use to view the Vine.

## Install

```shell
pip install vine_wayback
```

## Run

```
vine_wayback https://vine.co/v/iuKJ7JjF2Jt
💾 saved https://vine.co/v/iuKJ7JjF2Jt to /Users/edsu/Projects/vine-wayback/iuKJ7JjF2Jt
```

This will create a directory like:

```
iuKJ7JjF2Jt
├── index.html
├── iuKJ7JjF2Jt.json
└── iuKJ7JjF2Jt.mp4
```

## Use as a function

```python
from vine_wayback

vine = vine_wayback.vine("https://vine.co/v/iuKJ7JjF2Jt")

print(vine['twitter:title'])

open('media.mp4', 'wb').write(vine['video_raw'])
```
