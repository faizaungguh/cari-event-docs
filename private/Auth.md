# Auth Group Endpoint

## Admin

### Login

| Method | Path                   | Role  |
| ------ | ---------------------- | ----- |
| POST   | `{BaseUrl}/auth/admin` | Guest |

Request Body

```json
{
  "username": "faizaungguh", //string
  "password": "rahasia" //string(encrypt)
}
```

Response

```json
{
	"message": "Berhasil Login",
	"data" :{
		"token" : {randomToken} //jWT - payload(id, username)
	},
	"api-name" : "Cari Event API v1"
}
```

## Customer

### Register

| Method | Path                 | Role  |
| ------ | -------------------- | ----- |
| POST   | `{BaseUrl}/customer` | Guest |

Request Body

```json
{
  "username": "faizaungguh", //string
  "password": "rahasia", //string(encrypt)
  "email": "faizaungguh@gmail.com", //string
  "name": "Faiza Ungguh" //string
}
```

Response

```json
{
	"message": "Berhasil Registrasi",
	"data" :{
		"token" : {randomToken} //jWT - payload {id, username}
	},
	"api-name" : "Cari Event API v1"
}
```

### Login

| Method | Path                      | Role  |
| ------ | ------------------------- | ----- |
| POST   | `{BaseUrl}/auth/customer` | Guest |

Request Body

```json
{
  "username": "faizaungguh", //string
  "password": "rahasia" //string(encrypt)
}
```

Response

```json
{
	"message": "Berhasil Login",
	"data" :{
		"token" : {randomToken} //jWT - payload(id, username)
	},
	"api-name" : "Cari Event API v1"
}
```

## Creator

### Register

| Method | Path                | Role  |
| ------ | ------------------- | ----- |
| POST   | `{BaseUrl}/creator` | Guest |

Request Body

```json
{
  "username": "faizaungguh", //string
  "password": "rahasia", //string(encrypt)
  "email": "faizaungguh@gmail.com", //string
  "name": "Faiza Ungguh" //string
}
```

Response

```json
{
	"message": "Berhasil Registrasi",
	"data" :{
		"token" : {randomToken} //jWT - payload(id, username)
	},
	"api-name" : "Cari Event API v1"
}
```

### Login

Request Body

```json
{
  "username": "faizaungguh", //string
  "password": "rahasia" //string(encrypt)
}
```

Response

```json
{
	"message": "Berhasil Login",
	"data" :{
		"token" : {randomToken} //jWT - payload(id, username)
	},
	"api-name" : "Cari Event API v1"
}
```

## Logout

> **Mekanisme**
> Menghapus token yang masih aktif

| Method | Path             | Role                     |
| ------ | ---------------- | ------------------------ |
| DELETE | `{BaseUrl}/auth` | Admin, Creator, Customer |

Response

```json
{
  "message": "Berhasil Logout",
  "api-name": "Cari Event API v1"
}
```
