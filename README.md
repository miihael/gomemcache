## About

This is a memcache client library for the Go programming language
(http://golang.org/).
This fork uses different server selection algorithm - Jenkins Hash, libmemcached 1.0 default.

## Installing

### Using *go get*

    $ go get github.com/miihael/gomemcache/memcache

After this command *gomemcache* is ready to use. Its source will be in:

    $GOPATH/src/github.com/miihael/gomemcache/memcache

## Example

    import (
            "github.com/miihael/gomemcache/memcache"
    )

    func main() {
         mc := memcache.New("10.0.0.1:11211", "10.0.0.2:11211", "10.0.0.3:11212")
         mc.Set(&memcache.Item{Key: "foo", Value: []byte("my value")})

         it, err := mc.Get("foo")
         ...
    }

## Full docs, see:

See https://godoc.org/github.com/miihael/gomemcache/memcache

Or run:

    $ godoc github.com/miihael/gomemcache/memcache

