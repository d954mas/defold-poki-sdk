# Poki SDK native extension for Defold game engine
![pokisdk-hero](https://user-images.githubusercontent.com/2209596/102117637-db1df480-3e3e-11eb-9822-db237f36c0f6.jpg)
## Installation
To use this library in your Defold project, add the needed version URL to your `game.project` dependencies from [Releases](https://github.com/AGulev/defold-poki-sdk/releases)

<img width="401" alt="image" src="https://user-images.githubusercontent.com/2209596/202223571-c77f0304-5202-4314-869d-7a90bbeec5ec.png">


## API

Lua API corresponds to original JS API SDK:

```lua
poki_sdk.gameplay_start() -- in JS it's PokiSDK.gameplayStart()
poki_sdk.gameplay_stop() -- in JS it's PokiSDK.gameplayStop()
poki_sdk.commercial_break(function(self)end) -- in JS it's PokiSDK.commercialBreak()
poki_sdk.rewarded_break(function(self, success)end) -- in JS it's PokiSDK.rewardedBreak()
poki_sdk.set_debug(value) -- in JS it's PokiSDK.setDebug(value)
poki_sdk.capture_error(error_string) -- in JS it's PokiSDK.captureError(error_string)
poki_sdk.shareable_url(params, callback) -- in JS it's PokiSDK.shareableURL({}).then(url => {})
local value = poki_sdk.get_url_param(key) -- in JS it's PokiSDK.getURLParam('id')

-- Also, it's possible to check if AdBlock is active.
poki_sdk.is_ad_blocked()
```
Use this instruction: [PokiSDK - Defold](https://sdk.poki.com/defold.html)

Do not collect Lua errors manually using `sys.set_error_handler()`. The SDK collects Lua errors and the engine's errors and warnings automatically.

When you get your PokiSDK Sitelock code, just add it to your game as:
```lua
html5.run("Sitelock JS code from Poki")
```
For security reasons, this piece of code is not public, so please request it from your Poki contact.

---

If you have any issues, questions or suggestions please [create an issue](https://github.com/AGulev/defold-poki-sdk/issues) or contact me: me@agulev.com
