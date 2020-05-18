# Stream Share

Play synchronized content across multiple clients.

Uses python to create a web server that clients can connect to and receive events to play streaming content.

# Setup the server

* open port 1564 on your server's firewall
* if you're in a private network, forward port 1564 to your server
* run `./server` on your server, uses python3 and logs to stdout

> NOTE: I've seen issues with YouTube when clients connect to the server via an IP address instead of a host name.  It will sometimes say "Video Not Available".  I'm not sure why this happens, it's weird.  However, I have not seen this issue since I started using the iframe_api so it may not be an issue any longer, not sure.

# Clients

Once the server is started, clients can connect to it via their webrowser.  The default page will serve up a page for a client that receives stream events.  Connect to the `controller.html` page to be able to send streaming events to others.

# Feature Ideas

* have streaming clients report back their status, their timestamp, play/pause, volume, connected.  This data can be aggregated and sent to the controller page so they can see what's going on.
* support simple chat messages?
* allow controller to copy/paste full video links (not just youtube video id)
* allow controller to specify timestamp

# Issues

* Android/IPhones don't allow videos to play without the user clicking "play" (i.e. via JavaScript).

# License

This software is released under the https://en.wikipedia.org/wiki/WTFPL license.
