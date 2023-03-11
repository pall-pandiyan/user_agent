# user_agent

## About this Module

I created this module to manupulate user agents for request, cfscrape, cloudscraper or something similar, ths module contains UserAgent Class which houses set of functions to update the latestest user agents (from free api https://www.useragents.me/api), get a random user agent, add one or more custom user agent in the existing ua list, replace the existing list etc,.

## Requirements

requests==2.28.2

This module only needs requests, that is to update the user agent with the latest on from the "https://www.useragents.me/api", if you do not want this functionality we can modify the script a litte to get rid of it.

## Usage

Import the UserAgent class to your python program.

```python
from user_agent.user_agent import UserAgent
```

If you just want a random user agent:

```python
random_ua = UserAgent().get_a_random_ua()
```

Now, you can use this random user agent in requests or any similar package.

```python
headers = {
  "user-agent": random-ua,
}
response = requests.get(url, headers=headers)
```
