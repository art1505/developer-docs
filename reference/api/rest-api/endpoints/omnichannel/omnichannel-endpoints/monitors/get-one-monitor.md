---
description: Gives the details of a monitor
---

# Get one Monitor

![](../../../../../../../.gitbook/assets/enterprise.jpg)

{% hint style="warning" %}
![](../../../../../../../.gitbook/assets/Deprecated.png) This endpoint has been renamed to [get-a-monitor.md](get-a-monitor.md "mention") as from Rocket.Chat `5.0`
{% endhint %}

| URL                               | Requires Auth | HTTP Method |
| --------------------------------- | ------------- | ----------- |
| `api/v1/livechat/monitors.getOne` | `YES`         | `GET`       |

## Headers

| Argument       | Example        | Required | Description                                                    |
| -------------- | -------------- | -------- | -------------------------------------------------------------- |
| `X-User-Id`    | `myuser-name`  | Required | Your username hash (returned after you log in through the API) |
| `X-Auth-Token` | `myauth-token` | Required | Your token (returned after you log in through the API)         |

## Parameters

| Argument   | Example       | Required | Description |
| ---------- | ------------- | -------- | ----------- |
| `username` | `Bruno.Solis` | Required | Username    |

## Example Call

```bash
curl --location --request GET 'http://localhost:3000/api/v1/llivechat/monitors.getOne?username=Bruno.Solis \
--header 'X-Auth-Token: myauth-token' \
--header 'X-User-Id: myuser-name'
```

## Result

```javascript
{
    "_id": "gxcJTYapi5mPxuAme",
    "username": "Bruno.Solis",
    "emails": [
        {
            "address": "",
            "verified": false
        }
    ],
    "status": "offline",
    "name": "Bruno Solis",
    "statusLivechat": "not-available",
    "success": true
}
```
