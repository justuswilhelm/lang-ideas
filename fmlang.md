# Fakemile

Makefile-Like language that has recipes produce in-memory data instead of files.

## Example

Every recipe returns a path to a fifo buffer. Each line is executed in a
subshell.

```
main: greeting=hello_world
    cat $greeting

hello_world:
    echo "hello world"
```
