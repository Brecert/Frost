## Crafting

Crafting is not done in the traditional sense with defined recipes, but done in a more open way.

Wrapping string around a stick and some carved wood *could* create a tool, but it's likely to break after one hit because the
string or wood would come undone.

Unfortunately due to limitations, rope strength has to be a fixed value, and can't be physics based.

Instead the knot strength is calculated and that value is used.

Knot strengths include

* tightness/looseness
* rope quality
* wear and tear

All of these slowly deteriorate and they all deteriorate based on each others values, not to mention the weight of to connection and so on.

Knots aren't the only connector type, but I will use them as the main one for simplicity right now.

Other types may include glue, magic, fusing, etc..

Crafting saves the positions and levels of all connected items along with a random seed for future use.

## Forging

Forging is done with a hammer or other heavy tools.

To forge a player puts on an applicable material or item and must heat it up to hammer it.

The effectiveness of hammering is based on the density, softness, and malability levels.

As your forging skills increase, it's more likely to focus on a specific random seet for how the wood comes off, thus making it more "accurate" to what you expect.

Saving forged items can be difficult because of the memory it may take up (it's a specific process).

The idea is to record all hit points with a seed and value then when loading apply all hit points with the applicable seed and value when loading.

Then as the item takes damage you add the damage to seed and value record.

```
0:
  seed: 10203939202
  strength: 20
  material: iron
  etc...
1:
  etc...
```

## Carving

Carving is done with an axe on woods or other applicable materials.

The softness and density values are taken into account when determining the durability left on the axe, along with the axes levels aswell.

Unlike forging, malability is not taken into account.

Carving is similar to forging in which you manually cut off parts from the material slowly.

As your carving skill is increased, its more likely to focus on a specific random seed for how the wood comes off, thus making it more "accurate" to what you expect.

Carving is saved in the same way forging works
