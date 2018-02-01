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

var func = function (greeting) {
    return greeting + ":" + this.name;
};

 func = _.bind(func, {name: "Jim"}, "Hi");
 console.log(func()); //Hi:Jim  _.bind(func, object, *argument)这里的*argument指的是func中的参数

 var buttonView = {
     label: "underscore",
     onclick: function () {
         alert("clicked: " + this.label);
     },

     onHover: function () {
         console.log("hovering:" + this.label);
     }
 };

 // var obj1 = _.bindAll(buttonView, "onClick", "onHover");
 // jQuery("#underscore_button").bind("click", buttonView.onclick);// 把按钮的"click"绑定到buttonView.onClick中，jQuery选中的
                                                                  //按钮也有了以上的方法
 var subtract = function (a, b) {
     return b - a;
 };

 sub5 = _.partial(subtract, 5); //部分的，钟爱的
 console.log(sub5(20));//先传入的5是a的参数，后传入的20是b参数，是相反的传入过程

 subForm20 = _.partial(subtract, _, 20);
 console.log(subForm20(5));//给了一个占位符相当于是a参数,后面的20就是b参数

 var fibonacci = _.memoize(function (n) {
     return n < 2 ? n: fibonacci(n - 1) + fibonacci(n - 2);
 }); // 可以缓存函数的计算结果。 不是很理解

 var log = _.bind(console.log, console); //只有console.log也是可以的为什么呢？
  _.delay(log, 1000, "logged later"); //延时,_.delay(function, wait, *arguments)等待wait毫秒后调用function，有argument时
                                      //argument作为参数传入

 _.defer(function(){
     alert("deferred");
}); //延迟调用function直到当前调用栈清空为止，_.defer(function, *arguments)有argumets时会传入到函数中;

 /*var throttled = _.throttle(updatePosition, 100);
 $(window).scroll(throttled);*/ //当重量调用函数的时候，至少第隔wait毫秒调用一次。会在你调用第一时间尽快执行这个function,并且，如果
 //在wait调用任意次数的函数，都将尽快的被覆盖。禁用第一次执行的话，传递{leading: false},禁用最后一次执行传递{trailing: false}.
 // _.throttled(function, wait, [options]) 选项的意思，在[]的都是可选的参数

 /*var laayLayout = _.debounce(calculateLayout, 300);
 $(window).resize(lazyLayout);*///返回function函数的防反跳版本，将延迟函数的执行（真正的执行）在函数的最后一次调用 时刻的wait毫秒
 //之后，_.debounce(function, wait, [immediate})。immediate为true,debounce会在wait时间之后开始调用这个函数。

 var initialize = _.once(function () {
     console.log("Hello world!");
 });
 initialize();
 initialize();//创建只能调用一次的函数

 /*var renderNotes = _.after(notes.length, render); //创建一个函数，只有在运行了count次之后才有效果
 _.each(notes, function (note) {
     note.asyncSave({success: renderNotes});
 });*/

 /*var mothlyMeeting = _.before(3, askForRaise); //创建一个函数，调用不超过count次。当count已经达到时，最后一个函数调用的结果将
 mothlyMeeting();                              // 被记住并返回。
 mothlyMeeting();
 mothlyMeeting();*/

 var hello = function (name) {
     return "Hello:" + name;
 };
 hello = _.wrap(hello, function (hello) {
     return "before," + hello("Toni") + ", after";
 });

 console.log(hello());// 将第一个函数functin封装到函数wrapper里面，并把函数function作为第一个参数传给wrapper。理解了，但是
                      // 结果不相同，再研究一下.结果会调用Underscore.js中的函数为什么呢？
                      
  var isFalsy = _.negate(Boolean); //否定的意思
 var arr22 = _.find(["Jim", -1, true, 0, null], isFalsy); //返回第一个通过后面的函数检测的真值检测的元素值，找到后立即返回不会遍历
 console.log(arr22); // 找到第一个不是true的，就返回了

 var greet = function (name) {
     return "hi: " + name;
 };

 var exclaim = function (statement) {
     return statement.toUpperCase() + "!";
 };

 var welcome = _.compose(exclaim, greet); //组成，构成的意思
 console.log(welcome("Toni")); //返回函数集functions组合后的复合函数，也就是一个函数执行完之后把返回的结果再作为参数赋给下一个函数来执行
                               // 把函数f(), g(), 和h()组合起来可以得到复合函数f(g(h())). 

