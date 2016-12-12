---
title: API Reference

language_tabs:
  - lodash 
  - underscore 

toc_footers:
  - <a href='https://github.com/jpchen/slate'>Contribute on Github</a>

includes:
 - lodash

search: true
---

# Introduction

 This is a cross documentation of [lodash](https://lodash.com/) and [underscore.js](http://underscorejs.org/).  This arose from my need to translate some underscore.js code, and I noticed that there was no place that aggregated the APIs together.  This does not attempt to prescribe one nor the other as the library of choice, as there is plenty of [discussion](http://stackoverflow.com/questions/13789618/differences-between-lodash-and-underscore) of that already  As of the date of writing, this uses lodash [4.17.2](https://www.npmjs.com/package/lodash) and underscore [1.8.3](https://www.npmjs.com/package/underscore).  Freely use for your own benefit (risk).


# Get All Kittens

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```
> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```
