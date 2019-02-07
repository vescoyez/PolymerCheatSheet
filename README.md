# Polymer Cheat Sheet

## data binding

### One-way data-binding

##### example:
```html
<h1>[[data]]</h1>
```

### Two-way data-binding

##### example:
```html
<input value="{{data}}" type="text">
```

### Update value with javascript

##### example:
```javascript
this.set('data', newValue);
```

if array

```javascript
this.data.forEach(function(item, index){
  this.set('data.' + index, newValue);
});
```

other method like: push, pop, splice, shift, unshift

```javascript
this.push('array', item);
```

### filter

```html
<template is="dom-repeat" items="[[myArray]]" filter="isOdd" observe="count">
  <span>[[item.count]]</span>
</template>
```
```javascript
isOdd: function(item) {
  return item.count % 2;
}
```
