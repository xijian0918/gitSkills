# gitSkills

2018/2/5
1.注册Glthub账号
2.本地安装git
3.创建参考，拉取代码，提交代码
4.安装Webstorm

2018/2/6
1. html学习

2018/2/7
1.CSS学习，
  a. CSS Id和Class选择器
  b. CSS创建
  c. CSS Backgrounds
  d. CSS Text
  e. CSS Fonts、Link、列表样式、表格、盒子模型、边框、outline。Margin、Padding
2.notes
  a. ID属性和类名的第一个字符不要以数字开头，在部分浏览器中不起作用
  b. 外部样式表，内部样式表，内联样式
  c. 优先级逐级增加的选择器列表
     1）通用选择器
     2）元素（类型）选择器
     3）类选择器
     4）属性选择器
     5）伪类
     6）ID选择器
     7）内联样式
3.主要问题点：每一个标签下的属性太多，不容易记忆。
4.在Webstorm中怎么去操作，比如之前给的网站模型，如何在工具中去实现静态部分。

2018/2/8
1. CSS学习
   1）针对昨天CSS的学习，进行了一些练习
   2）CSS 分组和嵌套、dimension、Display、Positioning
2. notes
   1)块级元素(block)特性
   2)内联元素(inline)特性
   3)主要用的CSS样式有3个：
      a. display:block——显示为块级元素
      b. display:inline——显示为内联元素
      c. display:inline-block ——显示为内联块元素，表现为同行显示并可修改框高内外         边距等属性
   4)元素的堆叠，Z-index指定的数值越大，越被显示在前面。如没有指定，最后定位在
     HTML代码中的元素将被显示在最前面
3. CSS的设置各属性时是比较混乱的。

2018/2/10
1. CSS学习
   1)CSS Float、对齐、组合选择符、伪类、伪元素、导航栏、下拉菜单、提示工具、图片
     廊、图像透明/不透明、图像拼合技术、媒体类型、属性选择器
2. notes
   1).clearfix:after/before 可以用来清楚浮动
   2）* {box-sizing: border-box} 是CSS盒子模型，举例来说：如一个元素的width设为
      100px,那么这100px包含其它的border和padding
3. 对蚂蚁金服的网页布局进行了练习。

2018/2/12
1. js学习
   1）JS 用法、输出、语法、语句、注释、变量、数据类型、对象、函数
2. notes
   1）局部变量会在函数运行后被删除
   2）全局变量会在页面关闭后被删除
   3）直接赋值给尚未声明的变量，该变量将自动变为全局变量声明，即使它在函数内运行   4）JS变量均为对象，当你声明一个变量时，就创建了一个新的对象。
   5）在HTML中，所有全局变量都为Window变量。可使用window.XX

2018/2/13
1. js学习
2. notes
   1）=== 为绝对相等，即数据类型与值都必须相等。
   2）如果把数字与字符串相加，结果将成为字符串：
      var result1=5+5+"abc"; //结果将是“10abc”
      var result2=""+5+5+"abc"; //结果将是"55abc"
   3) html会压缩空格，所以直观上显示的是字符串，没有显示空格
   4）数字和布尔值相加，布尔值false转为0，true为1.
   5）数字与null（空值）相加，null转化为数字0；字符串与null（空值）相加，null转化为字符串。

2018/2/23
1. js学习
2. notes
   1）return false，在大多数情况下，为事件处理函数返回false，可以防止默认的事件       行为，例如默认点击一个<a>元素，页面会跳转到该元素href属性指定的页。而retur      n false可以终止这个跳转
   2) 检验是否为2-4个字的中文名称组成
      function ischina(str){
      var reg=/^[\u4E00-\u9FA5]{2,4}$/;
      return reg.test(str);
      }
   3) JS中的所有数据都是以64位浮点型数据(float)来存储。所有的编程语言，包括JS对       浮点型数据的精确度都很难确定。例如小数相加，需转化为整数后相加再抓为小数。

2018/2/27
1. ES6学习：let和const命令
2. notes
   1) 主要针对闭包进行了一个比较深入的了解

2018/2/28
1. ES6学习：变量的结构赋值
2. notes
   1）了解以下两个参数的区别
       function move({x = 0, y = 0} = {}) {         //此处参数为一个对象？！
       return [x, y];
       }

move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, 0]
move({}); // [0, 0]
move(); // [0, 0]
      
      function move({x, y} = { x: 0, y: 0 }) {     //此处参数只是为指定默认值?!
      return [x, y];
      }

move({x: 3, y: 8}); // [3, 8]
move({x: 3}); // [3, undefined]
move({}); // [undefined, undefined]
move(); // [0, 0]
    2）函数只能返回一个值，如要返回多个值，只能将他们放在数组或者对象里返回。
    3) \u0000~\uFFFF 正常字符的Unicode范围
    4）JavaScript 内部，字符以 UTF-16 的格式储存，每个字符固定为2个字节。对于那些需要4个字节储存的字符（Unicode 码点大于0xFFFF的字符），JavaScript 会认为它们是两个字符。
    5)fromCodePoint方法定义在String对象上，而codePointAt方法定义在字符串的实例对象上
3. 疑问
   加载模块时，往往需要指定输入哪些方法。解构赋值使得输入语句非常清晰。
   const { SourceMapConsumer, SourceNode } = require("source-map"); ??????
