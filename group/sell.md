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
	"price" : 4200
}
```