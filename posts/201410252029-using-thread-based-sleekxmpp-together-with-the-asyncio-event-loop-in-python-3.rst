.. link: 
.. description: 
.. tags: coding, python, asyncio, xmpp 
.. date: 2014/10/25 20:29:04
.. title: Using thread-based SleekXMPP together with the asyncio event loop in Python 3
.. slug: 201410252029-using-thread-based-sleekxmpp-together-with-the-asyncio-event-loop-in-python-3

Some months ago I've started to migrate my `push-based feed/twitter reader <https://github.com/mborho/silozippr>`_ from Node.js to Python3. As I also wanted to have integration of `Superfeedr <https://superfeedr.com>`_ and their `XMPP PubSub <http://documentation.superfeedr.com/subscribers.html#xmpp-pubsub>`_ service, a XMPP module was needed which would play nicely with the new `asyncio <https://docs.python.org/3/library/asyncio.html#module-asyncio>`_ module of Python3.

Problem:  `SleekXMPP <https://github.com/fritzy/SleekXMPP>`_ had support of all needed plugins, but is thread-based. Which isn't good, if you want to build your app in an asynchronous manner with the asyncio event loop.

Fortunately asyncio gives the possibility to run threads in an `Executor <https://docs.python.org/3/library/asyncio-eventloop.html#executor>`_, which I did.

In hope, somebody might find this helpfull,  I've rewritten the EchoBot-Example of SleekXMPP, running now in an asyncio executor. As you can see (`gist here <https://gist.github.com/mborho/55be89eead0b0e19e051>`_), the main thread with the event loop and the XMPP client, running in an executor, are communicating over a queue. So you can use your XMPP client not only for receiving messages, but also for sending. With the possibility to do work in the event loop! 

.. gist:: 55be89eead0b0e19e051


