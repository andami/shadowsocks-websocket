shadowsocks-websocket
===========

shadowsocks-websocket is a lightweight tunnel proxy which can help you get through
 firewalls. It is a port of [shadowsocks](https://github.com/clowwindy/shadowsocks), but
 through a different protocol; shadowsocks-websocket uses WebSockets instead of raw sockets.

Notice that the protocol is INCOMPATIBLE with the origin shadowsocks.

Usage
-----------

~~Use nodejs v0.8.x or v0.6.x, don't use v0.10.x!~~

*Now compatible with nodejs v0.10.x*

Put the code somewhere, for example shadowsocks-websocket/. Edit `shadowsocks/config.json`, change the following values:

    server          your server hostname, for example, your-server.com
    remote_port     remote port, where server listens for clients
    local_port      local port
    password        a password used to encrypt transfer
    timeout         in seconds
    method          encryption method, null by default, or use "rc4"

Upload the code to your server, and run `node server.js`.

On client, open terminal, cd into shadowsocks-websocket, run `node local.js`.

Change proxy settings of your browser into

    SOCKS5 127.0.0.1:local_port
