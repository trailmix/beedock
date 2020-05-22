# xhyve cli

currently some sort of CLI to manage xhyve on macos as some sort of "mobile" hypervisor

## Contributing

Currently you need [deno installed](../readme.md).

```bash
brew install --HEAD xhyve
brew install deno
```

Once installed a command like this will get the project started in watch mode:

```bash
# watch.ts watches all files, mod.ts is the entry point,
# it installs the cli each reload so with a save you can just test the cli
# idk if this is good, it downloads the external modules every time
deno run --allow-run --allow-read helpers/watch.ts install --unstable -f --allow-net mod.ts
```

### Test

```bash
# allow-run is needed most likely if the test spawns sub processes
deno test --allow-read --allow-run
```

### Watch, Test

```bash
# watch for any changes, and run tests
deno run --allow-run --allow-read helpers/watch.ts test --allow-read --allow-run
```

### Install

```bash
deno install -n xhyve-cli --unstable -f --allow-net mod.ts
## BONUS watch, test, install
deno run --allow-run --allow-read helpers/watch.ts test --allow-read --allow-run && deno install -n xhyve-cli --unstable -f --allow-net mod.ts
```
