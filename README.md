3.5.0 详细介绍 

http://e.v-get.com/z/o/js.xml

备注注释

注：这不是一个框架，仅仅是一个Javascript函数包。这个函数包仅仅使用26个大写英文字母+41个$开头的字符，禁止再扩展更多。其核心思想就是坚持用数学思想去“简化”代码。对于企业而言，针对编程人员的流动性不可预料，所以使用大众框架（如prototype.js 或者 jQuery 等）是非常重要的，故此函数包仅提供与对数学感兴趣、对用数学思想简化代码的人共同探讨使用，而非市场化、商业产品。

本函数包代码尚属很垃圾的阶段，但是目的不是商业化，本人是喜欢数学，把编程当兴趣，而不是为了找工作做产品（嘿，哥们，如果为了薪资，还是学jQuery比较好），所以旨在寻觅喜欢数学、喜欢用数学方法简化代码、有代码洁癖、把编程当作兴趣的志同道合的人，哪怕一个都足够了。

由于尚在积累后端代码规律，所以尚未推出后端代码规则。V-Get!前端代码坚持 简化 > 性能 > 可读性，可能有些规则和国际标准冲突，不过冲突部分都不会造成任何执行或者bug问题。这种冲突是编程习惯的因素导致，不同的编程习惯，代码标准坚持大方向统一，小习惯上自主的原则。

jQuery可以简化开发时间，但是太偏离代码简洁的原则，不过短期内可以使用 jQuery() 代替 jQuery $()函数实现临时特效，再慢慢通过原生态JS取代jQuery。

bol 布尔数； int 整数； flt 浮点； str 字符串； obj 对象； arr 数组；

a:o 对象数组； i:p 正整数； i:n 负整数；

版本说明：若同名函数性质或使用方法改变，版本第一位数改变；
若同名函数性质未改变，但是添加了一些使用和功能，版本第二位数改变；
若同名函数性质和功能未改变，只是优化了部分代码，版本第三位数改变；
公用函数

JS框架临时替代

▶
jQuery ： jQuery 的 $ 替代名（tech.qq.com 也是如是做的），修改方法，点击左边三角形备注
默认常量

▶
bol I ： TRUE
bol O ： FALSE
$1 ：
str $2 ： 'http://'
obj $3 ： window
obj $4 ： document
obj $5 ： window.location
$6 ：
str $7 ： 'click'
str $8 ： 'mouseover'
str $9 ： 'mouseout'
单大写字母

