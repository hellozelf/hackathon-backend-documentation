# HackAPI

HackAPI gathers data from various sources IE: Facebook, Instagram, TikTok, Youtube etc, and exposes the data through it's content endpoint. It also gathers data for Author of those gathered contents. As it gathers data from various sources, it might take some time to respond with your API request. 

## Steps

`1. Register`

Register Your Account via [HackAPI Signup](https://hackapi.hellozelf.com/signup/)
, use your email to signup and later user the username to login

`2. Visit Home page of HackAPI`

After registering visit [HackAPI Home Page](https://hackapi.hellozelf.com/home/),
There you will find your API Key, Do not share it with anyone.

`3. How to use the API Key`

In your request header add 

```curl
Headers:
x-api-key: <Your API Key>
```

Without the request header `x-api-key` it will not resolve your request


### About the API

Since the API, gathers data from various source in the internet, it might be slow also it might give you unwanted errors

You might get the following errors:

```json
{
  "message": "Rate limit exceeded",
  "code": 401
}
```

or 
```
{
  "message": "Unable to find contents",
  "code": 402
}
```

You might discover new errors while running the API

## Content and Author API Schema:

```python
{
    "page": 1,
    "next": 2,
    "data": [
    # You have to validate and analyze the data to find out useful data among them     
    ],
    "total_contents": 163,
    "page_size": 30
}
```

Find example response here [Postman Docs](https://www.postman.com/hellozelf/workspace/zelf-hackathon-backend/collection/22135478-cf469307-3989-4260-abc7-95db30696634?action=share&source=copy-link&creator=22135478)

