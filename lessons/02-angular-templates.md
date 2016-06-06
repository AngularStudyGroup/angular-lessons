## Dynamic Template On Angular

Here is a basic backbone html snippet, we have to write a lot boilerplate code like list `<li>` element or table `<tr>` element.

```html
<ul>
  <li>
    <span>Nexus S</span>
    <p>
      Fast just got faster with Nexus S.
    </p>
  </li>
  <li>
    <span>Motorola XOOM™ with Wi-Fi</span>
    <p>
      The Next, Next Generation tablet.
    </p>
  </li>
</ul>
```

First of all, we urge your to create a blank page. Generate a [angular template](https://code.angularjs.org/1.5.6/docs/tutorial/step_02) and using `ng-repeat` element to create a 3 X 4 table. The table header is already given in our afs project, the table content could be random letter or other thing.

After getting hang of `ng-repeat`, define a controller named `PeopleController`, using [Dependency Injection](https://code.angularjs.org/1.5.6/docs/guide/di) to inject page `$scope`. Passing a list of people below and show them in our pre-generated table.

```javascript
[{
    "name": "Lily",
    "gender": "female",
    "age": 67
}, {
    "name": "Tom",
    "gender": "male",
    "age": 23
}, {
    "name": "Bill",
    "gender": "male",
    "age": 37
}, {
    "name": "Nyan Pass",
    "gender": "female",
    "age": 7
}]
```

> **Relative Link:**
>
>1. https://code.angularjs.org/1.5.6/docs/tutorial/step_02
>2. https://code.angularjs.org/1.5.6/docs/guide/di
