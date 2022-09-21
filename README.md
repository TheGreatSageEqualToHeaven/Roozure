<div align="center">
    <a href="https://github.com/TheGreatSageEqualToHeaven/Roozure"><img src="https://github.com/TheGreatSageEqualToHeaven/Roozure/blob/main/Logo.png" height="217" /></a>
</div>

<hr />

**Roozure** is a tool designed to automatically obfuscate script packages, models and place files to make exploiting games harder.

## What Roozure Is
### **Roozure is**

<div>A utility to prevent exploiters from reading your source code efficiently</div>
<div>A utility to prevent exploiters from hooking your code </div>
<div>A utility to prevent exploiters from dumping information from your code</div>

### **Roozure is not**

<div>A security measure for your remotes</div>
<div>A complete prevention to exploiting</div>
<div>A lossless security measure (Debugging information will be worse)</div>

## Features

* Obfuscating a single script
* Obfuscating a folder of scripts
* Optionally obfuscate scripts with a [Luau VM](https://github.com/TheGreatSageEqualToHeaven/Fiu) (Will require manual setup)
* Optionally use a module script to store constants
* Have a list of strings that get replaced every time Roozure rebuilds a script
* Have a list of table keys that get replcated every time

## What type of obfuscation can Roozure do?

### Xoring Strings
Strings will be decrypted with `bit32.bxor` and `string.unpack` to rely on builtin optimizations

### Control Flow Flattening
Scripts will have their control flow flattened using while loops to make decompiled output hard to reverse

### VM Obfuscation
Scripts will be obfuscated with a Luau VM compatible with the newest format, this needs to be setup by creating a "Fiu" module in `ReplicatedStorage`

### Instance Obfuscation
Scripts will have their instances obfuscated through an esoteric method of getting the `__index` metamethod of `Instance`
```lua
local indexInstance
xpcall(function()
  game:________()
end, function()
  indexInstance = debug.info(2, "f")
end)
```

## Contributing
Edit this section later

# Loretta
[Loretta](https://github.com/LorettaDevs/Loretta/) is a C# Lua, GLua and Luau parser, code analysis, transformation and generation library maintained by me and [GGG](https://github.com/GGG-KILLER)

<div align="left">
    <a href="https://github.com/LorettaDevs/Loretta/"><img src="https://github.com/LorettaDevs/Graphics/blob/main/logo.svg" height="217" /></a>
</div>

# License
Both Loretta and Roozure are available under the MIT license.
Roozure also relies on noblox for updating models.
