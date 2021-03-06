HJKLPlugin
==========

A plugin for vim keybindings in Mac OS X Mail

# So what does this do?

It's a simple plugin that lets you use `vim` keybindings in Mac OS X's Mail.app.

At the moment, it only works on the message view pane (to navigate all messages in a given thread) and in the message list (to move the selection up or down and to expand/collapse threads).

It also allows you to hit `x` to delete a message and `v` to open the _first_ URL in an HTML message in the browser (useful if, like me, you miss Google Reader)

# How do I install it?

Before installing the plug-in, you'll need to make sure that Mail.app's plug-in support is turned on. For this, execute the following two commands in Terminal.app:

    defaults write com.apple.mail EnableBundles -bool true
    defaults write com.apple.mail BundleCompatibilityVersion 3

Run `install.sh` under your own account (i.e., do *not* use `sudo`, under any circumstances!). 

That will build and deploy the `.bundle` to your `~/Library/Mail/Bundles` folder.

# What manner of dark magic is this?

It's a bit of Python that swizzles Objective-C methods and handles keypresses, mapping them to the codes Mail.app expects. The whole codebase fits in a screenful, and you can tweak it to your liking with minimal effort.

# References

* [vim keybindings for Lion Mail.app](http://the.taoofmac.com/space/blog/2011/08/13/2110)
* [Making your mail sit up and beg](http://the.taoofmac.com/space/blog/2011/08/11/2240)
