# Pinhole

Polymer (v 1.0.x) behaviors with a set of filters to use in combination with a dom-repeat component.

[Visit the component page](http://ivanrod.github.io/pin-hole/components/pin-hole/)

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Install

Install it via bower:

    bower install pin-hole

Import it in your project:

```html
<link rel="import" href="../bower_components/pin-hole/pin-hole-behaviors.html">
```

## Usage

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
<input type="text" value={{ similarTo::input }} />
```
Filters:
- similarTo
- limitTo

Sorts:
- byText
- byEmailProvider
- byDate

## Testing

Simply navigate to the `/test` directory if
you are using Polyserve: `http://localhost:8080/components/pin-hole/test/`
