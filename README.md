#Introduction

Hem is a project for compiling CommonJS modules when building JavaScript web applications. You can think of Hem as [Bundler](http://gembundler.com/) for Node, or [Stitch](https://github.com/sstephenson/stitch) on steroids.

This is rather awesome, as it means you don't need to faff around with coping around JavaScript files. jQuery can be a npm dependency, so can jQueryUI and all your custom components. Hem will resolve dependencies dynamically, bundling them together into one file to be served up. Upon deployment, you can serialize your application to disk and serve it statically.

#Installation

    npm install -g hem

    or

    npm install -g git@github.com:aeischeid/hem.git

#Usage

Please see the [Hem guide](http://spinejs.com/docs/hem) for usage instructions.

#TODO

* Need to setup HEM so that it will build/compile a physical specs file
* Integrate with phantom for running tests by command or by watching for file changes -> need to setup the index.html file to determine if running the server or by file system, should be able to look at the url fro http: or file://. Also need different output formats from the phantom script, sometimes report everything, other times just errors? Ability to only specific specs or test? Perhaps this can be configured by slug file.
* Check if running at root at project, look for slug.json file and throw error if its not there??
* This would be cool -> integrate with live-reload for changes. We should be able to inject https://github.com/livereload/livereload-js while in server mode and then run the livereload-server inside hem or could strata handle the incoming requests? Looks like simple json requests. Would we need an option for the browser to regain its focus? Another option is instead of injecting the script into the page is to use the live reload plugin.
* Make hem more generic to work with other types of frameworks like angular?? probably move more configuration to slug.json if we do this
* consider merging dust and html templates feature from: git://github.com/guillaume86/hem.git ( at least including strait html templates is probably a good idea considering eco's current ineffeciancies)
* port and update hem guide here since hem will probably be depricated in spine docs in favor of catapult

#History

Originally developed by @maccman to compliment Spine.js. He started a replacement project which is a ruby based project called catapult. Some of us still love the mode.js and hem way of doing things. In the spirit of open source it is forked and we are hoping to disccus moving npm repo to point to this version of hem which we plan to maintain for the near future at least.
