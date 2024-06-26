<img  src="https://i.imgur.com/iJe6rsZ.png"  width="500">



![Number of GitHub stars](https://img.shields.io/github/stars/d60/twikit)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/d60/twikit)
![Version](https://img.shields.io/pypi/v/twikit?label=PyPI)
[![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=Create%20your%20own%20Twitter%20bot%20for%20free%20with%20%22Twikit%22!%20%23python%20%23twitter%20%23twikit%20%23programming%20%23github%20%23bot&url=https%3A%2F%2Fgithub.com%2Fd60%2Ftwikit)
[![Discord](https://img.shields.io/badge/Discord-%235865F2.svg?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/nCrByrr8cX)
[![BuyMeACoffee](https://img.shields.io/badge/-buy_me_a%C2%A0coffee-gray?logo=buy-me-a-coffee)](https://www.buymeacoffee.com/d60py)


# Twikit <img height="35"  src="https://i.imgur.com/9HSdIl4.png"  valign="bottom">

simple API wrapper to interact with twitter's unofficial API.

You can log in to Twitter using your account username, email address and password and use most features on Twitter, such as posting and retrieving tweets, liking and following users.

- [Documentation (English)](https://twikit.readthedocs.io/en/latest/twikit.html)



If you have any questions, you can ask on [Discord](https://discord.gg/nCrByrr8cX).



## Features

### Humanized Requests

twikit has no humanity spoof on sending requests.
This repo is fixing that to prevent your account from being frozen.

### No API Key Required

This library uses the unofficial API, therefore does **not require an API key**.

### Completely Free

This library is completely free to use.


## Functionality

This library allows you to perform various Twitter-related actions, including:

-  **Create tweets**

-  **Search tweets**

-  **Retrieve trending topics**

- etc...



## Installing

```bash

pip install git+https://github.com/voidpro-dev/twikit-humanity.git

```



## Quick Example

**Define a client and log in to the account.**

```python
from twikit import Client

USERNAME = 'example_user'
EMAIL = 'email@example.com'
PASSWORD = 'password0000'

# Initialize client
client = Client('en-US')

# Login to the service with provided user credentials
client.login(
    auth_info_1=USERNAME ,
    auth_info_2=EMAIL,
    password=PASSWORD
)
```

**Create a tweet with media attached.**

```python
# Upload media files and obtain media_ids
media_ids = [
    client.upload_media('media1.jpg'),
    client.upload_media('media2.jpg')
]

# Create a tweet with the provided text and attached media
client.create_tweet(
    text='Example Tweet',
    media_ids=media_ids
)

```

**Search the latest tweets based on a keywords**
```python
tweets = client.search_tweet('python', 'Latest')

for tweet in tweets:
    print(
        tweet.user.name,
        tweet.text,
        tweet.created_at
    )
```

**Retrieve user tweets**
```python
tweets = client.get_user_tweets('123456', 'Tweet')

for tweet in tweets:
    print(tweet.text)
```

More Examples: [examples](https://github.com/d60/twikit/tree/main/examples) <br>

## Contributing

I would like to hear your thoughts and suggestions.

If you have any features you'd like to see added or encounter any issues,

please let me know in the [issues](https://github.com/voidpro-dev/twikit-humanity/issues) section.

Additionally, if you find this library useful, I would appreciate it if you would star this repository or share this library⭐! Thank you very much!
