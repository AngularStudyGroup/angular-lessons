## Dynamic Template On Angular

This is a basic backbone html snippet, we have to write a lot boilerplate code like list `<li>` element or table `<tr>` element.

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


### Answer

#### First Page

```html
<!doctype html>
<html lang="en" ng-app>
<head>
    <meta charset="UTF-8">
    <title>Assignment 002</title>
    <link rel="stylesheet" href="/content/css/vendor.css">
</head>
<body>
    <table class="table table-striped">
        <thead>
            <tr><th>Name</th><th>Gender</th><th>Age</th></tr>
        </thead>
        <tbody>
            <!-- Write your code here -->
            <tr ng-repeat="i in [1, 2, 3, 4]">
                <td>{{ i }} Girl</td>
                <td>Female</td>
                <td>20</td>
            </tr>
        </tbody>
    </table>
    <script src="/bower_components/angular/angular.js"></script>
</body>
</html>
```

#### Second Page

```html
<!doctype html>
<html lang="en" ng-app="lessonTwo">
<head>
    <meta charset="UTF-8">
    <title>Assignment 002</title>
    <link rel="stylesheet" href="/content/css/vendor.css">
</head>
<body ng-controller="PeopleController">
    <table class="table table-striped">
        <thead>
            <tr><th>Name</th><th>Gender</th><th>Age</th></tr>
        </thead>
        <tbody>
            <!-- Write your code here -->
            <tr ng-repeat="people in peoples">
                <td>{{ people.name }}</td>
                <td>{{ people.gender }}</td>
                <td>{{ people.age }}</td>
            </tr>
        </tbody>
    </table>
    <script src="/bower_components/angular/angular.js"></script>
    <script type="text/javascript">
        (function () {
            "use strict";
            angular.module("lessonTwo", []).run();
            angular.module("lessonTwo").controller("PeopleController", ["$scope", function ($scope) {
                $scope.peoples = [{
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
                }];
            }]);
        })();
    </script>
</body>
</html>
```
