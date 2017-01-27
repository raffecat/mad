# MAD web server

A local web server for front-end dev that watches for file changes.

This server is not appropriate for production; use [Nginx](http://nginx.org/) instead.

### Installing

MAD requires [node.js](https://nodejs.org/) and is installed and run from the [terminal](http://www.imore.com/how-use-terminal-mac-when-you-have-no-idea-where-start) or [command prompt](http://www.computerhope.com/issues/chusedos.htm).

```npm install -g mad```

### Using

MAD will serve files from the current directory unless you use the `-d` option.

```
% mad -m
MAD: serving /home/bob/folio/static on http://localhost:8000/ [mask .html]
```

### Help

```
% mad help
Options:
  -p, --port  TCP port to listen on                 [number] [default: 8000]
  -d, --dir   Local directory to serve               [string] [default: "."]
  -s, --slow  Serve files slowly (can specify ms delay)
  -m, --mask  Mask the .html extension on .html files              [boolean]
  --help      Show help                                            [boolean]
```
