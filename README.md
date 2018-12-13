# POC: Hugo with Starlight Plugins

Requires hugo built from this PR: https://github.com/gohugoio/hugo/pull/5521

There's a plugins directory which is configurable in the config.toml.  There's
also a plugins directory that can be in a theme.. hugo will look for plugins in
the user's directory first and if not found will look in the theme's directory
(so you can override the theme code).


Usage looks like this:

```
{{plugins.Starlight "hello.star" "name" "bob" "page" .Page}}
```

The first argument is required and is the name of the file to read.  Any
remaining arguments must be in "name", value pairs, the name must be a string,
the value can be whatever you want. 