JavaScript中有5种简单数据类型（也被称为基本数据类型）：Undefined、Null、Boollean、Number和String。还有一种复杂数据类型：Object，Object本质上是有一组无序的名值对组成的。JavaScript不支持任何创建自定义类型的机制，而所有值最终豆浆是上诉6中数据类型之一。

## typeof()
使用<code>typeof()</code>可以检测变量的数据类型。对一个值使用<code>typeof()</code>可以返回一个字符串用于判断类型。
注意，当一个值是'Null'时，会返回'object'。因为特殊值Null被认为是一个空的对象的引用。<br>
如果这个值是函数，那么将返回'function'。<br>
对未初始化的变量执行typeof和对未声明的变量执行typeof都会返回undefined值。

## Undefined
Undefined类型只有一个值，即undefined。在使用'var'声明变量但未对其初始化时，这个变量的值就是undefined。例如：
```
var message;
alert(message == undefined); //ture
```
上面的例子只是声明了变量message，但并未对其进行初始化。比较这个变量与undefined字面量，结果他们是相等的。

在JS中使用未声明的变量会返回Error，但是对声明但并未初始化的变量和没
没有声明的变量使用typeof()都将返回undefined
## Null
Null类型是的第二个只有一个值的数据类型，这个特殊的值是null。null值表示一个空对象指针，因此使用typeof()检测null值时会返回'object'。对undefined和null使用'=='时，会返回true。因为undefined值是派生自null值的，对他们使用严格等于'==='就会返回false。

## Boolean
Boolean类型只有两个字面值：true和false。可以调用转型函数Boolean将一个值转换为其对应的Boolean值。

## Number
JS中的Number类型接受十进制、八进制与十六进制，但是在进行计算时，他们最终都将被转换为十进制。<br>
八进制第一位必须是零(0),然后是八进制数字序列(0\~7)。如果字面值中的数值超出范围，那么前导零将被忽略，后面的数值将被当作十进制数值解析。八进制字面量在严格模式下将会报错。<br>
十六进制字面值的前两位必须是0x，后面跟任何十六进制数字(0\~9及A\~F)，其中字母A~F可以大写，也可以小写。<br>


如果在小数点后没有跟任何数字，或者浮点数本身表示的就是一个整数，那么该值会被转换为整数。
可以用科学计数法表示某些极大或者极小的数字。如下：
```
var floatNum = 3.125e7; //等于31250000
var num = 3e-7;//等于0.0000003
```
科学计数法的写法为： 前面是一个数值(可以是整数也可以是浮点数)，中间是一个大写或小写的字母e，后面是10的幂中的指数，该幂值将用来与前面的数相乘。

NaN(Not a Number)是一个特殊的值，这个数值用于表示一个本来要返回数值的操作数未返回数值的情况。例如，在JS中，任何数值除以非数值会返回NaN,不会抛出错误影响其他代码的执行。<br>
NaN有两个特点。首先，任何涉及NaN的操作都会返回NaN(例如NaN/2)。其次，NaN与任何值都不相等，包括NaN本身。<br>
使用isNaN()函数检测是否"不是数值"。isNaN()在接收到一个值之后，会尝试将这个值转换为数值。转换成功会返回false。转换失败会返回true，因为他们"不是数值"。

有三个函数可以把非数值转换为数值：Number()、parseInt()和parseFloat()。第一个函数Number()可以用于任何数据类型，而另外两个函数专门用于把字符串转换成数值。

## String类型


## Object类型