▶
A() ： 将所有 a标签的 target 变成'_blank'，并将 s.v-get.com/l?l= 还原
A('id', targetName) ： 将 $('id') 下所有 target="_blank" 的 a标签的 target 变成'_blank' '_self' '_parent' 等之一，并将 s.v-get.com/l?l= 还原
A('id', targetName, start, length) ： 将 $('id') 下 target="_blank" 的 第start个的第end个（如果end为空，那么表示到最后一个）a标签的 target 变成'_blank' '_self' '_parent' 等之一，并将 s.v-get.com/l?l= 还原
A('', targetName, start, length) ： 将所有target="_blank" 的 第start个的第end个（如果end为空，那么表示到最后一个）a标签的 target 变成'_blank' '_self' '_parent' 等之一，并将 s.v-get.com/l?l= 还原
A('id', '_') ： 这是设置不可修改的target="_blank" ，或者已经被修改成_self后，再修改回_blank的a 必须使用 A('id','_');
B() ： 设置鼠标触发 li / p 变化。B(a触发模块,b触发背景颜色#开头，或者触发className,c触发颜色,d离开背景色#开头，或者离开className,e鼠标离开颜色);
str C(obj) ： 获取某个元素的className
C(obj, className) ： 设置这个元素的className 为 class值，className 也可为 ''
D(obj) ： obj.style.display:none
D(obj, I) ： obj.style.display:block
E(obj, type, function) ： 防冒泡事件
F(arr, function(single, sequence){}) ： for 语句 single = arr[sequence);
G ：
str H(obj) ： 返回obj的innerHTML
H(obj, str) ： obj.innerHTML = str
bol I ： 常量 true
J(url) ： 所有内容加载完成后，在<head>标签后加载这个url 地址的js代码
J(url, func) ： 所有内容加载完成后，在<head>标签后加载这个url 地址的js代码，再执行函数
J(url, func, obj) ： 所有内容加载完成后，在obj元素后加载这个url 地址的js代码，再执行函数
K(cookieName) ： 获取 cookieName 值，getCookie(cookieName)
K(cookieName, value, days) ： 设置 cookieName 值，有效期为 days 天
int L(str/arr) ： 字符串/数组的长度，不存在就返回0；自然数（包括0、负数、正数）长度都为0
M('d',0,5,215,5000,MD); ： 跑马灯/图片滚动效果
N(t,z,d,f) ： 目录下滑
bol O ： 常量 false
P ：
Q() ： 设置所有a target="_blank"；加入收藏夹；随机广告
R ：
S(obj, style) ： 获取样式表中的样式。S($("id"),'width'); o.style.width只能对 <div style="width:100px">这种能用，而对于用css独立页写的，或者放在<style>里面的，都无法使用
T(str) ： 判断str是否为（自然数、字符串、小数、【有值】array、存在的对象、有值类、布尔TRUE）
T(str, int:type) ： 判断str类型是不是 [0:'',1:'undefined',2:'boolean',3:'number',4:'string',5:'object',6:'function'][type]；若type为0，那么就是用上面的T(str)判断，如果为负数，就永远为false
U ：
V ：
W ：
X ：
Y ：
Z(html) ： 弹出一个id="z" ，内容为html的悬浮框
$

▶
obj $('id') ： 返回单个id对象，document.getElementById('id')
a:o $('^tag') ： 返回所有tag标签的对象数组，document.getElementsByTagName('tag')
a:o $('^*') ： 返回所有标签的对象数组，document.getElementsByTagName('*')
a:o $('.className') ： 返回所有class="className"的对象数组
a:o $('^tag.className') ： 返回所有tag标签的class="className"的对象数组
a:o $('id^tag') / $('^tag.className', $('id')) ： 返回id对象下所有tag标签的对象数组，document.getElementById('id').getElementsByTagName('tag')
a:o $('^tag', obj) ： 返回obj【如$('id')/$('^div')[0]】对象下所有tag标签的对象数组，document.getElementById('id').getElementsByTagName('tag')
a:o $('id^tag.className') / $('^tag.className', obj) ： 返回id对象下所有tag标签的class="className"的对象数组
$+小写字母

▶
$a ：
$b(obj, x, y) ： 设置这个元素背景位置为 background-positon:x,y
$c ：
$d ：
$e(bool) ： ie= i chrome=c firefox=f opera=o safari=s，没有b就是整数版本，比如 i9 i8 i6 c24 有b，就是具体版本 i9.0 i8.0 i6.0 c24.0.1312.57
$f ：
$g(obj, attribute) ： 获取 obj的 attribute值
$g(obj, attribute, value) ： 设置obj的 attribute值，value可以为（自然数[含0]、""、字符串）
$h ：
$i(num) ： 将负数、字符串转换成整数，如果num未指定，返回0
$j ：
str $k(str) ：获取当前链接 location.search 如 v-get.com/s?l=1&k=%E6%88%91%E7%88%B1%E4%BD%A0 的某个参数 $k("k") 返回 我爱你，$k("l) 返回 1
str $k(str, true) ： 获取当前链接 location.search 如 v-get.com/s?l=1&k=我爱你 的某个参数 $k("k") 返回 $k("k",I); 返回 decodeURI("我爱你") 即 “%E6%88%91%E7%88%B1%E4%BD%A0”
str $k(str, bol, url) ： 返回链接url的上述参数；$k("sk",O,"s?sk=E维科技"); 返回 “E维科技”； $k("sk",I,"s?sk=E维科技"); 返回“E%E7%BB%B4%E7%A7%91%E6%8A%80”
str $l(str) ： 返回str.toLowerCase()
str $l(url, true) ： 获取一个链接的域名；$l("e.v-get.com"); 返回 v-get.com
int $m(obj) ： 返回obj含边框的高的高度， 返回整数，而 $S(obj,"height")返回含 px的字符串
int $m(obj, TRUE) ： 返回obj含边框的宽的宽度，返回整数，而 $S(obj,"width")返回含 px的字符串
$n ：
$o(str) ： clearTimeout(str)
$o(str, TRUE) ： clearIntervale(str)
$o(func, time) ： setTimeout(func, time)
$o(func, time, true) ： setInterval(func,time)
arr $p(str, splits) ： str.split(splits);
$q ：
str $r(str, replace_pattern, replaceto) ： str.replace(replace_pattern, replaceto) 【并且已经先将 [\n\r] 等换行符替换掉了】
$s(arr) ： 返回数组arr中，随机一个元素
str $s(str,int:start,int:length) ： str.substr(start,length); 没有指定length就截取到尾部，如果start为0，从头开始；为负数，就是从倒数第start截取到尾部；$s('123456789',-2) = '89'
$t ：
$u ：
$v ：
$w ：
$x(str, chrs_search, int:start) ： 从start位字符开始，查找chars_search字符/串，找到返回找到位置，没找到返回-1；str.indexOf(chrs_search, start||0)
$y ：
$z ：
$+大写字母

▶
$A(url, vars, obj) ： $A("a.php","3342&sk=js",$("ajax"));Ajax Post，ajax会出现跨域问题。vars 默认传递 'v='+vars; 如果传递多个值，vars 可以是 123&b=3423&c=33…… 获得post返回输出值之后，写入 obj
$A(url, vars, false, func(h){}) ：var fun=function(h){alert(h);};$A("a.php","3342&sk=js",O,【function(h){alert(h);} 或者 fun(h)】);这里函数里面的h是post传递之后返回输出值，这里不会预先输出，而是可以再设置直接传递一个返回值的函数
$A(url, vars, obj, func(h){}) ：将返回值输出在obj中，并执行带这个输出值h的函数
$B ：
$C(tagName="div", id=idName/class=className, str, position_obj=document.body) ： $C("span","id=love","I Love You..."); 创建一个id=idName或class=className的tagName标签，并将str作为其innerHTML，【并且返回这个创建的元素obj】 $C(O,"id=love","love"); 在document.body后创建一个 <div id="love">love</div>，而且可以使用obj操作这个元素；var obj=$C("script");
$D(obj, ) ： $D(a外面的id,显示区的tagName,是否有class ，默认 id=?da cda class=?d 或者 id=?d ?do
$E ：
$F ：
$G ：
$H ：
$I ：
$J ：
$K(obj, strs) ： $K($("id"),"上海市,北京市");批量替换用逗号隔开的关键词为红色
str $L(url) ： 将非本站域名下的网址改变成s.v-get.com/l?l=
$M ：
$N ：
$O ：
$P ：
$Q ：
$R ：
$S() ：
$T ：
$U ：
$V ：
$W ：
$X ：
$Y ：
$Z ：
