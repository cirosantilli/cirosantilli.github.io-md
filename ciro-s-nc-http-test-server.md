<h1 id="ciro-s-nc-http-test-server">Ciro's <code>nc</code> HTTP test server</h1>

↑ **Parent:** [Test server](test-server.md)

As per [https://stackoverflow.com/a/52351480/895245](https://stackoverflow.com/a/52351480/895245) our standard test setup is:
```
while true; do
  resp=$"$(date): hello\n"
  len="$(printf '%s' "$resp" | wc -c)"
  printf "HTTP/1.1 200 OK\r\nContent-Length: $len\r\n\r\n${resp}\n" | nc -Nl 8000
done
```

## ↑ Ancestors (9)

1. [Test server](test-server.md)
2. [Server (computing)](server-computing.md)
3. [Networking hardware](networking-hardware.md)
4. [Computer network](computer-network.md)
5. [Computer](computer-split.md)
6. [Information technology](information-technology.md)
7. [Area of technology](area-of-technology.md)
8. [Technology](technology-split.md)
9. [Ciro Santilli's Homepage](split.md)

## ← Incoming links (1)

- [tcpdump](tcpdump.md)
