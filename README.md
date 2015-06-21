# Pinhole

A set of filters to use with a dom-repeat component in polymer 1.0.


## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Use

You can use this behaviors in your custom elements in combination with a dom-repeat element:

```javascript
	Polymer({
		is: 'my-list',
		behaviors: [
			PinHoleBehavior
		],
		...
```

Just add the filters and sorts to the dom-repeat element:
```html
<template is="dom-repeat" items="{{ myItems }}" filter="{{ applyFilters(filterConfig) }}" sort="{{ applySorts(sortConfig) }}">
  <li><span>{{ item }}</span></li>
</template>	
```

### Properties

Use the properties added with the behavior to customize your lists: 

```html
<input type="text" value={{similarTo::input}} />
```

## Testing 

Simply navigate to the `/test` directory if
you are using Polyserve: `http://localhost:8080/components/pin-hole/test/`
