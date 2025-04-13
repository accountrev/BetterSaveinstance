# Description
Some edits to UniversalSynSaveInstance such as fixing gethiddenproperty (terrain, etc) and more. I'll try to keep this up to date with the original.


# Loadstring

```lua
local Params = {
 RepoURL = "https://raw.githubusercontent.com/Devraj2010isme/BetterSaveinstance/refs/heads/main/",
 SSI = "saveinstance",
}
local synsaveinstance = loadstring(game:HttpGet(Params.RepoURL .. Params.SSI .. ".luau", true), Params.SSI)()
local Options = {} -- Documentation here https://luau.github.io/UniversalSynSaveInstance/api/SynSaveInstance
synsaveinstance(Options)
```
# Differences From the Original
- Fixed gethiddenproperty, in the original it uses UGCValidationService:GetPropertyValue instead. (Allows for terrain to save)
- Added a counter at the end of the file to prevent overriding when writing to file names that already exist.
  - EX:
    - place 1 example.rbxlx
    - place 1 example(2).rbxlx
 - Better default executors for many options
# Universal Syn Save Instance

Or shortly USSI, a project aimed at resurrecting saveinstance function from Synapse X.<br />
Reason: Many Executors fail miserably at providing good user experience when it comes to tinkering with saving instances.

> [!WARNING]
> As stated under the Section 7 (b) in the LICENSE:
> - You **MUST** always include the following Credit string: `UniversalSynSaveInstance https://discord.gg/wx4ThpAsmw`
> - You are **NOT** allowed to claim authorship of the source code provided in this repository
> - You **MUST** always include the following [License](https://github.com/luau/UniversalSynSaveInstance/blob/main/LICENSE)

> [!TIP]
> Important part about this saveinstance is that it doesn't modify anything, therefore reduces the amount of detection vectors by a lot.<br />
> You can also enable the `SafeMode` option to completely bypass any detections and save **ANY** game!<br /><br />
> If this script is helpful to you, please click `⭐ Star` in the upper right corner of the page to support it, thank you!


# Acknowledgments
> [!IMPORTANT]
> This document is based largely on the efforts of [@Anaminus] & [@Dekkonot], authors of the [Roblox Format Specifications]. Additional
resources include:
> 
> - [Syngp Synapse X Source code 2019][Synapse X Source 2019] for base saveinstance code (extended by [@mblouka] & [@Acrillis])
> - [Moon/LorekeeperZinnia][@LorekeeperZinnia] for being the original creator of saveinstance that was used in Synapse X, Elysian and many others. As well as being an inspiration for this project.
> - [Rojo Rbx Dom Xml] for being a fallback documentation in case something wasn't clear in the [Roblox Format Specifications]
> - [Roblox File Format] for a list of redirects of old/deprecated xml properties that still use the old tag values
> - [Roblox Client Tracker] for an extended & close to full JSON Api Dump (with hidden properties & default values)

\*\*\* View source code of this file for more credits

[@Acrillis]: https://github.com/Acrillis
[@Anaminus]: https://github.com/Anaminus
[@Dekkonot]: https://github.com/Dekkonot
[@mblouka]: https://github.com/mblouka
[@LorekeeperZinnia]: https://github.com/LorekeeperZinnia
[bit32]: https://create.roblox.com/docs/reference/engine/libraries/bit32
[buffer]: https://create.roblox.com/docs/reference/engine/libraries/buffer
[pack]: https://create.roblox.com/docs/reference/engine/libraries/string#pack
[unpack]: https://create.roblox.com/docs/reference/engine/libraries/string#unpack
[string]: https://create.roblox.com/docs/reference/engine/libraries/string
[DataType Exceptions]: https://github.com/rojo-rbx/rbx-dom/blob/8ca9250fa5a5ad3756c89e1e111e1aabaf698b27/rbx_reflector/src/cli/generate.rs#L196
[KRNL Docs]: https://app.archbee.com/public/PREVIEW-2Jp4SDaAD4P1COFfx1p_t/PREVIEW-EtjA4sQe5zYUxIHwA6CqJ#mDB9D
[KRNL-like saveinstance Options]: https://app.archbee.com/public/PREVIEW-2Jp4SDaAD4P1COFfx1p_t/PREVIEW-EtjA4sQe5zYUxIHwA6CqJ#mDB9D
[Rojo Rbx Dom Xml]: https://github.com/rojo-rbx/rbx-dom/blob/master/docs/xml.md
[Rojo Rbx Dom Binary]: https://github.com/rojo-rbx/rbx-dom/blob/master/docs/binary.md
[Luau Syntax]: https://luau-lang.org/syntax
[Rbx-Binary-Format]: https://github.com/Dekkonot/rbx-binary-format/blob/master/src/writer.lua
[Roblox Client Tracker]: https://github.com/MaximumADHD/Roblox-Client-Tracker
[Roblox File Format]: https://github.com/MaximumADHD/Roblox-File-Format
[Roblox Format Specifications]: https://github.com/RobloxAPI/spec/
[Roblox Format Specifications Binary]: https://github.com/RobloxAPI/spec/blob/master/formats/rbxl.md
[SharedStrings]: https://github.com/RobloxAPI/spec/blob/master/formats/rbxlx.md#sharedstring
[Synapse X Docs Old]: https://synapsexdocs.github.io/custom-lua-functions/misc-functions/#save-instance
[debug]: https://web.archive.org/web/20221021015553/https://docs.synapse.to/reference/debug_lib.html
[Synapse X Docs]: https://web.archive.org/web/20230318113846/https://docs.synapse.to/reference/misc.html
[Synapse X Source 2019]: https://github.com/Acrillis/SynapseX
[PropertyPatches v1]: https://github.com/MaximumADHD/Roblox-File-Format/blob/main/Plugins/GenerateApiDump/PropertyPatches.lua#L72
[PropertyPatches v2]: https://github.com/rojo-rbx/rbx-dom/tree/master/patches
[PropertyPatches v3]: https://github.com/rojo-rbx/rbx-dom/blob/master/rbx_dom_lua/src/customProperties.lua
[UNC]: https://github.com/unified-naming-convention/NamingStandard/commit/613c1956b801ace54ba141dfc60842a16608b54f
