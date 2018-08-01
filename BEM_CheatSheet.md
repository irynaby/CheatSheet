# CSS:BEM

* Block
* Element (__)
* Modifier (_ or --)

```css
.menu {}
.menu__item {}
.menu__item_active {}
```

## Naming rules
```css
block-name__elem-name_mod-name_mod-val
```

* Names are written in lowercase Latin letters.

* Words are separated by a hyphen (-).

* The block name defines the namespace for its elements and modifiers.

* The element name is separated from the block name by a double underscore (__).

* The modifier name is separated from the block or element name by a single underscore (_).

* The modifier value is separated from the modifier name by a single underscore (_).

* For boolean modifiers, the value is not included in the name.

