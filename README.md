## Bluetooth Battery Monitor

There are two primary motivations for this project:

* My Magic Mouse 2 goes dead without me ever having seen a notification. On the same Mac, my Magic Mouse (the original model with AA batteries) _did_ give me notifications when the batteries needed to be changed, so I don't know if it's due to differences in the driver software or the OS upgrade to Mojave. Either way, it sucks.
* I figured this would be a good oportunity to finally do something meaty in XCode, and in Swift to boot. I've been using XCode command-line tools for C/C++ development forever, but they're pretty much like the tools on every other platform, so I decided to try doing some serious work in the IDE.

#### Background

I've long avoided XCode development, in part because I just can't stomach the Objective-C syntax.
Several years back I actually wrote a bunch of C++ wrapping the OS X APIs to make them tolerable, but just never had the motivation to do much more with the library.

Fast-forward to the present, and Swift is far more tolerable (to me) than Objective-C.
Sure, it's got some nits that just seem stupid to me (no parameterization of Protocols - WTF, Apple?), and I'd gladly end every statement with a semicolon if it allowed me to skip the braces around single-statement conditionals, but overall there's a lot to like.

So, given a language that I don't find offensive and an IDE I want to get more familiar with, here goes ...

### The Plan

I won't go so far as to claim I'm bothering with a software specification.
Instead, I'm thinking along the following lines, subject to change with each line of code I type.

#### Requirements

* Primarily a status-bar icon.
  * Whether there's a main menu is _TBD_.
* Connected Bluetooth devices supporting the "Battery Service" GATT will be monitored.
* The icon will reflect the lowest battery level of the connected devices.
* Status bar icon is composed of fragments from the BatteryUIKit framework.
  * Icon/fill is red when below a warning threshhold.
  * Icon displays properly in dark and light UI modes.
* Application is able to launch on startup.

#### Possible Enhancements

* Adjustable warning threshhold.
* Adjustable device list.
* Preference Pane.
* Formalized help.

### License

Follow the terms of the [license](LICENSE) and you can do _almost_ anything you want.
