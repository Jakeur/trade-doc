# Sell stock

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
	"price" : 1234
}
```