[![NPM](https://nodei.co/npm/boats.js.png?downloads=true&downloadRank=true&stars=true)](https://nodei.co/npm/boats.js)

# Boats.js
The official https://discord.boats API wrapper for Node.js

## Installation
Simply run `npm i boats.js` (or `yarn add boats.js`)

## Usage
Posting Bot Server Count:
```js
const BoatsClient = require('boats.js');
const Boats = new BoatsClient('API TOKEN', 'API VERSION (optional, either "v1" or "v2")'));

Boats.postStats(SERVER_COUNT, 'BOT_ID').then(() => {
    console.log('Successfully updated server count.');
}).catch(err => {
    console.error(err);
});
```

Getting Bot Info:
```js
const BoatsClient = require('boats.js');
const Boats = new BoatsClient('API TOKEN');

Boats.getBot('BOT_ID').then(bot => {
    console.log(bot);
}).catch(err => {
    console.error(err);
});
```

Getting User Info:
```js
const BoatsClient = require('boats.js');
const Boats = new BoatsClient();

Boats.getUser('USER_ID').then(user => {
    console.log(user);
}).catch(err => {
    console.error(err);
});
```

Checking if a user voted your bot:
```js
const BoatsClient = require('boats.js');
const Boats = new BoatsClient('API TOKEN');

Boats.getVoted('BOT_ID', 'USER_ID').then(voted => {
    console.log(voted);
}).catch(err => {
    console.error(err);
});
```

## License
[MIT](LICENSE)
