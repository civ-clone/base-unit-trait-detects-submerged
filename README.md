# base-unit-trait-detects-submerged

The `DetectsSubmerged` unit trait: a unit type with it detects submerged units.

A unit type with this trait reveals `Submerged` units near it.

For example: Civ2: flag 14 (Destroyer, Cruiser, AEGIS Cruiser, Helicopter).

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(DetectsSubmerged)`:

```ts
import DetectsSubmerged from '@civ-clone/base-unit-trait-detects-submerged/DetectsSubmerged';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, DetectsSubmerged));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
