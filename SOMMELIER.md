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

### Notes

- Eliza is built on top of the [AI SDK by Vercel](https://sdk.vercel.ai/docs/introduction)
- `generateObjectV2()` for requiring a structured response from an LLM
- The [runtime](https://github.com/PeggyJV/eliza/blob/c51e3081a171d7323aabaeb90f15d483b3fd7359/packages/core/src/runtime.ts#L54) can provide a `State` in plugin handlers. A `State` is basically just a formatted prompt with all of the context you pass into it, which can be included in the LLM prompt to inform its response. See the [`composeState` method](https://github.com/PeggyJV/eliza/blob/c51e3081a171d7323aabaeb90f15d483b3fd7359/packages/core/src/runtime.ts#L750)
