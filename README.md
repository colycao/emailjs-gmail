A wrapper for [emailjs](https://npmjs.com/package/emailjs)  


## Install  
`$ npm install --save send-gmail`  

## Initialize
```javascript
// initialize to create the `send` function
const { send } = require('send-gmail')(process.env.GMAIL_USERNAME, process.env.GMAIL_PASSWORD);
```

> Note: Less secure app access must be [enabled](https://myaccount.google.com/lesssecureapps) for the Gmail account sending mail.

## Examples
### Simple
```javascript
  // send a message to an email (async)
  send('5555555555@txt.att.net', 'Aloha!', "Google <no-reply@google.com>");
```

### Callback
```javascript
  // send a message to an email (async)
  send('5555555555@txt.att.net', 'Aloha!', function myCallback(err, message) {
    console.log('message sent');
  }, "Google <no-reply@google.com>");
```

### Promise
```javascript
  // send a message to an email (async)
  send('5555555555@txt.att.net', 'Aloha!').then(() => {
    console.log('message sent');
  }, "Google <no-reply@google.com>");
```

### Async/Await
```javascript
(async () => {
  // send a message to an email (async)
  await send('5555555555@txt.att.net', 'Aloha!', "Google <no-reply@google.com>");
})(); 
```
