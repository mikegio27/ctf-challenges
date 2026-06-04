# ctf-challenges

CTF challenge server registry to store containers and READMEs to share while
keeping code private.

The challenge **source stays in private repos**; only the built container images
are published here (to GHCR), so you can pull a challenge and try to crack it
locally without seeing the source.

---

## joshua
A wargames themed box. Still somewhat of a work in progress, but it is ready to be cracked. Responsible use of AI is important.

### Pull & run

```sh
docker pull ghcr.io/mikegio27/ctf-challenges/joshua:latest

docker run --rm -p 8765:8765 -p 8080:8080 \
  ghcr.io/mikegio27/ctf-challenges/joshua:latest
```

Then open the WOPR UI and start playing:

- **UI:** http://localhost:8080
- **WebSocket:** `ws://localhost:8765`

Everything you need is on the box — players get only `host:port`, no handout.
Start at the chat, get a foothold, and work your way to `FLAG{...}`.
