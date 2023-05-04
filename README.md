# 3p-libopenmetaverse

[Autobuild][autobuild] bottling of the C# [libopenmetaverse][] library.

## Requirements

- [autobuild][]
- [mono][]

Clone this repository and its submodules:
```
git clone --recurse-submodules https://github.com/secondlife/3p-libopenmetaverse
```

If you already have the code checked out, initialize and pull the libopenmetaverse submodule:
```
cd 3p-libopenmetaverse
git submodule init
git submodule update
```

Build and package:
```
autobuild configure
autobuild build
autobuild package
```

### Updating libopenmetaverse 

3p-libopenmetaverse uses a submodule to vendor its library, this makes it incredibly easy
to perform updates:

```
cd libopenmetaverse 
git fetch
git checkout <tag or other ref>
cd ..
git commit -am "Updated libopenmetaverse to ..."
```

### Publishing new versions

1. Create a PR
2. Merge into `main`
3. [Create a new release](https://github.com/secondlife/3p-libopenmetaverse/releases)

Version format: `v<libomv-version>-r<release-version>` ex `v9.3.0-r0`

[libopenmetaverse]: https://github.com/openmetaversefoundation/libopenmetaverse
[autobuild]: https://github.com/secondlife/autobuild
[mono]: https://www.mono-project.com/
