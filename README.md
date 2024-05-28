Working on NODE.js only

import { SimpleHttpClient, SimpleHttpRequest } from '@scdb/simple-http';

const httpClient = new SimpleHttpClient(
  new SimpleHttpRequest('https://api.myip.com/')
);

httpClient.get().then((res) => {
  res.res.on('data', (d) => console.log(d.toString()));
});
