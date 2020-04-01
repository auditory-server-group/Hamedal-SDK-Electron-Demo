<p>
  <a href="https://www.npmjs.com/package/@hamedal-falcon"></a>
</p>


<img class="hamedal-logo" width="200px" height="auto" src="https://cdn.shopify.com/s/files/1/0119/8424/0736/files/HAMEDAL_284bd7f1-ddb6-4bb0-b84d-b1ada2af7625_251x.png?v=1568187958" />

# Hamedal Software Development Kit (SDK)

## Prerequisites
Hamedal SDK supportes the following node versions: 

- 13.0.0

Hamedal SDK supportes the following electron versions: 

- 7.2.1

We recommend using nvm as your node version manager [https://github.com/creationix/nvm](https://github.com/creationix/nvm).

After you've setup nvm run
```
  nvm use 13.0.0
```

## Get started
Then you can install and start using the huddly sdk you need first install it and the transport
```
  npm install @hamedal-falcon
```

Start by creating the sdk and the transport

```javascript
var Hamedal = require('hamedal-falcon');

var cameras = Hamedal.devices();

// Create instances of hamedal device you want to use
var falcon = new Hamedal.FalconCamera(cameraInfo);

```
Then you should be good to go. All the actions on the cameraManager are done after the attach event. For example, to change the camera model, call `setAIMode` when the camera is attached.

```javascript

falcon.enableAIMode().then(value => {

  console.log(value);
  
}).catch(reason => {

  console.log(reason);
  
});


```
## Here is demo screenshot image.

<img class="hamedal-demo" width="200px" height="auto" src="https://cdn.shopify.cn/s/files/1/0119/8424/0736/files/2020-04-01_4.49.41.png?v=1585731079" />

## Issues
If you have a question or found a bug please [open an issue](https://github.com/hamedal-sdk/issues). Thank you

