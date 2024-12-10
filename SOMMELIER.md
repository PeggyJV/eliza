# Sommelier Team README

## Plugin Submodule

The plugin-somm directory is a git submodule of [this private repo](https://github.com/PeggyJV/Eliza_plugin). After first cloning, ensure you have an ssh key from your host registered on your Github account, and then run

```bash
git submodule update --init --recursive
```

To update the submodule when changes occur upstream, run

```bash
git submodule update --recursive --remote
```
