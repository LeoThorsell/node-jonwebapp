# Simple http router with app abstraction
Seaport, bouncy, express...


## Example
In this example, assume we have *.example.com to our server.

Router:
```javascript
var webapp = require('jonwebapp');
var server = webapp.server({httpPort: 80});
server.on('log', (msg) => {
	console.log(msg);
});
```

Application (app1.example.com):
```javascript
var webapp = require('jobwebapp');

// 'app1' is the subdomain we want our app to use. 
// app is an express instance
var app = webapp('app1');

app.get('*', (req, res) => res.end('Hi!\n'));
```

