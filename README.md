# Angular Owl Carousel - 2

Impl for [OwlCarousel2]


### Installation

##### NPM
```ssh
npm install --save owl.carousel
```

##### Bower
```ssh
bower install --save owl.carousel
```

```ssh
npm install angular-owl-carousel2
```

```ssh
bower install angular-owl-carousel2
```


### Usage

In Your Angular application include one module:

```js
angular.module('CarouselApp', ['angular-owl-carousel-2'])
```

In Your HTML Layout include an original Owl Carousel files and Angular Carousel 
```html
<!-- CSS -->
<link rel="stylesheet" href="../bower_components/owl.carousel/dist/assets/owl.carousel.css">
<link rel="stylesheet" href="../bower_components/owl.carousel/dist/assets/owl.theme.default.css">

<!-- JS -->
<script src="../bower_components/jquery/dist/jquery.js"></script>
<script src="../bower_components/owl.carousel/dist/owl.carousel.js"></script>
<script src="../bower_components/angular/angular.js"></script>

<script src="../src/angular-owl-carousel-2.js"></script>
```

```js
$scope.items = [1, 2, 3, 4, 5, 6, 7, 8];
    let owlApi;
    
    $scope.properties = {
        items: 2,
        onChange: function () {
            console.dir(arguments);
        }
    };

    $scope.ready = function ($api) {
        owlAPi = $api;
    };

    $timeout(function () {
        console.dir(owlAPi);
        owlAPi.trigger('next.owl.carousel',[2000]);
    }, 2000)

```

```html
<ng-owl-carousel class="owl-theme" owl-items="items" owl-properties="properties" owl-ready="ready($api)">
    <div class="item"><h4>Free Item</h4></div>
    <div class="item" data-ng-repeat="item in items"><h4>{{$index}}</h4></div>
</ng-owl-carousel>
```
   [OwlCarousel2]: <https://github.com/OwlCarousel2/OwlCarousel2>
