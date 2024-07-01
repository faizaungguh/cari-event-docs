## Get All customer

| Method | Path                  | Role     | Params | Auth  |
| ------ | --------------------- | -------- | ------ | ----- |
| GET    | `{BaseUrl}/customers` | customer | -      | token |

Response

```json
{
	"message": "Data customer Loaded",
	"data" : [
		{
			"_id" : {ObjectId}, //string
			"username" : "faizaungguh", //string
			"password" : "rahasia", //string(encrypt)
			"name" : "Faiza Ungguh", //string
			"noKtp" : 3302100300300303, //int
			"imageKtp" : "/path", //string
			"address" : "Kalibagor", //string
			"contact" : "85180180180" //string
		},
		{
			"_id" : {ObjectId}, //string
			"username" : "ungguhf", //string
			"password" : "rahasia", //string(encrypt)
			"name" : "Faiza Ungguh", //string
			"noKtp" : 3302100300300301, //int
			"imageKtp" : "/path", //string
			"address" : "Kalibagor", //string
			"contact" : "85180180180" //string
		},
	],
	"count" : 2,
	"page" : 1,
	"api-name" : "Cari Event API v1"
}
```

## Get customer By Id

| Method | Path                     | Role     | Params | Auth  |
| ------ | ------------------------ | -------- | ------ | ----- |
| GET    | `{BaseUrl}/customer/:id` | customer | id     | token |

Response

```json
{
	"message": "Data customer By ID {id} is Loaded",
	"data" :{
		"_id" : {ObjectId}, //string
		"username" : "faizaungguh", //string
		"password" : "rahasia", //string(encrypt)
		"name" : "Faiza Ungguh", //string
		"noKtp" : 3302100300300303, //int
		"imageKtp" : "/path", //string
		"address" : "Kalibagor", //string
		"contact" : "85180180180" //string
	},
	"api-name" : "Cari Event API v1"
}
```

## Update customer

| Method | Path                     | Role     | Params | Auth  |
| ------ | ------------------------ | -------- | ------ | ----- |
| PATCH  | `{BaseUrl}/customer/:id` | customer | id     | token |

Request Body

```json
{
  "username": "ungguhf", //string
  "password": "yarahasia", //string(encrypt)
  "name": "Ungguh F", //string
  "noKtp": 3302100300300303, //int
  "imageKtp": "/path", //string
  "address": "Kalibagor", //string
  "contact": "85180180180" //string
}
```

Response

```json
{
	"message": "Data customer By ID {id} is Updated",
	"data" :{
		"_id" : {ObjectId}, //string
		"username" : "ungguhf", //string
		"password" : "yarahasia", //string(encrypt)
		"name" : "Ungguh F", //string
		"noKtp" : 3302100300300303, //int
		"imageKtp" : "/path", //string
		"address" : "Kalibagor", //string
		"contact" : "85180180180" //string
	},
	"api-name" : "Cari Event API v1"
}
```

## Delete customer

| Method | Path                     | Role     | Params | Auth  |
| ------ | ------------------------ | -------- | ------ | ----- |
| DELETE | `{BaseUrl}/customer/:id` | customer | id     | token |

Response

```json
{
  "message": "Data customer By ID {id} is Deleted",
  "api-name": "Cari Event API v1"
}
```
