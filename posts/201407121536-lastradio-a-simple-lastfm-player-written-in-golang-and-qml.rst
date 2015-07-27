.. link: 
.. description: 
.. tags: go, golang, last.fm, spotify
.. date: 2014/07/12 15:36:17
.. title: LastRadio - a simple Last.fm player written in Golang and QML
.. slug: 201407121536-lastradio-a-simple-lastfm-player-written-in-golang-and-qml

`LastRadio <https://github.com/mborho/lastradio>`_ is a simple
Last.fm radio player written in `Golang`_ and `QML
<http://qt-project.org/doc/qt-5/qtqml-index.html>`_, using Spotify
(Premium) as music source.

.. image:: /images/lastradio3.png

I've listened a lot to `Last.fm <http://last.fm>`_ radio and I was quite
upset as they stopped their streaming service. Same time I've started
getting interested in the `Go Programming Language`_, and stumbling over
the `QML bindings for Go <https://github.com/go-qml/qml>`_ led me to the
idea to build a simple music player, using the `Last-fm-API
<http://www.lastfm.de/api>`_ as data source and `Spotify
<http://stotify.com>`_ as music source. Which turned out working just fine!

Doing things in QML is always fun, and having packages written in Go
available for both `Last.fm-API <https://github.com/shkh/lastfm-go>`_
and `Libspotify <https://github.com/op/go-libspotify>`_ reduced the work
only on getting the UI done and building some logic to get the sound
served...

After getting the whole thing packaged as .deb and making it available
in a `Lastradio-PPA
<https://launchpad.net/~martin-borho/+archive/ubuntu/lastradio>`_, it's
now ready to get installed on Ubuntu 14.04! (64-bit-desktop only atm, sorry).

::

    sudo add-apt-repository ppa:martin-borho/lastradio
    sudo apt-get update
    sudo apt-get install lastradio

It's in a"pre-beta" state for now. But having all the things in place,
I've started to reiterate over it already. Some nasty quirks left, but
it already served me countless hours with my favourite music, which is
exactly what was intended! 

So overall I'm impressed by `Go`_ and it will be not the last time I've used
it, I'm especially curious about using it on a server. Its primitives,
interfaces, packaging and tools are fun to use. And channels and goroutines are just a
great way to build something on top of the internet!

Sourcecode: https://github.com/mborho/lastradio

PPA: https://launchpad.net/~martin-borho/+archive/ubuntu/lastradio

.. _Go Programming Language:
.. _Go:
.. _Golang: http://golang.org

