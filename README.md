# GUPSHUP-ACCESS-API:

```
const request1 = require('request');
 function callBackUrl(request, response) {
    /* Here we are getting: 
       request.method,
       request.body(msg info.)
       and request.headers 
    */
    r.send("Response from call back url ")
    const options = {
      'method': 'POST',
      'url': 'https://api.gupshup.io/sm/api/v1/msg',
      'headers': {
        'Cache-Control': 'no-cache',
        'Content-Type': 'application/x-www-form-urlencoded',
        'apikey': 'e7b49xxxxxxxxxxxxxdc26ecf39a',
        // 'User-Agent': 'PostmanRuntime/7.23.0',
        // 'Accept': '*/*',
        // 'Postman-Token': 'ab146903-xxxxxxxxxxx885c81d8abbb',
        // 'Host': 'api.gupshup.io',
        // 'Accept-Encoding': 'gzip, deflate, br',
        // 'Content-Length': '209',
        // 'Connection': 'keep-alive'
      },
      form: {
        'channel': 'whatsapp',
        'source': '917834811114 ',
        'destination': '918003555725',
        'src.name\n': 'TestingRamandAward',
        'message': 'Response from message api',
        // 'message.payload.isHSM': 'true',
        // 'message.payload.type': 'text',
        // 'message.payload.text': 'yes, template message'
      }
    }
    request1(options, function (error: any, response: any) { 
      console.log("Body : " + response.body);
      if (response.statusCode == 200) {
        // msg has been sent the destination number
        //here put what you want to do with the request
      }
      if (error) {
        console.log(error)
      }
    }
  }
```
[whatsapp-api-documentation](https://www.gupshup.io/developer/docs/bot-platform/guide/whatsapp-api-documentation)

[How does session messaging and template messaging work in Access API?](https://www.gupshup.io/developer/faq/whatsapp)
