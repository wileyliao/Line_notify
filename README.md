# Line_notify
Sending Line notification in the specific point of programs

## Steps:
- Search Line Notify
- loggin(upper right corner)
- Personal page (upper right corner)
- click 發行權杖 (Get access token)

## Code:
```python
import requests
url = 'https://notify-api.line.me/api/notify'
token = 'Access token'
headers = {
    'Authorization': 'Bearer ' + token    # 設定權杖
}

data = {
    'message': f'HS_DESK done!! {filename}'  # 設定要發送的訊息
}
data = requests.post(url, headers=headers, data=data)
```
