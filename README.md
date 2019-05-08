# redis-nodejs-caching
This is a demo project to illustrate caching API calls in NodeJS (Express) using Redis in-memory data store. In its simplest 
form, an API calls is made to a remote API ``/photos`` to retrieve a list of photos. For each request, Express server queries 
Redis for any cached request using a unique key. If the key exists Express loads the photos from Redis.

## Prerequisites
Install the following to get started:

* NodeJS (https://nodejs.org/en/download/)
* Redis (https://redis.io/download)
* Postman (https://www.getpostman.com/downloads/)

## Setup
Start the development server by:

```
$ node server.js
```

Using Postman, visit http://localhost:3000/photos. The first request will take longer time, as data is being pulled from 
a remote Server. See below the comparison of the Remote and Redis requests:

Remote Request:

<img src="./screenshots/api.png"
     alt="remote api request"
     style="float: left; margin-right: 10px;" />


Redist Request:

<img src="./screenshots/redis.png"
     alt="redis api request"
     style="float: left; margin-right: 10px;" />


## License
```
MIT License

Copyright (c) 2019 Mr Mod

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
