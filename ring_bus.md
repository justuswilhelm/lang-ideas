# Ring Bus

Statically typed network programming language with fixed ring buffer primitive
data type

## Applications

- Stream Processing
- Routing

## Requirements

- Static Typing
- Primitive Data Types (with big/little endian support):
    - Ring Buffer
    - Int64
    - UInt64
    - Structs with full memory layout control
    - Type Safe Union
- Elegant type safe switch statement
- Syntax easy to type on english keyboard, e.g. -=,.;'`[]
- Efficient binary unpacking and packing
- Fixed size loops
- Byte string methods
- Socket library
- Deterministic runtime behavior
- Suitable for soft-realtime systems
- Shell
- Every function has a user definable time out through decorator pattern
- Every function automatically returns the last value evaluated
- No garbage collection
- No memory allocation

## Sample Code

```
= retry 10
= timeout 5
write_value socket sock, byte[] message = server_response do
    sock.send message
    [header.8, _.8, body.8] = sock.read 24
    switch header[0] do
        case 'a' do
            [
                type=response_type.A,
                body=body,
            ]
        end
        case 'c' do
            [
                type=response_type.C,
                body=body,
            ]
        end
    end
end
```

Possibly interesting: Threaded code, no function returns

## Related Work

- [Snabb](https://github.com/snabbco/snabb)
- [click](https://github.com/kohler/click/)
