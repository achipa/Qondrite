#Qondrite

A QML wrapper for [Asteroid](http://github.com/modora/asteroid), a 
javascript client (browser and node) for a Meteor backend.

##Table of contents

[Why](#why)

[Install](#install)

[Example usage](#example-usage)

##Why

Meteor is an awesome platform, but its canonical
front-end is not very flexible. Asteroid gives the
possibility to connect to a Meteor backend with any JS app.
Qondrite in turn makes this possible to do in any QML app.

[Blog post on the library](http://mondora.com/#!/post/e2da7bd7ccb774de13324488b4e24abd)

##Background and Demo

!VIDEO https://www.youtube.com/watch?v=A9KqDrqYRsc

##Install

Dependencies (installed as git subtrees)

q.js from https://github.com/achipa/q/blob/v1/q.js

asteroid from https://github.com/achipa/asteroid/blob/master/dist/asteroid.qml.js

ddp.js from https://github.com/achipa/ddp.js/blob/master/src/ddp.js

JSONListModel from https://github.com/achipa/qml-utils/blob/master/JSONListModel/JSONListModel.qml

Log.js from https://github.com/krnekit/qml-utils/blob/master/qml/Log.js

##Example-usage

Use Qondrite.qml as follows:

    Qondrite {
        id: asteroid
        meteor_url: "localhost:3000"
        onOpen: statusText = "Connection to " + url + " established";
        onClose: statusText = "Connection closed";
        onError: statusText = "Error: " + errorString;
    }

Example self-contained Qt project using Qondrite:

https://github.com/achipa/outqross_blog/tree/master/3_OutQross.Meteor_demo

