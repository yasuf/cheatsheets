## Run a logging local server with node

1. Create a new project folder and cd into it: `mkdir my_project && cd my_project`.

2. Run `npm init` in the new folder.

3. Run `npm install --save morgan express`.

4. Create an `index.js` file with this:

```js
//index.js file 
const express = require('express')
const morgan = require('morgan')
const bodyParser = require('body-parser');
const app = express()
const port = 5000

app.use(morgan('tiny'));
app.use(bodyParser.urlencoded({ extended: false }));
app.use(bodyParser.json());

app.get('/*', (req, res) => {
  res.status(200);
  res.send({ success: true });
})

app.post('/*', (req, res) => {
  res.status(200);
  console.log(req.body);
  res.send(req.body);
})

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})

```

5. Run the server with `node index.js`.

6. Run ngrok locally and make sure it points to `localhost:5000` like it usually does, if not modify the port in `index.js` so that it matches ngrok