var obj1 = {one: 1, two: 2, three: 3};
 var arr11 = _.keys(obj1);
 console.log(arr11); // 检索object拥有的所有的可枚举的属性的名称。返回一个数组

 function Stooge(name) { //助手的意思，这是一个构造函数
     this.name = name;
 }
 Stooge.prototype.silly = true; //蠢的，不明事理的
 // var arr12 = _.allKeys(new Stooge("Jim"));
 // console.log(arr12); //检索object拥有的和继承的所有属性的名称，返回一个数组。但是这个报错

 var obj11 = {one: 1, two: 2, three: 3};
 var arr13 = _.values(obj11);
 console.log(arr13); //返回object对象的所有的属性值

 var obj22 = {start: 5, end: 12};
 var foo = function (val, key) {//是反的，属性值在前，属性名在后面
     return val + 5;
 };

 // console.log(_.mapObject(obj22, foo)); //类似于map,这是用于对象。转换每个属性的值。报错

 var obj23 = {one: 1, two: 2, three: 3}; // 一对的意思，一对夫妻
 console.log(_.pairs(obj23)); //把对象转变为一个[key, value]形式的数组

 var obj33 = {Moe: "Moses", Larry: "Louis", Curly: "Jerome"};
 console.log(_.invert(obj33));//返回一个object副本，使键和值对换。确保object里所有的值都是唯一的且可以序列成字符串

 var moe = _.create(Stooge.prototype, {name: "Jim"});//给函数的原型增加一个作为own（自己的）属性，和Object.create一样

 console.log(_.functions(_)); //返回一个对象里所有的方法名，而且是已经排序的也就是说，对象里每个方法（属性值是一个函数）的名称

 // console.log(obj33, predicate); // 类似于_.findIndex,但是对于的是对象中的键

 console.log(_.extend({name: "Jim"}, {name: "Toni", age: 50}));// 复制来源对象中的甩的属性覆盖到目标对象上，并且返回目标对象
  // 复制是按顺序的，如果目标对象上有重复的会被覆盖掉。第一个是目标对象，第二个是来源对象。 延伸，扩大的意思

 // _.extend(desination,*sources); // 类似于extend，但是只复制自己的属性覆盖到目标对象（不包括继承过来的属性）

 var obj21 = {name: "moe", age: 30, userid: "moe1"};
 var obj01 = _.pick(obj21, "name", "age");  //挑选的意思
 console.log(obj01); //返回一个object副本，只过滤出keys（有效的键组成的数组）参数指定的属性值

 var obj02 = _.pick(obj21, function (value, key, object) { //这里都是这样先是，值、键、对象。感觉像是反着的
     return _.isNumber(value);
 })
 console.log(obj02); // 或者接受一个判断函数，指定挑选的那个keys

 var obj31 = {name: "Toni", age: 2, job: "Player"};
 var obj03 = _.omit(obj31, "job");// 省略，遗漏，删掉的意思
 console.log(obj03);  //返回一个object副本，只过滤出除去keys(有效的键组成的数组)参数指定的属性值。指定了那个key就把那个去除掉

 var obj04 = _.omit(obj31, function (value, keys, object) {
     return _.isNumber(value); //value是数字的key
 });
 console.log(obj04); //或者接受一个判断函数，指定忽略的哪个key,这里就是value是数字的那个key

 var obj32 = {name: "Jim"};
 var obj33 = {name: "Toni", age: 2, job: "Player"};
 var obj05 = _.defaults(obj32, obj33);
 console.log(obj05); //用defaults对象（第二个参数）填充object(第一个参数）中的undefined属性。并且返回这个object.一旦这个属性被
 // 填充，再使用default方法将不会有任何效果
 console.log(_.defaults(obj05, {job: "Teacher"}));// 这个时候再给同一属性使用_.defaults方法已经无效

 var obj33 = {name: "Pasha"};
 console.log(_.clone(obj33)); //创建一个浅复制的克隆object.任何嵌套的对象或数组都通过引用拷贝，不会复制。

 _.chain([1, 2, 3, 200])
     .filter(function (num) {
         return num % 2 == 0;
     })
     .tap(alert)
  .map(function (num) {
    return num * num;
})
    .values(); //这个不是很理解

 var obj34 = {name: "Toni", age: 2, job: "Player"};
 console.log(_.has(obj34, "name")); // 对象是否包含给定的吗？等同于object.hasOwnProperty(key),但是使用hawOwnProperty函数的
                                     //一个安全引用，以防意外覆盖
 console.log(obj34.hasOwnProperty("name"));

 var stooge = {name: "Jim"};
 console.log(_.property("name")(stooge));//返回一个函数，这个函数返回任何传入的对象的key属性。在这里返回的是对象stooge中的name
                                          //键值

 console.log(_.propertyOf(stooge)("name")); //  无看到的解释不太一样，返回的结果相同，还要再研究源码

 var ready = _.matches({selected: true, visible: true}); //返回一个断言函数，这个函数会给你一个断言可以用来辨别给定的对象是否匹配
                                                         // attrs(里面的唯一的一个参数)指定键/值属性
 var readyToGoList = _.filter(list, ready); //遍历list中的每个值，返回所有通过（第二个参数可以是一个函数）真值的检测的元素所组成的数组

 var stooge = {name: "Toni", age: 2, job: "Player"};
 var clone = {name: "Toni", age: 2, job: "Player"};

 console.log(stooge == clone);
 console.log(_.isEqual(stooge, clone)); // 执行两个对象之间的优化深度比较，确定他们是否应被视为相等。返回布尔值

 var obj1 = {name: "Jim", age: 2};
 // console.log(_.isMatch(obj1, {age: 2})); //_.isMatch(object, properties)告诉你properties中的键和值是否包含在object中。

 console.log(_.isEmpty([1, 2, 3]));
 console.log(_.isEmpty({}), _.isEmpty([])); // 如果不包含任何值返回true.对于字符串和类数组对象，如果length属性为0，也返回true.

 console.log(_.isElement($("body")[0]));
 console.log(_.isElement(document.getElementsByTagName("body")[0])); // 如果object(参数）是一个DOM元素，返回true.

 var str1 = "This is my wife";
 var arr1 = [1, 2, 3];
 console.log(_.isArray(str1), _.isArray(arr1)); // 如果是数组，就返回true.

 console.log(_.isObject({})); // _.isObject(object)如果object是一个对象，返回true.需要注意的是JavaScript数组和函数也是对象，
 console.log(_.isObject(1));  // 字符串和数字不是对象

 (function () {
    console.log( _.isArguments(arguments));
})(1, 2, 3);

 var arg = _.isArguments([1, 2, 3]);
 console.log(arg);

 var underscore = _.noConflict(); //冲突的意思。 放弃Underscore的控制变量“_"。返回Underscore对象的引用。

 var stooge = {name: "Jim", age: 2, job: "Player"};
 // console.log(stooge === _.identity(stooge));// 返回与传入参数相等的值，相当于数学里的：f(x) = x.这个函数看似无用，但是在Underscore
  //里被用作默认的迭代器iterator.不过在这里有报错 。身份的意思

 var foo = {name: "Toni", age: 2};
 // console.log(foo === _.contant(foo)); // 报错

 // obj.initialize = _.noop;  // 返回undefined,不论传递给它是什么参数。可以用作默认可先的回调参数。初始化的意思，空的意思

/* _.(3).times(function (n) {
     genie.grantWishNumber(n);
 });*///_.times(n, iteratee, [context]) 调用给定的迭代函数n次，第一次调用iteratee传递index参数。生成一个返回值的数组。

 // console.log(_.random(0, 30)); // 返回最小到最大之间的随机整数。

/* _.mixin({
     capitalize: function (string) {
         return string.charAt(0).toUpperCase() + string.substring(1).toLowerCase();
     }
 });

 console.log(_("fabio").capitalize());*/

 var stooges = [{name: "curly", age: 25}, {name: "moe", age: 21}, {name: "larry", age: 23}];
 var youngest = _.chain(stooges)
     .sortBy(function (stooge) {
         return stooge.age;
     })
     .map(function (stooge) {
         console.log( stooge.name + "is" + stooge.age);
     })
     .first()
     .values()
