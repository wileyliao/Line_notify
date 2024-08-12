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

# 如果要在迴圈的每一圈發送訊息，下面兩個需要一起寫在迴圈裡
# 訊息需要根據迴圈設定不同的值(如Loops idenity)
# 若迴圈中訊息都相同，Line Server會視為重複無意義的請求-->而不再發送通知
data = {
    'message': f'Function done!! {Loops idenity}'  # 設定要發送的訊息
}
data = requests.post(url, headers=headers, data=data)
```
