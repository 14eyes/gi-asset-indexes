# gi-asset-indexes

Genshin Impact partially mapped asset indexes

![connect-asset-index](https://cdn.discordapp.com/attachments/140874168110546955/1052950781558530058/AI.png)

 `raw_names.txt` ~~used to try and match path~~ removed due to size.

[Current status](/STATUS.md)

Files are compact JSON. Indexes larger than 100 MiB (GitHub's file limit) are split into byte parts
`<name>.json.001`, `<name>.json.002`, ... (listed in `MappedParts`/`RawParts` in `version-index.json`). Join them back with:

```
cat <name>.json.0* > <name>.json
```

`PathHashRest` (upper bytes of the 64-bit path hash, ~3.2+) is only present when non-zero, and `Size` only from 4.0 on.
Mapped names have no type suffix.

P.S. Thanks to Terax and other people for helping
