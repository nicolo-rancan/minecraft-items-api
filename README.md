# Minecraft items api

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<br />

##### You can use this api to access all minecraft items (1.16.5)

###### Unofficial package

## Installation

```js
gh repo clone nicolo-rancan/minecraft-items-api
```

###### Internal port 3000 is used if an `.env` file is not present with the `port` variable.

## Usage

### Available endpoints

##### Get all minecraft items (limit: 1000 requests per hour)

```js
const ... = await fetch("baseurl/api/items");
```

###### Example response:

```js
{
  "generated": 1620803566367,
  "data": [
    {
      "name": "Air",
      "image": "https://minecraftitemids.com/item/32/stone.png",
      "url": "https://minecraftitemids.com/item/air",
      "id": "minecraft:air",
      "legacy_id": "N/A",
      "numerical_id": "N/A"
    },
    .
    .
    .
  ]
}
```

<br />

##### Get specific item informations (limit: 1000 requests per hour)

```js
const ... = await fetch("baseurl/api/items/itemname");
```

###### Example response:

```js
{
  "description": "Stone, not to be confused with cobblestone, can only be obtained when a stoneblock is broken with a silk touch pickaxe. It is required for many redstone items such as the comparator, and decorative items like stonebricks.",
  "properties": [
    {
      "key": "item_id",
      "value": "minecraft:stone"
    },
    .
    .
    .
  ]
}
```

<br />

##### Update cache memory (limit: 1 request per hour)

```js
const ... = await fetch("baseurl/api/update");
```

###### This will update the memory cache used to serve the items list, so it is used to get more infos out of them.

<br />
