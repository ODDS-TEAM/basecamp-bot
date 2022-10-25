ขออนุญาตเขียนเป็นภาษาไทยเพื่อให้ทุกคนเข้าถึงได้ง่ายนะครับ

# Basecamp Bot

เนื้องจากบทสนทนาของพวกเราชาว ODDS ส่วนหนึ่งจะอยู่ที่ Basecamp เลยอยากมี Bot ไว้ช่วยเหลือเรื่องต่าง ๆ เช่น จดจำข้อมูลที่ต้องใช้บ่อย ๆ, แจ้งเตือนให้กรอกเงินเดือน เป็นต้น (ดู ideas เพิ่มที่ [README.md](../README.md))

วิธีการส่งข้อความเข้าห้องแชท Campfire ทำได้หลายวิธี

...

[good first issue]

...

## x. ส่งข้อความผ่าน API ของ user

อย่างแรกต้อง Set up Oauth2 เพื่อเอา access token ก่อน https://github.com/basecamp/api/blob/master/sections/authentication.md#oauth-2

*ใช้ ODDS user เพื่อ test ได้เลย รหัสผ่านขอได้ที่ @atb ครับ*

- Register แอปใหม่ที่หน้า https://launchpad.37signals.com/integrations
- กดไปที่แอป แล้วกด Authorization dialog Preview...
- เมื่อ Allow access จะได้ code ติดมากับเว็บ ODDS ไว้ใช้สำหรับขอ access token
- วิธีขอ Access token

  ```sh
  curl -X POST https://launchpad.37signals.com/authorization/token?type=web_server&client_id=your-client-id&redirect_uri=your-redirect-uri&client_secret=your-client-secret&code=verification-code
  ```

- ลองส่งข้อความเข้า Campfire https://github.com/basecamp/bc3-api/blob/master/sections/campfires.md#create-a-campfire-line

  ```sh
  curl -X POST -H 'User-Agent: ODDS (team@odds.team)' \
  -H 'Authorization: Bearer $TOKEN' \
  -H 'Content-Type: application/json' \
  -d '{"content": "This message was sent by a bot 🤖"}' \
  https://3.basecampapi.com/$ACCOUNT_ID/buckets/$BUCKET_ID/chats/$CHAT_ID/lines.json
  ```

  *Url สามารถ copy จาก basecamp บน browser ได้*
