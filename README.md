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
