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
 
 var underscore1 = _.contains([1, 2, 3], 4);
 console.log(underscore1);

 var arr1 = _.invoke([[5, 1, 7], [3, 2, 1]], "sort"); //invoke_.invoke(list, methodName, *arguments)
//在list的每个元素上执行methodName方法。 任何传递给invoke的额外参数，invoke都会在调用methodName方法的时候传递给它。
 console.log(arr1);

 var stooges = [{name: "Jim", age: 29, job: "Student"}, {name: "Toni", age: 2, job: "Player"},
                {name: "Pasha", age: 26, job: "Teacher"}];
 var stooges1 = _.pluck(stooges, "job"); // pluck 拉，拽;
 console.log(stooges1);

 var stooges2 = _.max(stooges, function (a) {
         return a.age;
 });
 console.log(stooges2);

 var stooges3 = _.min(stooges, function (b) {
         return b.age;
 });
 console.log(stooges3);

 var arr11 = _.sortBy([53, 121, 630, 88, 526], function (num) {
           return num;
 }); // 从小到大的排序
 console.log(arr11);

 var stooges11 = _.sortBy(stooges, "age");
 console.log(stooges11);

 var group1 = _.groupBy([1.2, 2.2, 2.5], function (num) {
      return Math.floor(num);
 });
 console.log(group1);

 var group2 = _.groupBy(["one", "two", "three"], "length");
 console.log(group2);

 var stooges12 = _.indexBy(stooges, "job");
 console.log(stooges12);

 var result = _.countBy([1, 2, 3, 4, 5], function (num) {
     return num  % 2 == 0 ? "even" : "odd";
 });
 var result1 = _.countBy([0, 1, 2, 3, 4, 5], function (num) {
       return num >= 2 ? ">=2" : "<2" ;
 });
 console.log(result1);
 console.log(result);

 var shuffle1 = _.shuffle([1, 2, 3, 4, 5, 6]); //拖曳
 console.log(shuffle1);

 var sample1 = _.sample([1, 2, 3, 4, 5, 6]);
 console.log(sample1);

 var sample2 = _.sample([1, 2, 3, 4, 5, 6], 3);
 console.log(sample2);

 console.log((function () {
  return _.toArray(arguments).slice(2);
 })(1, 2, 3, 4));

 var size = _.size({name: "Jim", age: 33, job: "Player"});
 console.log(size);

 var arr4 = [0, 1, 2, 3, 4, 5, 6];
 var arr41 = _.partition(arr4, function (num) {// 划分
      return num >= 3;

 });
 console.log(arr41);

