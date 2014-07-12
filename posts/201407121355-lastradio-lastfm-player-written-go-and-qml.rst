.. link: 
.. description: 
.. tags: 
.. date: 2014/07/12 13:55:03
.. title: LastRadio - Last.fm player written Go and QML
.. slug: 201407121355-lastradio-lastfm-player-written-go-and-qml

LastRadio
=========

`LastRadio <https://gitorious.org/lastradio/lastradio>`_ is a simple Last.fm radio player written in `Golang`_ and `QML <http://qt-project.org/doc/qt-5/qtqml-index.html>`_, using Spotify (Premium) as music source.

I've listened a lot to `Last.fm <http://last.fm>`_ radio and I was quite upset as they stopped streaming their radio. Same time I've started getting interested in the `Go Programming Language`_, and stumbling over the `QML bindings for Go <https://github.com/go-qml/qml>`_ led me to the idea to build a simple music player, using the `Last-fm-API <http://www.lastfm.de/api>`_ as data source and `Spotify <http://stotify.com>`_ as music source. Which turned out working just fine!

Doing things in QML is always fun, and having packages written in Go available for both `Last.fm-API <https://github.com/shkh/lastfm-go>`_ and `Libspotify <https://github.com/op/go-libspotify>`_ reduced the work only on getting the UI done and building some logic to get the sound served...

After getting the whole thing packaged as .deb and making it available in a `Lastradio-PPA <https://launchpad.net/~martin-borho/+archive/ubuntu/lastradio>`_, it's now ready to get installed on Ubuntu 14.04! (64-bit only atm, sorry). It's in a"pre-beta" state for now. But having all the things in place, I've started to reiterate over it already. Some nasty quirks left, but LastRadio already served me countless hours with my favourite music, which is exaclty what was intended! :)

I'm impressed by `Golang`_ and it will be not the last time I've used it, I'm especially curious about using it on a server. Its primitives, interfaces, packaging and tools are fun to use. And channels are just a great way to build something on top of the internet! 

.. _Go Programming Language:
.. _Go:
.. _Golang: http://golang.org

