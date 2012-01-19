DetectSyntax
============

Description
-----------

DetectSyntax is a plugin for Sublime Text 2 that allows you to detect the syntax of files that might not otherwise be detected properly. For example, files with the `.rb` extension are usually Ruby files, but when they are found in a Rails project, they could be RSpec spec files, Cucumber step files, Ruby on Rails files (controllers, models, etc), or just plain Ruby files. This is actually the problem I was trying to solve when I started working on this plugin.

Installation
------------

DetectSyntax can be installed in a variety of ways:

* Through Package Control [http://wbond.net/sublime_packages/package_control] (http://wbond.net/sublime_packages/package_control)
* By cloning this repository in Packages
* By downloading the files and placing them into a directory under Packages, such as DetectSyntax or User.

Usage
-----

DetectSyntax is based on the idea that there are rules for selecting a certain syntax. You define the rules, the plugin checks them. The first one to pass wins. If you have need of multiple conditions that must be met, you should use the function rule. See the default settings file for more on function rules.

Create your rules in `Packages/User/DetectSyntax.sublime-settings`. The easiest way to get started is to just copy the default settings file found in `Packages/DetectSyntax/DetectSyntax.sublime-settings` to your user directory and modify it to meet your needs. Do keep in mind that if you have a `DetectSyntax.sublime-settings` file in your `Packages/User` directory, the default settings will not load. So if there are any default rules you want to use, copy them into your custom settings file. See the default settings file for examples and comments related to creating rules.

Credits
-------

It all started by forking the plugin created by JeanMertz (1). I modified it quite extensively until I ended up with something entirely my own (2). @maxim and @omarramos commented on the gist and suggested it should be part of Package Control. As I had created it solely for my own consumption, it seemed a bit "hard-coded" to be valuable as a package, but then I took a look at SetSyntax (3) and saw how using settings would make it very flexible. That set me on the path that led to DetectSyntax.

(1) [https://gist.github.com/925008] (https://gist.github.com/925008)  
(2) [https://gist.github.com/1497794] (https://gist.github.com/1497794)  
(3) [https://github.com/aparajita/SetSyntax] (https://github.com/aparajita/SetSyntax)