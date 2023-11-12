# Webhook Layanan WhatsAuth
WebHook Menggunakan method HTTP POST dengan Header bernama Secret  
![image] 
Format JSON dalam body yang dikirim ke WebHook :  
![image]
Lengkapnya :
```json
{
  "phone_number": "1234567890",
  "reply_phone_number": "0987654321",
  "chat_number": "1122334455",
  "chat_server": "server1.chat.example",
  "group_name": "Example Group",
  "group_id": "G-123456",
  "group": "yes",
  "alias_name": "JohnDoe",
  "messages": "This is a test message",
  "from_link": true,
  "from_link_delay": 30,
  "is_group": true,
  "filename": "document.pdf",
  "filedata": "base64EncodedString",
  "latitude": 37.7749,
  "longitude": -122.4194,
  "liveloc": true
}
```

## Contoh Source Code WebHook
Berikut ini adalah contoh source code webhook
1. [Untuk Go di Google Cloud Funtion](./gcf)
2. [Untuk PHP di Web Hosting](./hosting)

## Release Package
```sh
go get -u all					#update existing package
go mod tidy					#generate go mod
git tag                                 	#check current version
git tag v0.0.3                          	#set tag version
git push origin --tags                  	#push tag version to repo
go list -m github.com/whatsauth/webhook@v0.0.3   #publish to pkg dev, replace ORG/URL with your repo URL
```
