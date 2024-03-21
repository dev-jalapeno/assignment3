# 3040Crypto API

Our company, 3040Crypto, should offer API endpoints for any developer to use!

At its heart, 3040Crypto is a Crypto Wallet service, storing users' Crypto Currencies.  
However, we currently aren't leveraging APIs, and therefore not staying competitively sound.

We should consider adding further functionality via API access for developers. This means creating a suite of powerful transactions that enable account changes, purchasing or selling of coins, and more, outside of our application. Not only would this allow third-party services to incorporate our wallet into their service, increasing our market share, but would also mean that the development required to do so would be on someone else's time.

The first API we propose implementing would deal with crypto wallet management by allowing users to buy or sell their cryptocurrency.
<br>
<br>
## Prerequisites
To use the API, a user must have a 'user token'. This is created when they make a wallet with 3040Crypto, so having an account with us is required. For another application to use the API, the user must willingly share their `user token` with the application/service in question. This prevents people from using a wallet that does not belong to them.
<br>
<br>
# API
## Buy Coin Endpoint
This POST request will buy the user's coin.
```
json?usertoken=USER_TOKEN&coin=COIN
```

- `usertoken` - User token pertaining to the User buying the coin
- `coin` - SYMBOL for coin (their stock market name, typically 3 or 4 letters)

Passing a valid User Token and a valid coin would use money in the user's account to purchase one unit of the cryptocurrency.
<br>
<br>
### *Example*

```
[
  {
    "usertoken": "aw7y9djj0ps37nd0"
  },
  {
    "coin": "PEPE"
  }
]
```
<br>

RETURNS
```
[
  {
    "status": {
      "code": "400"
      "description": "Bad Request"
    }
  }
]
```
<br>

## Sell Coin Endpoint
This POST request will sell the user's coin.
```
json?usertoken=USER_TOKEN&coin=COIN
```

- `usertoken` - User token pertaining to User selling the coin
- `coin` - SYMBOL for coin (4 letter stock market name).

Passing a valid user token and a valid coin would sell one unit of the cryptocurrency in the user's wallet.
<br>
<br>
### *Example*

```
[
  {
    "usertoken": "aw7y9djl0ps37nd0"
  },
  {
    "coin": "OSMO"
  }
]
```
<br>

RETURNS
```
[
  {
    "status": {
      "code": "200"
      "description": "OK"
    }
  }
]
```
