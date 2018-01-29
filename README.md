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

 var arr = [5, 4, 3, 2, 1];
 var arr1 = _.first(arr, 3);
 console.log(arr1);

 var arr2 = _.initial(arr, 3);  //最初的
 console.log(arr2);

 var arr3 = _.last(arr, 2);
 console.log(arr3);

 var arr4 = _.rest(arr, 2);
 console.log(arr4);


 var arr20 = [0, 1, false, 2, "", 3, null, 4, undefined]; //紧凑
 var arr21 = _.compact(arr20);
 console.log(arr21);

 var arr22 = [1, [2, [3, [4]]]];
 var arr23 = _.flatten(arr22); //弄平
 var arr24 = _.flatten(arr22, true);
 console.log(arr2);
 console.log(arr23);
 console.log(arr24);

 var arr30 = [1, 2, 1, 0, 3, 1, 4];
 var arr31 = _.without(arr30, 0, 1);
 console.log(arr31);

 var arr40 = [[1, 2, 1, 4], [1, 2, 3, 112 ], [4, 5, 6, 2]];
 var arr41 = _.union(arr40);
 console.log(arr41);
 console.log(_.union(arr40));
 console.log(arr40);
 console.log(_.union([1, 2, 1, 4], [1, 2, 3, 112 ], [4, 5, 6, 2]));//同盟 只能直接写数组，不能传参数
 //把不相同的数字组成一个新的数组


 var arr50 = _.intersection([1, 2, 6], [1, 2, 3], [1, 2, 5]);
 console.log(arr50); //交叉，相交。把数组中相同的项组成一个新的数组，存在它的参数中

 var arr60 = _.difference([1, 2, 3, 4, 5], [5, 2, 9]);
 console.log(arr60); // 返回第一个数组中与后面的数组不相同的项

 var arr70 = _.uniq([1, 2, 2, 3, 1, 4]);
 console.log(arr70); //去重

 var str1 = _.zip(["Toni", "Pasha", "Jim"], [2, 26, 22], ["Player", "Teacher", "Student"]);
 console.log(str1); //把多个数组中相应位置的值合并在一起，组成新的数组,参数是一个数组

 var str11 = _.unzip([["Jim", "Toni", "Pasha"], [22, 3, 26], ["Softer", "Player", "Teacher"]]);
 console.log(str11); // 参数是一个二维数组，返回的结果与_.zip的结果相同

var arr = _.indexOf([1, 1, 2, 3,], 2);
 console.log(arr); //返回后面的项在数组中的索引

 var arr1 = _.lastIndexOf([1, 2, 3, 1, 2, 3], 3);
 console.log(arr1); //从后向前找，找到返回所在的索引

 var arr2 = _.sortedIndex([10, 20, 30, 40, 50], 45);
 console.log(arr2);

 var stooges = [{name: "Toni", age: 2}, {name: "Pasha", age: 26}];
 var arr3 = _.sortedIndex(stooges, {name: "Jim", age: 23}, "age");
 console.log(arr3); //把后面的项按顺序插入到数组中，返回插入项所在的索引，最后一个参数是迭代器

 /*var arr1 = _.findIndex([4, 6, 8, 12], 4);
 console.log(arr1);

 var arr2 = _.findIndex([4, 6, 8, 12], isPrime);
 console.log(arr2); // 当isPrime(最好的)为真时，返回索引
*/
 var users = [{"id": 1, "name": "Bob", "last": "Brown"}, {"id": 2, "name": "Ted", "last": "White"},
              {"id": 3, "name": "Frank", "last": "James"}, {"id": 4, "name": "Ted", "last": "Jones"}];

/* var arr3 = _.findLastIndex(users, {name: "Ted"});
 console.log(arr3);// 报错，不是一个function*/

 var arr4 = _.range(10);
 console.log(arr4);

 var arr5 = _.range(1, 11, 2);
 console.log(arr5);

 var arr6 = _.range(0, 50, 5);
 console.log(arr6);

 var arr7 = _.range(0, -10, -1);
 console.log(arr7);

 var arr8 = _.range(0);
 console.log(arr8); // _.range([start], stop, [step])
