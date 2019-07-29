1. 导入Vue的包
2. 创建一个Vue的实例
el:表示，当前我们 new 的这个 Vue 实例，要控制页面上的哪个区域
data:存放的是 el 中要用到的数据
methods:定义了当前Vue实例所有可用的方法
<hr>
使用 v-cloak 能够解决 插值表达式闪烁的问题
默认 v-text 是没有闪烁问题的
v-text会覆盖元素中原本的内容，但是 插值表达式  只会替换自己的这个占位符，不会把 整个元素的内容清空
v-bind: 是 Vue中，提供的用于绑定属性的指令
注意： v-bind: 指令可以被简写为 :要绑定的属性
v-bind 中，可以写合法的JS表达式
Vue 中提供了 v-on: 事件绑定机制 缩写是 @要绑定的事件
<hr>
跑马灯思路分析:
1. 给按钮，绑定一个点击事件   v-on   @
2. 在按钮的事件处理函数中，写相关的业务逻辑代码：拿到 msg 字符串，然后 调用 字符串的 substring 来进行字符串的截取操作，把 第一个字符截取出来，放到最后一个位置即可；
3. 为了实现点击下按钮，自动截取的功能，需要把 2 步骤中的代码，放到一个定时器中去；
<hr>
事件修饰符：
使用  .stop  阻止冒泡
使用 .prevent 阻止默认行为
使用  .capture 实现捕获触发事件的机制
使用 .self 实现只有点击当前元素时候，才会触发事件处理函数
使用 .once 只触发一次事件处理函数
<hr>
v-bind 只能实现数据的单向绑定，从 M 自动绑定到 V， 无法实现数据的双向绑定
使用  v-model 指令，可以实现 表单元素和 Model 中数据的双向数据绑定
注意： v-model 只能运用在 表单元素中 input(radio, text, address, email....)   select    checkbox   textarea
<hr>
小结：
 1. MVC 和 MVVM 的区别 

 2. 学习了Vue中最基本代码的结构 

 3. 插值表达式   v-cloak   v-text   v-html   v-bind（缩写是:）   v-on（缩写是@）   v-model   v-for   v-if     v-show 

4. 事件修饰符  ：  .stop   .prevent   .capture   .self     .once 

 5. el  指定要控制的区域    data 是个对象，指定了控制的区域内要用到的数据    methods 虽然带个s后缀，但是是个对象，这里可以自定义了方法 

 6. 在 VM 实例中，如果要访问 data 上的数据，或者要访问 methods 中的方法， 必须带 this 

 7. 在 v-for 要会使用 key 属性 （只接受 string / number） 

 8. v-model 只能应用于表单元素 

 9. 在vue中绑定样式两种方式  v-bind:class   v-bind:style 