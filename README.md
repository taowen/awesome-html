# awesome-html

collection of "html over the wire" libraries to enable [HATEOAS](https://en.wikipedia.org/wiki/HATEOAS)

## html diff

* https://github.com/patrick-steele-idem/morphdom
* https://github.com/choojs/nanomorph
* https://github.com/Matt-Esch/virtual-dom
* https://github.com/alpinejs/alpine/blob/main/packages/morph/src/morph.js
* https://turbo.hotwired.dev/ (diff manually)

## html diff (native)

react native based

* https://hyperview.org/
* https://meliorence.github.io/react-native-render-html/

react native itself

* ios: https://github.com/facebook/react-native/blob/main/React/Base/RCTRootView.m
* android: https://github.com/facebook/react-native/blob/8adedfeb1581760629edfa48fb2e9b9ffe145bff/ReactAndroid/src/main/java/com/facebook/react/ReactRootView.java
* windows: https://github.com/microsoft/react-native-windows/blob/59df2c597641c9beee3a4eafcb3b880f5e040f6e/vnext/Microsoft.ReactNative/ReactRootView.cpp
* macos: https://github.com/microsoft/react-native-macos/blob/main/React/Base/RCTRootView.m

## event handling

* https://stimulus.hotwired.dev/
* https://htmx.org/
* https://docs.stimulusreflex.com/
* https://alpinejs.dev/
* https://github.com/marko-js-archive/marko-widgets/blob/master/docs/get-started.md
* https://github.com/catberry/catberry
* https://github.com/stimulusreflex/cable_ready
* https://unpoly.com/
* https://kasta-ua.github.io/twinspark-js/
* https://github.com/bplok20010/eval5/issues/15

## server centric

* https://github.com/phoenixframework/phoenix_live_view
* https://github.com/beenotung/ts-liveview

# The Power of UI as "Interface"

API stands for "Application Programming Interface", it is a kind of interface. UI stands for "User Interface", it is also a kind of interface. If we have code running in client and server, the two piece of code talks to each other with API. If we have code running in the server which delivers UI to end user, there is no API in between. This way (also knowns as [HATEOAS](https://en.wikipedia.org/wiki/HATEOAS)) we eliminate the cost to maintain API compatibility with older versions of client.

Integrate two piece of code via API is troublesome. It is always easier to have two piece of code provide its own UI and just concat the two UI blocks together as big UI. This way, they do not need to understand the API of each other, treating the peer as a black box. When requirement change, the integrating interface remain unchanged.

This is the power of UI as "Interface". Html is a special format of UI, which can be server generated, and serialized to render on any private platform (iOS, Android, MiniProgram). The libraries above want to "make html great again" by fixing its problem:

* Html should support incremental update (html over the wire, morph)
* Html should provide native client user experience (toast, flash, navigation, client side animation...)
