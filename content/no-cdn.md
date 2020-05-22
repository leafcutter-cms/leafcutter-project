# How to run Leafcutter without CDN libraries

By default this template uses a theme package that loads common third-party front-end libraries from cdnjs.com. If you are concerned about the privacy implications of this, rest easy! Not using a CDN is literally one Composer command away. The default `theme-core` package provides all the same libraries (maybe not the exact same versions at any given time, but close), and will take over if you just uninstall the `theme-cdnjs` package.

```bash
composer remove leafcutter/theme-cdnjs
```

Not using a CDN will place some additional load on your server, but has the potential to actually improve front-end performance. Since the libraries all get loaded from local files, Leafcutter can 

## Adding CDN libraries back in

If you removed the CDN theme package, and would like to add it back, simply run the following command. It is adviseable to use a wildcard version constraint, because `theme-core` specifies which versions of `theme-cdnjs` it is compatible with. Other addons and themes are also supposed to specify their theme version requirements via a requirement of `theme-core`. Specifying a version constraint for `theme-cdnjs` in your `composer.json` is a great way to wind up in dependency hell.

```bash
composer require leafcutter/theme-cdnjs:*
```
