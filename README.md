# 3040Crypto API

Our company, 3040Crypto, should offer API endpoints for any developer to use!

At it's heart, 3040Crypto is a Crypto Wallet service, storing users' Crypto Currencies.  
However, we currently aren't leveraging APIs, and therefore not staying competetively sound.

We should consider adding further functionality via API access for developers.  
Meaning, we create a suite of powerful transactions that enable account changes, purchasing or selling of coin, and more, outside of our application.
Not only would this allow third-party services to incorporate our wallet into their service, increasing our marketshare, but would also mean that the development required to do so would be on someone elses' time.

## Prerequisites
Before a developer can access our API, they must get an `access token` from us, for use in their POST request. This essentially limits the API usage to verified users, bolstering our security.

Furthermore, a user must willingly share their `user token` with the application/service in question. Meaning, developers using the API won't be able to take actions on users behalf, regardless of having a valid `access token` or not.

# API

## Buy Coin
This POST request buys the users coin.
```
json?usertoken=USER_TOKEN&coin=-COIN
```

- `usertoken` - User Token pertaining to User buying the coin
- `coin` - SYMBOL for coin (4 letter stock market name).

### *Example*

```

```
RETURNS
```
```

## Sell Coin
This POST request sells the users coin.
```
json?usertoken=USER_TOKEN&coin=-COIN
```

- `usertoken` - User Token pertaining to User selling the coin
- `coin` - SYMBOL for coin (4 letter stock market name).
### *Example*

```

```
RETURNS
```
```