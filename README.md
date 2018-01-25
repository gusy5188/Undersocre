# Undersocre.js
 // _.each([1, 2, 3], console.log);
 _.each({one: 1, two: 2, three: 3}, console.log );
 var arr = [1, 2, 3];
 var arr1 = _.map(arr, function (num) {
     return num * 3;
 });
 console.log(arr1);


 var arr2 = _.map({one: 1, two: 2, three: 3}, function (num, key) {
     return num * 4;
 });
 console.log(arr2);

 var arr3 = _.map([[1, 2], [3, 4], [5, 6]], _.first);
 console.log(arr3);

 var sum = _.reduce([1, 2, 3], function (memo, num) {
     return memo + num;
 }, 1);
 console.log(sum);

 var list = [[0, 1], [2, 3], [4, 5]];
 var flat = _.reduceRight(list, function (a, b) {
     return a.concat(b);
 }, [8, 9]);
 console.log(flat);

 var even = _.find([1, 21, 3, 41, 5, 61], function (num) {
     return num % 2 == 0;
 });
 console.log(even);

 var even1 = _.filter([1, 21, 3, 41, 5, 61], function (a) {
     return a % 2 == 0;
 });
 console.log(even1); //没有匹配的项时返回一个空数组

 var listOfPlays = [1, 2, 3,];
 // var obj1 = _.where(obj, )

 var obj = _.where(listOfPlays, {author: "Shakespeare", year: 1611});
 console.log(obj);

 var obj1 = _.findWhere([1, 2, 3], {one: 1, two: 2, three: 3});
 console.log(obj1);

 var odds = _.reject([1, 2, 3, 4, 5, 6], function (a) {
     return a % 2 == 0;
 });
 console.log(odds);

 var ever = _.every([true, 1, null, "yes"], _.identity); //every原生的比较好
 console.log(ever);

 var som = _.some([true, false, 0, null]);  //原生的比较好
 console.log(som);
