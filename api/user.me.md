# user.me

返回当前用户的信息。

## 请求方式

```
GET {base_url}/user.me
```

## 请求参数

**需要登录**


## 响应

### 200

```javascript
{
  "inactive": false,
  "role": "normal",
  "email": "support@bearyinnovative.com",
  "name": "BearyBot",
  "type": "assistant",
  "created": "2017-01-11T12:28:31.000+0000",
  "id": "=bwMkR",
  "avatars": {
    "small": null,
    "medium": null,
    "large": null
  },
  "team_id": "=bw52O",
  "full_name": "倍洽小助手",
  "mobile": null,
  "profile": {
    "bio": null,
    "position": null,
    "skype": null
  }
}
```
### 错误响应

```javascript
{
  "code": // error code,
  "error": "unexpected error"
}
```

<!-- generated by gen_doc.js -->
