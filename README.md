# gretchen-fetch
Making "fetch" happen!

This fetch library is _so fetch_! It would make Gretchen proud.

## What is this?

A fetching library that can be used in any javascript-based application, whether that is client side or server side. Included in this fetching library is 3 ways to fetch:
1. Promise-based (regular promise, or async/await)
2. Callback-based (but why would you want to?)
3. Class-based (e.g. new Gretch())

## Installing and Importing

Install:
```
npm install gretchen-fetch
or
yarn gretchen-fetch
```

Importing:
```
import Gretch from 'gretchen-fetch';
or
const Gretch = require('gretchen-fetch');
```

## Usage

Promise-based
```
const somePromise = Gretch.get('<url>', { ...queryParams });
or
const results = await Gretch.get('<url', { ...queryParams });
```

Callback-based
```
Gretch.get('<url>', { ...queryParams }, function(results) {});
```

Class-based
```
const gretchen = new Gretch();
gretchen.makeFetchHappen(options);
```

## The nitty-gritty

There are several static methods built for you. Each follow the pattern of the following for parameters:
```
Gretch.method(url, params/data, callback, options)
```
- Gretch.get:
- Gretch.post: 
- Gretch.put:
- Gretch.delete: 
- Gretch.patch: 
- Gretch.options: 
- Gretch.head:

Alternately, you can use the raw request method to customize to your liking:
```
Gretch.fetch({
  method: <see list above, defaults to "get">
  url: '<url>',
  params: { "key": "value" },
  data: <some data>,
  callback: (results)=>{},
  headers: { "name": "value" },
  timeout: <ms>,
  responseType: <valid reponse type, defaults to json>,
  .......?
});
```
