packed version of [passy/angular-masonry](https://github.com/passy/angular-masonry) including the most dependencies + [angular-images-loaded-custom](https://github.com/JohnnyTheTank/angular-images-loaded-custom)

## Usage
1. Install via either [bower](http://bower.io/), [npm](https://www.npmjs.com/) or downloaded files:
    1. `bower install --save angular-masonry-packed`
    2. `npm install --angular-masonry-packed`
    3. use CDN ([jsDelivr](https://www.jsdelivr.com/projects/angular.masonry-packed))
    4. download [angular-masonry-packed.zip](https://github.com/JohnnyTheTank/angular-masonry-packed/zipball/master)
2. Add `wu.masonry` to your application's module dependencies.
3. Include dependencies in your HTML.
    1. When using bower:
    ```html
    <!-- dependencies -->
    <script src="bower_components/jquery/dist/jquery.js"></script>
    <script src="bower_components/angular/angular.js"></script>
    <!-- angular-masonry-packed -->
    <script src="bower_components/angular-masonry-packed/dist/angular-masonry-packed.min.js"></script>
    ```
    2. When using npm:
    ```html
    <!-- dependencies -->
    <script src="node_modules/jquery/dist/jquery.js"></script>
    <script src="node_modules/angular/angular.js"></script>
    <!-- angular-masonry-packed -->
    <script src="node_modules/angular-masonry-packed/dist/angular-masonry-packed.min.js"></script>
    ```

    4. when using CDN files
    ```html
    <!-- dependencies -->
    <script src="//code.jquery.com/jquery-2.1.4.min.js"></script>
    <script src="//ajax.googleapis.com/ajax/libs/angularjs/1.4.8/angular.min.js"></script>
    <!-- angular-masonry-packed -->
    <script src="//cdn.jsdelivr.net/angular.masonry-packed/0.14.5/angular-masonry-packed.min.js"></script>
    ```

    4. when using downloaded files
    ```html
    <!-- dependencies -->
    <script src="jquery.js"></script>
    <script src="angular.js"></script>
    <!-- angular-masonry-packed -->
    <script src="angular-masonry-packed.min.js"></script>
    ```
        
4. read docs on this the original repo: [passy/angular-masonry](https://github.com/passy/angular-masonry)

5. Use this custom events ([angular-images-loaded-custom](https://github.com/JohnnyTheTank/angular-images-loaded-custom)) for refreshing layout:
```javascript
$scope.$on('imagesLoaded.SUCCESS', function() {
    $scope.$broadcast("masonry.reload");
});

$scope.$on('imagesLoaded.ALWAYS', function() {
    $scope.$broadcast("masonry.reload");
});
```