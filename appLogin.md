# appLogin

驗證使用者帳號密碼

### HTTP Request

```
https://114.34.125.246:8090/servlet/HRNative/appLogin
```

### Request body

| Key | Value | Type | Description |
|:----------|:-------------|:-----|:------------|
| request | {"uid:"admin","pwd":"1234"} | Object | 請將帳號密碼組成物件 |


### JSON representation

Here is a JSON representation of request.

```json
{
  "request":{
      "uid":"admin",
      "pwd":"1234"
  }
}
```


### Properties

| Property | Type | Description |
|:---------|:-----|:------------|
| **uid**   | String | 帳號 |
| **pwd** | String | 密碼 |
