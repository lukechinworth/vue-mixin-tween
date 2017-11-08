# Vue Mixin Tween
Vue mixin factory to tween component numerical data (using Tween.js).

## Installation
`npm install vue-mixin-tween`

## Usage
To tween a component prop, e.g. `width`:

```
import VueMixinTween from 'vue-mixin-tween';

export default {
    props: {
        width: Number,
    },
    mixins: [
        VueMixinTween('width'),
    ],
    // this.widthTween now available in your component
    // update width to new value, and widthTween will tween from the old to the new
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

## Contributing
Please send a pull request if you'd like to improve the project.
