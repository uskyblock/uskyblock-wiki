![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

The `levelConfig.yml` file holds the heart of uSkyBlock, the *scores of each block-type*.

It's a very simple config file, just 4 sections and a version number.

But the values, and their meaning is not for the faint-hearted.

The *key* to understanding this config file is, to understand how the *keys* are formatted.

## `general`

```yml
general:
  # pointsPerLevel - number of points needed to advance 1 island level.
  pointsPerLevel: 1000

  # default - the default value for blocks not listed in blockValues here.
  default: 10

  # useDiminishingReturns - If true, diminishing returns will be used for all blocks using the default scale 
  # (custom scales can be defined in the section below).
  # If useDiminishingReturns is false, the blocks listed in the dimishingReturns section will still be affected.
  useDiminishingReturns: false
  # defaultScale - the default value to use for diminishing returns. This is the number of blocks before DR starts to 
  # lower value.
  defaultScale: 10000
```

## A note on block-ids (keys) and `blockValues`.
To understand the way this config file is structured, keep in mind, that all blocks in Minecraft have both an *ID*, and a *data-value*.

If you want to keep it simple, you can simply ignore data-values, and use block-ids all through the config.
If you want to use data-values, you need to keep in mind, that different blocks uses data-values very differently.

I.e. `stone` (1) uses data-values for different types of stone (Granite, `1:1`) etc.
Where as, Quartz (155) uses data-values for both different types, and their orientation (`155:2`=Pillar Vertical, `155:3`=Pillar North South).

## `blockValues`

**Keys**
Keys in the `blockValues` section controls how blocks are treated.

`'<num>'` - This denote ALL blocks with this *block-ID* (all data-value-variants is counted as the ID:0 block).

`'<num>:*'` - This denote ALL blocks with this *block-ID* and data-values (all data-value-variants are counted separately).

`'<num>:<min>-<max>'` - Addresses a subset of *block-ID*s with data-values.

**Values**

The values have a special meaning for this section.

**positive-decimals** - Are simply the score assigned to each block of the designated type (see about keys above).

**`-1`** - Is used for _sub-types_ to mean _share count/values with the base-block ID (`<id>:0`).

**`-<num>`** - Is used to group different blocks together (for sharing limits or diminishing-returns).

I.e.
```yml
blockValues:
  # Give 20 pts. per LOG (naturally occurring wood)
  '17': 20
  # Count Acacia and Dark Oak as "normal LOGs".
  '162:*': -17
blockLimits:
  # Limit logs to only contribute to item-level for the first 20000 blocks. (Reg. of sub-type).
  '17': 20000
```

## `blockLimits`
Lists "hard-limits", that once a block-count reaches this limit, any additional blocks have no influence on the island-score.

Best used for blocks that are either easily obtainable, or have a very high score (i.e. cobble, or a dragon-egg).

## `diminishingReturns`
Lists a "soft-limit", at which point extra blocks will slowly give less and less per block added.