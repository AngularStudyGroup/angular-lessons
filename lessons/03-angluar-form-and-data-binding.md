## Angular Form Attributes

### Synopsis

As a web developer, we are familiar with web form. There can be little doubt that how to operate form by using javascript is a basic skill. If you have ever used jQuery, you must have seen some codes like below.

```html
<form>
	<input type="text" name="gender" />
</form>
```

```javascript
(function() {
	$("form").on("submit", function(event) {
		event.preventDefault();
		var gender = $("input[name='gender']");
		if (gender.val() === "female") {
			// some logic
		}
	});
})();
```

It's so verbose and hard to loop every elements in a form. You have to write a lot of dumplate code just for selecting specific form attribute. What's worse, binding the response from server side to a existing form would be a hard work !!! (Damn it.)

It's time to hug angular.js and see how angular.js achieve two-way data-binding by using magic `ngModel` directive.

### Bind 

First of all, you should read [**Simple Form**](https://code.angularjs.org/1.5.6/docs/guide/forms#simple-form) Charpter, glance at the sample code and have a rough impression on `ng-model` attribute.

Then we need head back to the code from lesson two. We will enrich the person table by adding some new properties. You can get the initial code from latest afs project and head rush to this exercise.

### Reference

1. https://code.angularjs.org/1.5.6/docs/guide/forms
2. https://code.angularjs.org/1.5.6/docs/api/ng/directive/ngModel

