# Pull index

Get last index from a specific marketplace.
In option, you can request for a specific index (index=Z) and the number of previous values from this index (count=Y) you want to pull.

**URL** : `/group/pull/marketplace_id=X[&count=Y&index=Z]`

**Method** : `GET`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples** : In this example, the Group pulls the last index from the Marketplace ID 4 (crypto currency market : Bitcoin)

```json
{
	"marketplace": "bitcoin",
	"position": 167,
	"value": 8730
}
```

In this example, the Group pulls 3 values (Count parameter) before the Index 112 from the Marketplace ID 3 (raw materiel market : Gold)

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