# Welcome

You will find below all requests you can call.

Before the event, the server will reset each week, every Sunday on 11:42 pm.
During this period, if you find any bug or if the server crashes, we will do our best to fix everything. Feel free to contact : rodolphe1.assere@epitech.eu.

For the event, the server will be reset at the beginning.

Parameters at the beginning :
* Money : 10 000 euros
* Delay between 2 requests : 5 seconds
* Kick-out duration : 10 minutes

Don't spam the server or you will be kicked out.

Marketplace IDs :
* 1 : Crypto-currency
* 2 : Raw materials
* 3 : Stock exchange
* 4 : Forex
* 5 : EPITECH (based on transactions done on 4 others marketplace)

## Login

Use Office365 login

* [Login](login.md) : `GET /login/`
* [Reset Token](reset_token.md) : `GET /reset_token/`

## Trading requests

Get indexes and buy/sell shares depending on your prediction

* [Pull Index](group/pull.md) : `GET /group/pull/`
* [Sell Shares](group/sell.md) : `GET /group/sell/`
* [Buy Shares](group/buy.md) : `GET /group/buy/`

\pagebreak

# Login

Login in Office365 platform.

**URL** : `/login`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Details** : When you are logged successfully, you will find your token on the provided light client.

\pagebreak

# Reset Token

Reset your token when you are logged.

**URL** : `/reset_token`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content example** In this example, you will get a new token

```json
{
    "token": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d"
}
```

\pagebreak

# Pull index

Get last index from a specific marketplace.
In option, you can request for a specific index (index=Z) and the number of previous values from this index (count=Y) you want to pull.

**URL** : `/group/pull/marketplace_id=X[&count=Y&index=Z]`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples** : In this example, the Group pulls the last index from the Marketplace ID 1 (crypto currency market : Bitcoin)
* marketplace_id=1

```json
{
	"marketplace": "bitcoin",
	"position": 167,
	"value": 8730.0
}
```

In this example, the Group pulls 3 values (Count parameter) before the Index 112 from the Marketplace ID 2 (raw materiel market : Gold)
* marketplace_id=2
* count=3
* index=112

```json
[
	{
		"marketplace": "gold",
		"position": 110,
		"value": 130.3
	},
		{
		"marketplace": "gold",
		"position": 111,
		"value": 112.4
	},
		{
		"marketplace": "gold",
		"position": 112,
		"value": 131.9
	}
]
```

\pagebreak

# Buy stock

Buy stocks from a marketplace

**URL** : `/group/buy/marketplace_id=X&quantity=Y`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content** : In this example, the Group buys 8 shares in the Marketplace ID 2. The price of each bought share is 1234 euros

```json
{
	"group": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d" ,
	"marketplace": 2,
	"action": "BUY",
	"quantity": 8,
	"price" : 1234.9
}
```

\pagebreak

# Sell stock

Sell stocks to a marketplace

**URL** : `/group/sell/marketplace_id=X&quantity=Y`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content** : In this example, the Group sells 10 shares in the Marketplace ID 3. The price of each sold share is 4200 euros

```json
{
	"group": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d" ,
	"marketplace": 3,
	"action": "SELL",
	"quantity": 10,
	"price" : 4200.3
}
```
