# League

## Troubleshooting

### Missing node signing public key

Restart the DFX network with:

```
dfx start --clean
```

The `--clean` option removes checkpoints and stale state information from your project’s cache so that you can restart the Internet Computer replica and web server processes in a clean state.

### How to upgrade the SDK

To upgrade from a previous SDK version, run:

```
dfx upgrade
```

For a clean installation instead of an upgrade, run:

```
~/.cache/dfinity/uninstall.sh && sh -ci "$(curl -sSL https://sdk.dfinity.org/install.sh)"
```

[vue]: https://vuejs.org/
[sdk]: https://sdk.dfinity.org/docs/index.html
[project]: https://sdk.dfinity.org/docs/developers-guide/tutorials/explore-templates.html
[vuetify]: https://vuetifyjs.com/
[]: 
[]: 