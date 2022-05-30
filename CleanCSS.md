# Clean CSS

## SMACSS

Organize your CSS in 3 folders

### 1. base

Base styles are just **Normalize** plus some **basic default element styles** (colors, typography, margins & padding).

### 2. modules

Modules are standalone, reusable components that have no knowledge of their parent container. 
Their only dependencies are the app’s base styles. 
We can **safely delete** a module **when** it’s **no longer needed** without causing changes elsewhere in our CSS.

Since setting a module’s width, position or margins would require knowledge of the context it appears in, modules are always either fullwidth block elements or inline elements.

### 3. state

Module-specific state classes are defined in the same file as the module itself (e.g. .my-module--is-active) but we keep **global state classes** separate, e.g. .is-hidden.

## BEM

### Block

Standalone entity that is meaningful on its own. 
*E.g.: menu*

### Element

A part of a block that has no standalone meaning and is semantically tied to its block. 
E.g.: *.menu__item*

### Modifier

A flag on a block or element. Use them to change appearance or behavior.
E.g.: *.button--big*