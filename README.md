# Vue Mixin Tween
Vue mixin factory to tween component numerical data (using Tween.js).

## Installation
`npm install vue-mixin-tween`

## Usage
To tween a vm prop `width`:

```
import VueMixinTween from 'vue-mixin-tween';

export default {
    mixins: [
        VueMixinTween('width'),
    ],
    // this.widthTween now available in your component
};
```

## API
### `VueMixinTween(propName[, duration[, ease]])`
#### `propName: String`
Component property to watch for changes. Tweened property available on component context at `${propName}Tween`.

#### `duration: Number = 500` (optional)
Duration of tween.

#### `ease: Function = TWEEN.Easing.Quadratic.Out` (optional)
Easing function to tween value with.
