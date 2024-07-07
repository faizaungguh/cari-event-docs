## Get All Creator

| Method | Path                | Role    | Params | Auth  |
| ------ | ------------------- | ------- | ------ | ----- |
| GET    | `{BaseUrl}/creator` | creator | -      | token |

Response Body Success :

```json
{
	"message" : "Data creator Loaded",
	"data" : [
		{
			"_id" : {ObjectId},
		    "username" : "creator",
			"creatorName" : "Faiza Organizer",
			"logo" : "/path",
			"contact" : 08888888,
			"penjamin" : {
				"name" : "Ungguh Faizaturrohman",
			}
		},
		{
			"_id" : {ObjectId},
		    "username" : "creator",
			"creator" : "Faiza Organizer",
			"logo" : "/path",
			"contact" : 08888888,
			"penjamin" : {
				"name" : "Ungguh Faizaturrohman",
			}
		},
	],
	"count" : 2,
	"page" : 1,
	"api-info" : "Cari Event API v1"
}
```

## Get Creator By Id

| Method | Path                    | Role    | Params | Auth  |
| ------ | ----------------------- | ------- | ------ | ----- |
| GET    | `{BaseUrl}/creator/:id` | creator | -      | token |

Response

```json
{
	"message" : "Data creator by ID {id} is Loaded",
	"data" : {
		"_id" : {ObjectId}, //string
		"username" : "creator", // string
		"password" : "rahasia", // string(encrypt)
		"creatorName" : "Faiza Organizer", // string
		"logo" : "/path", // string | path file
		"banner" : "/path", // string | path file
		"description" : "deskripsi organizer", // string
		"contact" : 08888888, // number
		"media" : {
			"website" : "http://faiza-organizer.co.id", // string
			"instagram" : "faiza_organizer", // string
			"twitter" : "faiza_organizer", // string
		},
		"address" : {
			"address" : "Jl. Nan keras", // string
			"kecamatan" : "Mantan", // string
			"kabupaten" : "Ngapak", // string
			"postCode" : 55522, // number
		},
		"penjamin" : {
			"name" : "Ungguh Faizaturrohman", // string
			"contact" : 08888888, // number
			"ktp" : "/path", // string | path file | ktp penjamin
		},
		"legal" : {
			"npwp" : "/path", // string | path file | npwp
			"permissionLicense" : "/path", // string | path file | permissionLicense usaha
		}
	},
	"api-info" : "Cari Event API v1"
}
```

## Update Creator By Id

| Method | Path                    | Role    | Params | Auth  |
| ------ | ----------------------- | ------- | ------ | ----- |
| GET    | `{BaseUrl}/creator/:id` | creator | -      | token |

Request Body

```json
{
  "username": "creator", // string
  "password": "rahasia", // string(encrypt)
  "creator": "Faiza Organizer", // string
  "logo": "/path", // string | path file
  "banner": "/path", // string | path file
  "description": "deskripsi organizer", // string
  "contact": 08888888, // number
  "media": {
    "website": "http://faiza-organizer.co.id", // string
    "instagram": "faiza_organizer", // string
    "twitter": "faiza_organizer" // string
  },
  "address": {
    "address": "Jl. Nan keras", // string
    "kecamatan": "Mantan", // string
    "kabupaten": "Ngapak", // string
    "postCode": 55522 // number
  },
  "penjamin": {
    "name": "Ungguh Faizaturrohman", // string
    "contact": 08888888, // number
    "ktp": "/path" // string | path file | ktp penjamin
  },
  "legal": {
    "npwp": "/path", // string | path file | npwp
    "permissionLicense": "/path" // string | path file | permissionLicense usaha
  }
}
```

Response

```json
{
	"message" : "Data Creator By ID {id} is Updated",
	"data" : {
		"_id" : {ObjectId}, //string
		"username" : "creator", // string
		"password" : "rahasia", // string(encrypt)
		"creator" : "Faiza Organizer", // string
		"logo" : "/path", // string | path file
		"banner" : "/path", // string | path file
		"description" : "deskripsi organizer", // string
		"contact" : 08888888, // number
		"media" : {
			"website" : "http://faiza-organizer.co.id", // string
			"instagram" : "faiza_organizer", // string
			"twitter" : "faiza_organizer", // string
		},
		"address" : {
			"address" : "Jl. Nan keras", // string
			"kecamatan" : "Mantan", // string
			"kabupaten" : "Ngapak", // string
			"postCode" : 55522, // number
		},
		"penjamin" : {
			"name" : "Ungguh Faizaturrohman", // string
			"contact" : 08888888, // number
			"ktp" : "/path", // string | path file | ktp penjamin
		},
		"legal" : {
			"npwp" : "/path", // string | path file | npwp
			"permissionLicense" : "/path", // string | path file | permissionLicense usaha
		}
	},
	"api-info" : "Cari Event API v1"
}
```

## Delete Creator By Id

| Method | Path                     | Role     | Params | Auth  |
| ------ | ------------------------ | -------- | ------ | ----- |
| DELETE | `{BaseUrl}/customer/:id` | customer | id     | token |

Response

```json
{
  "message": "Data Creators By ID {id} is Deleted",
  "api-info": "Cari Event API v1"
}
```
