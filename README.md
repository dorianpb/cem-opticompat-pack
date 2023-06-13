# Custom Entity Models Optifine Compatibility Resource Pack

The primary purpose of this pack is to translate between the part names used by Optifine into ones used by Minecraft. If using [my CEM mod](https://github.com/dorianpb/cem), this pack is basically required for it to work.

# Installation

Simply download the `.zip` and place the zip in your resource packs folder.

# Format

Each file should be placed in `assets/<namespace>/<entity name>.json`.
The names for `entity name` and `entity layer` are the ones used by Minecraft. By default, this file is used to target all layers of an entity. To target a specific layer, name the file `<entity name>_<entity layer>.json`.

The contents of each file should look like this:

```
{
    "partnames":{
        "<optifine part name>" : "<real part name>",
        ...
    },
    "modelfixes":{
        "<real part name>" : [
            <x offset>, <y offset>, <z offset>
        ],
        ...
    }
}
```

Empty parts can be omitted. The model fix offsets are for calcuating where transparent parts go when using the model fix if the mod gets it wrong. It has no effect if the model fix is turned off.
