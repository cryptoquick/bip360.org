# bip360.org

## build

In bips.dev, with submodule pointed to cryptoquick/bips, p2qrh branch:

```sh
git submodule update --recursive --init
./scripts/bips.sh
./scripts/static.sh
./scripts/generate.sh
./scripts/tailwind.sh
cd web/
zola serve
```

Visit:

http://127.0.0.1:1111/360/

Ctrl-U, Ctrl-A, Ctrl-C

Paste in index.html.orig

Apply changes.patch to index.html.orig output to index.html:

```sh
patch bip360.html.orig -o bip360.html < changes.patch
```

If updates to the patch file are ever needed:

```sh
diff bip360.html.orig bip360.html > changes.patch
```
