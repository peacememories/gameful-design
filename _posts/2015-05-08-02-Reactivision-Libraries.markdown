---
layout: post
title: Reactivision Libraries
category: assignments
comments: true
---

Since we wanted do write an application in haskell, we kind of have to write all the Reactivision libraries ourselves. So here goes:

#TUIO

[TUIO](http://www.tuio.org/?specification) is the protocol used to communicate between the Reactivision tracker and any applications using the input device. All Reactivision apps are therefore also TUIO clients

A starting point for the TUIO haskell library is set up [here](https://github.com/peacememories/tuio-haskell).

#OSC

TUIO is based on the Open Sound Protocol ([OSC](http://opensoundcontrol.org/spec-1_0)).
There is an [existing library](http://hackage.haskell.org/package/hosc) for this protocol, but we ran into some issues with the parser, so we decided to roll our own.

[osc-haskell](https://github.com/peacememories/haskell-osc) is basically ready for use. For now it only features a parser (based on [attoparsec](http://hackage.haskell.org/package/attoparsec)), but I am working on a printer, too. There also isn't any real documentation there yet, which I will remedy as soon as i can manage.

Most of you will probably run with processing, but if any of you want to use these libraries, feel free to do so, and also please submit bug reports if you run into issues.

Happy coding.