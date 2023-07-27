# MAD web server

Convenience local web server for front-end development.

* .html masking: `/users.html` is served as `/users`
* Slow responses: adds 100ms to simulate network delays.
* Case-sensitivity: warn if url casing doesn't match the file system.
* Proxy `/api/` to any url, e.g. real rest api, aws lambdas.
* Reports missing files and actual file paths (no guessing)

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

Usage: mad [directory] [options]  (use -s0 or --no-s to turn off -s etc)

Options:
  -a, --access  Access log (log every request)         [boolean] [default: true]
  -B, --bind    IP address to listen on          [string] [default: "localhost"]
  -p, --port    TCP port to listen on                   [number] [default: 8000]
  -s, --slow    Serve files slowly (can specify ms delay)         [default: 100]
  -m, --mask    Mask the .html extension on .html files[boolean] [default: true]
  -r, --redir   Redirect .html paths to remove .html   [boolean] [default: true]
  -b, --block   Block .html paths to test masked URLs [boolean] [default: false]
  -P, --proxy   Proxy /api/ URLs (trims /api/ prefix)     [string] [default: ""]
  -w, --wait    Wait for an API request (specify /path/to/api)
                                                           [array] [default: ""]
  -h, --help    Show help                                              [boolean]
```
