# CODE-EXP-2022-backend

Backend server for our CODE_EXP application

## Base URL

```
https://code-exp-2022.herokuapp.com
```

## Admin

### URL
```
GET /admin
```

### Request

Query Parameters
- `pw` - Password to access admin site (Ask ._.#6830 on discord for it)

### Response

```
{
    "tables": [table_name],
    "table_name": [
        {
            "user_username": "username",
            "title": "title",
            "description": "description",
            "backgroundcolor": "FFFFFF",
            "bordercolor": "000000",
            "startdate": "2022-01-01T00:00:00.000Z",
            "enddate": "2022-01-01T12:00:00.000Z",
        }, ...
    ]
}
```

## Login

### URL

```
POST /login
```

### Request

Body
```
{
    "username": username,
    "password": password,
}
```

### Response

```
200 - Login success
401 - Login failed
```

## Register

### URL
```
POST /register
```

### Request

Body
```
{
    "username": username,
    "password": password,
    "pfp": path-to-pfp,
    "platoon": platoon,
}
```

### Response

```
201 - Registration successful
```

## Events

### URL
```
GET /events
```

### Request

Body
```
{
    "username": username,
    "password": password,
}
```

### Response

```
[
    {
        "user_username": "username",
        "title": "title",
        "description": "description",
        "backgroundcolor": "FFFFFF",
        "bordercolor": "000000",
        "startdate": "2022-01-01T00:00:00.000Z",
        "enddate": "2022-01-01T12:00:00.000Z"
    }, ...
]
```

### URL

```
POST /events
```

### Request

Body
```
{
    "username": username,
    "password": password,
    "body": {
        "user_username": "username",
        "title": "title",
        "description": "description",
        "backgroundcolor": "FFFFFF",
        "bordercolor": "000000",
        "startdate": "2022-01-01T00:00:00.000Z",
        "enddate": "2022-01-01T12:00:00.000Z",
    },
}
```

### Response

```
201 - Event created
```