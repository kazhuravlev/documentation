# Install and quick start

The simplest way to use javascript client is including it into your web page using `script` tag:

```html
<script src="centrifuge.js"></script>
```

Javascript client built on top of [Event Emitter](https://github.com/Wolfy87/EventEmitter)
by [Oliver Caldwell](https://github.com/Wolfy87).

Centrifuge-js is also available via `npm` and `bower` so you can use:

```bash
npm install centrifuge
```

Or:

```bash
bower install centrifuge
```

**Note** that if you want to use SockJS you must import it on your page before Centrifuge
javascript client:

```html
<script src="//cdn.jsdelivr.net/sockjs/1.0/sockjs.min.js" type="text/javascript"></script>
<script src="centrifuge.js" type="text/javascript"></script>
```

**If you are planning to support Internet Explorer < 8** then you also need to include
JSON polyfill library:

```html
<script src="//cdnjs.cloudflare.com/ajax/libs/json3/3.3.2/json3.min.js" type="text/javascript"></script>
<script src="//cdn.jsdelivr.net/sockjs/1.0/sockjs.min.js" type="text/javascript"></script>
<script src="centrifuge.js" type="text/javascript"></script>
```

First you need to create new centrifuge object instance:

```javascript
<script type="text/javascript">

    var centrifuge = new Centrifuge({
        url: 'http://centrifuge.example.com/connection',
        user: 'USER ID',
        timestamp: 'TIMESTAMP',
        token: 'TOKEN'
    });

</script>
```

And you are ready to connect to Centrifugo server calling `connect()` method:

```
<script type="text/javascript">
    // ... create centrifuge object as shown above

    centrifuge.connect();
</script>
```

In next section we will talk about all these configuration options in detail.