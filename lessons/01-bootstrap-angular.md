## Angular initialization

Following this document https://docs.angularjs.org/guide/bootstrap#manual-initialization, your would learn two types of method for initializing your angular app.

1. Create two pages on [afs](https://github.com/AngularStudyGroup/afs)
2. Using these two method for showing a hello world page like below.

```html
<h2>Hellow World</h2>
```

### Answer

#### Page 1

```html
<!doctype html>
<html lang="en" ng-app>
<head>
    <meta charset="UTF-8">
    <title>Assignment 001</title>
</head>
<body>
    <h2>
        {{ "Hellow World" }}
    </h2>
    <script src="/bower_components/angular/angular.js"></script>
</body>
</html>
```

#### Another Page 1

```html
<!doctype html>
<html lang="en" ng-app="lesson-001">
<head>
    <meta charset="UTF-8">
    <title>Assignment 001</title>
</head>
<body>
    <h2>
        {{ "Hellow World" }}
    </h2>
    <script src="/bower_components/angular/angular.js"></script>
    <script type="text/javascript">
        (function () {
            'use strict';
            angular.module('lesson-001', []).run();
        })();
    </script>
</body>
</html>
```

#### Page 2

```html
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Assignment 001</title>
</head>
<body ng-controller="IndexController">
    <h2>
        {{ helloWorldMessage }}
    </h2>
    <script src="/bower_components/angular/angular.js"></script>
    <script type="text/javascript">
        (function () {
            'use strict';
            angular.module('lesson-001', [])
                .controller('IndexController', ['$scope', function ($scope) {
                    $scope.helloWorldMessage = 'Hello World';
                }]);

            angular.element(document).ready(function () {
                angular.bootstrap(document, ['lesson-001']);
            });
        })();
    </script>
</body>
</html>
```
