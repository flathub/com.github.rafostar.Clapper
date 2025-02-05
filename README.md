## com.github.rafostar.Clapper

Level up your video experience with a modern and user-friendly media player.

## com.github.rafostar.Clapper.Enhancers

This extension adds default set of plugins enhancing `Clapper` library capabilities.
It can be used by other apps which implement `libclapper`.
If you want to check which plugins are available, see source repository [here](https://github.com/Rafostar/clapper-enhancers).

In order to allow your app to load and use enhancers, add following changes to your manifest:

```json
{
    "add-extensions": {
        "com.github.rafostar.Clapper.Enhancers": {
            "version": "stable",
            "directory": "extensions/clapper/enhancers",
            "add-ld-path": "lib",
            "no-autodownload": false,
            "autodelete": false
        }
    },
    "finish-args": [
        "--env=CLAPPER_ENHANCERS_PATH=/app/extensions/clapper/enhancers/plugins",
        "--env=PYTHONPATH=/app/extensions/clapper/enhancers/python/site-packages"
    ],
    "cleanup-commands": [
        "mkdir -p /app/extensions/clapper/enhancers"
    ]
}
```
