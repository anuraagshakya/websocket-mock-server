A simple and configurable mock server with UI console for websocket, with which you can either send message manually or make rules to get matched response. Err... It's hard to summarize, Let's take a look!

# Installation

## [npm package](https://www.npmjs.com/package/websocket-mock-server)

```
npm install websocket-mock-server
```

## [github repo](git@github.com:anuraagshakya/websocket-mock-server.git)

```
git clone git@github.com:anuraagshakya/websocket-mock-server.git
```

You may need to install npm and type script.

Install npm:
```
brew install npm
```

Install typescript:
```
npm install -g typescript 
```

Preparation:
```
npm install
npm run build
```

Run:
```
npm run test
```

# Configuration

package.json
```json
{
  "script": {
    "mock": "wsmock -c CONFIG_PATH"
  }
}
```

The following config.js will be used and watched as default config when no `CONFIG_PATH` is provided.
```javascript
module.exports = {
  port: 4040,
  // a function exported to handle specific input and return output which will be sending later.
  rule: function (input) {}
  // set the delay time before sending auto message 
  autoMsgTimeout: 1000,
};
```

# Run - default configurations

```
npm run test
```

# Run


Terminal
```
npm run mock
```

![preview](./public/img/preview.png)

The frontend provide a chatroom-like way for you to send WebSocket message to server, which will be broadcast to other clients.


# TODO

- [ ] feat: Serial message flow test; 
