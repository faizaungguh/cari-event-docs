# Admin Group Endpoint

## Create Admin

| Method | Path                | Role  | Params | Auth  |
| ------ | ------------------- | ----- | ------ | ----- |
| POST   | `{BaseUrl}/admin`   | Admin | id     | token |

Request Body

```json
{
  "username": "ungguhf", //string
  "password": "yarahasia", //string(encrypt)
  "name": "Ungguh F" //string
}
```

Response

```json
{
	"message": "Data Admin By ID {id} is Createds",
	"data" :{
		"_id" : {ObjectId}, //string
		"username" : "ungguhf", //string
		"password" : "yarahasia", //string(encrypt)
		"name" : "Ungguh F" //string
	},
	"api-name" : "Cari Event API v1"
}
```

## Get All Admin

| Method | Path               | Role  | Params | Auth  |
| ------ | ------------------ | ----- | ------ | ----- |
| GET    | `{BaseUrl}/admins` | Admin | -      | token |

Response

```json
{
	"message": "Data Admin Load",
	"data" : [
		{
			"_id" : {ObjectId}, //string
			"username" : "faizaungguh", //string
			"password" : "rahasia", //string(encrypt)
			"name" : "Faiza Ungguh" //string
		},
		{
			"_id" : {ObjectId}, //string
			"username" : "faizaungguh", //string
			"password" : "rahasia", //string(encrypt)
			"name" : "Faiza Ungguh" //string
		},
	],
	"count" : 2,
	"page" : 1,
	"api-name" : "Cari Event API v1"
}
```

## Get Admin By Id

| Method | Path                  | Role  | Params | Auth  |
| ------ | --------------------- | ----- | ------ | ----- |
| GET    | `{BaseUrl}/admin/:id` | Admin | id     | token |

Response

```json
{
	"message": "Data Admin By ID {id} is Loaded",
	"data" :{
		"_id" : {ObjectId}, //string
		"username" : "faizaungguh", //string
		"password" : "rahasia", //string(encrypt)
		"name" : "Faiza Ungguh" //string
	},
	"api-name" : "Cari Event API v1"
}
```

## Update Admin

| Method | Path                  | Role  | Params | Auth  |
| ------ | --------------------- | ----- | ------ | ----- |
| PATCH  | `{BaseUrl}/admin/:id` | Admin | id     | token |

Request Body

```json
{
  "username": "ungguhf", //string
  "password": "yarahasia", //string(encrypt)
  "name": "Ungguh F" //string
}
```

Response

```json
{
	"message": "Data Admin By ID {id} is Updated",
	"data" :{
		"_id" : {ObjectId}, //string
		"username" : "ungguhf", //string
		"password" : "yarahasia", //string(encrypt)
		"name" : "Ungguh F" //string
	},
	"api-name" : "Cari Event API v1"
}
```

## Delete Admin

| Method | Path                  | Role  | Params | Auth  |
| ------ | --------------------- | ----- | ------ | ----- |
| DELETE | `{BaseUrl}/admin/:id` | Admin | id     | token |

Response

```json
{
  "message": "Data Admin By ID {id} is Deleted",
  "api-name": "Cari Event API v1"
}
```
