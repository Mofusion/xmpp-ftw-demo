# XMPP-FTW (For The Web/Win)

The goal of this project is to make XMPP really simple to use for developers. This module takes away all of the XML 
and works by hooking to events which are passed between client and server using a transport in JSON. In the example 
code we use socket.io, but there is no reason this can not be replaced with engine.io, or implement your own transport 
and pass in as a connection.

# Try it out...

The code is now up and running at https://xmpp-ftw.jit.su so you can try it out. Be aware that this 
setup is only for trying xmpp-ftw out and may be slow as we need to go client ↔ nodejitsu (east coast US) ↔  your XMPP server and back each time.

* https://xmpp-ftw.jit.su/manual -- XMPP-FTW manual
* https://xmpp-ftw.jit.su/demo -- Awesome demo tool, generated from manual
* <del>https://xmpp-ftw.jit.su/chat</del> -- Old chat client, no longer updated

The version running on the website matches 'master' branch here and auto-deploys with commits.

# Blog posts/Talks

* http://blog.superfeedr.com/easy-xmpp-ftw/
 * XMPP-FTW XMPP and JSON for the Web
* http://www.evilprofessor.co.uk/615-xmpp-ftw-now-supports-superfeedr/
 * XMPP-FTW now supports [SuperFeedr](http://www.superfeedr.com)
* http://www.evilprofessor.co.uk/573-talking-at-the-first-xmppuk-event-march-2013/
 * Talking at the first XMPPUK event (March 2013) 
* http://www.evilprofessor.co.uk/562-new-demo-system-for-xmpp-ftw/
 * How the demo client works
* http://www.evilprofessor.co.uk/579-xmpp-for-the-web-xmpp-ftw/
 * Introduction to XMPP-FTW

# Build status

[![Build Status](https://secure.travis-ci.org/lloydwatkin/xmpp-ftw.png)](http://travis-ci.org/lloydwatkin/xmpp-ftw)

* npm i xmpp-ftw
* Create your socket.io connection manually and then pass this socket into the constructor

```javascript
io.sockets.on('connection', function(socket) {
     new require('xmpp-ftw').Xmpp(socket);       
});
```
* All events are prefixed with 'xmpp.'

For an example of usage and a breakdown of commands simply install ```xmpp-ftw-demo``` 

* `git clone https://github.com/lloydwatkin/xmpp-ftw-demo`
* `npm i .`
* `npm run-script develop`
* Go to http://localhost:3000
* See instructions on the page

Alternatively have a look at the demo client:

* `npm run-script develop`
* Go to `http://localhost:3000/demo`

To work on the code in 'development mode' (where process restarts as files change) run `npm run-script develop`.

# License

License is Apache 2.0, please let me know if this doesn't suit.

# See also...

* Strophe http://strophe.im/
* Stanza.io https://github.com/legastero/stanza.io
