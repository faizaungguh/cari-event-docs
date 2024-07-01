## Create Event

| Method | Path              | Role    | Params             | Auth |
| ------ | ----------------- | ------- | ------------------ | ---- |
| POST   | `{BaseUrl}/event` | Creator | idCreator, creator | -    |

Request

```json
{
	"title" : "Konser Tunggal Fajar SadBoy 2024",
	"banner" : "/path",
	"description" : "Ini deskripsi konser",
	"detail" : "Ini detail konser",
	"ticket" : [
		{
			"category" : "gold",
			"price" : 15000
		},
		{
			"category" : "silver",
			"price" : 10000
		},
		{
			"category" : "bronze",
			"price" : 5000
		},
	],
	"dateHeld" : Date,
	"dateEnd" : Date,
	"Time" : Time,
	"category" : {
		"title" : "Konser"
	},
	"contact" : 0888888888,
	"location" : {
		"address" : "Jl. Nan keras", // string
		"kecamatan" : "Mantan", // string
		"kabupaten" : "Ngapak", // string
		"postCode" : 55522, // number
	},
}
```

Response

```json
{
	"message" : "Data Event Created",
	"data" : {
		"_id" : {ObjectId},
		"title" : "Konser Tunggal Fajar SadBoy 2024",
		"description" : "Ini deskripsi konser",
		"detail" : "Ini detail konser",
		"ticket" : [
			{
				"ticketId" : {ObjectId},
				"category" : "gold",
				"price" : 15000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "silver",
				"price" : 10000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "bronze",
				"price" : 5000
			},
		],
		"dateHeld" : Date,
		"dateEnd" : Date,
		"Time" : Time,
		"category" : {
			"idCategory" : {ObjectId},
			"title" : "Konser"
		},
		"contact" : 0888888888,
		"location" : {
			"address" : "Jl. Nan keras", // string
			"kecamatan" : "Mantan", // string
			"kabupaten" : "Ngapak", // string
			"postCode" : 55522, // number
		},
		"creator" : {
			"creatorId" : {ObjectId},
			"creatorName" : "Faizaungguh Organizer",
			"logo" : "/path"
		}
	},
	"api-name" : "Cari Event API v1"
}
```

## Get All Event

| Method | Path               | Role | Params | Auth |
| ------ | ------------------ | ---- | ------ | ---- |
| GET    | `{BaseUrl}/events` | All  | -      | -    |

Response

```json
{
	"message" : "Data Event Loaded",
	"data" : [
		{
			"_id" : {ObjectId},
			"banner" : "/path",
			"title" : "Konser Tunggal Fajar SadBoy 2024",
			"dateHeld" : Date,
			"price" : {lowerPrice},
		},
	],
	"count" : 2,
	"page" : 1,
	"api-name" : "Cari Event API v1"
}
```

## Get Event By Id

| Method | Path                  | Role    | Params | Auth |
| ------ | --------------------- | ------- | ------ | ---- |
| GET    | `{BaseUrl}/event/:id` | Creator |        | -    |

Response

```json
{
	"message" : "Data Event By Id {id} is Loaded",
	"data" : {
		"_id" : {ObjectId},
		"title" : "Konser Tunggal Fajar SadBoy 2024",
		"description" : "Ini deskripsi konser",
		"detail" : "Ini detail konser",
		"ticket" : [
			{
				"ticketId" : {ObjectId},
				"category" : "gold",
				"price" : 15000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "silver",
				"price" : 10000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "bronze",
				"price" : 5000
			},
		],
		"dateHeld" : Date,
		"dateEnd" : Date,
		"Time" : Time,
		"category" : {
			"idCategory" : {ObjectId},
			"title" : "Konser"
		},
		"contact" : 0888888888,
		"location" : {
			"address" : "Jl. Nan keras", // string
			"kecamatan" : "Mantan", // string
			"kabupaten" : "Ngapak", // string
			"postCode" : 55522, // number
		},
		"creator" : {
			"creatorId" : {ObjectId},
			"creatorName" : "Faizaungguh Organizer",
			"logo" : "/path"
		}
	},
	"api-name" : "Cari Event API v1"
}
```

## Update Event

| Method | Path                  | Role    | Params | Auth |
| ------ | --------------------- | ------- | ------ | ---- |
| GET    | `{BaseUrl}/event/:id` | Creator |        | -    |

Request Body

```json
{
	"title" : "Konser Tunggal Fajar SadBoy 2024",
	"banner" : "/path",
	"description" : "Ini deskripsi konser",
	"detail" : "Ini detail konser",
	"ticket" : [
		{
			"category" : "gold",
			"price" : 15000
		},
		{
			"category" : "silver",
			"price" : 10000
		},
		{
			"category" : "bronze",
			"price" : 5000
		},
	],
	"dateHeld" : Date,
	"dateEnd" : Date,
	"Time" : Time,
	"category" : {
		"title" : "Konser"
	},
	"contact" : 0888888888,
	"location" : {
		"address" : "Jl. Nan keras", // string
		"kecamatan" : "Mantan", // string
		"kabupaten" : "Ngapak", // string
		"postCode" : 55522, // number
	},
}
```

Response

```json
{
	"message" : "Data Event By Id {id} is Updated",
	"data" : {
		"_id" : {ObjectId},
		"title" : "Konser Tunggal Fajar SadBoy 2024",
		"description" : "Ini deskripsi konser",
		"detail" : "Ini detail konser",
		"ticket" : [
			{
				"ticketId" : {ObjectId},
				"category" : "gold",
				"price" : 15000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "silver",
				"price" : 10000
			},
			{
				"ticketId" : {ObjectId},
				"category" : "bronze",
				"price" : 5000
			},
		],
		"dateHeld" : Date,
		"dateEnd" : Date,
		"Time" : Time,
		"category" : {
			"idCategory" : {ObjectId},
			"title" : "Konser"
		},
		"contact" : 0888888888,
		"location" : {
			"address" : "Jl. Nan keras", // string
			"kecamatan" : "Mantan", // string
			"kabupaten" : "Ngapak", // string
			"postCode" : 55522, // number
		},
		"creator" : {
			"creatorId" : {ObjectId},
			"creatorName" : "Faizaungguh Organizer",
			"logo" : "/path"
		}
	},
	"api-name" : "Cari Event API v1"
}
```

## Delete Event

| Method | Path                  | Role     | Params | Auth  |
| ------ | --------------------- | -------- | ------ | ----- |
| DELETE | `{BaseUrl}/event/:id` | customer | id     | token |

Response

```json
{
  "message": "Data Event By ID {id} is Deleted",
  "api-name": "Cari Event API v1"
}
```
