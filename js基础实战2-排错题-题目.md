# js基础实战2-排错题-题目

==请说出以下代码都错在哪里，以及书写正确的代码==



## JS代码书写位置

```html
<script src="./02.js">
    alert('弹框出现')
</script>
```

分析错误：不能再引用的script标签中写js代码

正确写法：
<script>
    alert('弹框出现')

</script>

    
```js

```





在

## 输出语句

```js
prompt(请输入您的姓名)
```

分析错误：括号中没有引号

正确写法：

```js
prompt('请输入姓名')

```





## 变量01

```js
let age = 18
let age = 19
```

分析错误：重复定义变量





## 变量02

```js
console.log(age)
let age = 18
```

分析错误：  不能先输出为定义的变量

正确写法：

```js
let age = 18
console.log(age)

```







## 字符串01

```js
let username = 张三
```

分析错误：字符串没有加""

正确写法：

```js
let username = '张三'

```







## 字符串02

```js
let uname = '张三"
```

分析错误：不能一个单引号一个双引号

正确写法：

```js
let uname = '张三'

```







## 数组

```js
// 需求：取出 星期六 

let arr = ['星期一', '星期二', '星期三', '星期四', '星期五', '星期六', '星期日']
console.log(arr[6])
```

分析错误：数组是从0开始的索引

正确写法：

```js
let arr = ['星期一', '星期二', '星期三', '星期四', '星期五', '星期六', '星期日']
console.log(arr[5])


```









## 自增

```js
// 让num自身增加1

let num = 10

num + 1
```

分析错误：没有定义接收 num+1的变量

正确写法：

```js
let num = 10
    num = num +1
```









## switch分支

```js
let num = prompt('请输入一个数字')

switch (num) {
    case 1:
        alert('用户您输入的是数字1')
    case 2:
        alert('用户您输入的是数字2')
    case 3:
        alert('用户您输入的是数字3')
    default:
        alert('用户您输入的是非1、2、3的数字')
}
```

分析错误：没有能打断循环的条件

正确写法：

```js
let num = prompt('请输入一个数字')

switch (num) {
    case 1:
        alert('用户您输入的是数字1');
        break
    case 2:
        alert('用户您输入的是数字2');
        break
    case 3:
        alert('用户您输入的是数字3');
        break
    default:
        alert('用户您输入的是非1、2、3的数字');
        break
}
```







## while循环

```js
let num = 1
while (num <= 5) {
    document.write(`月薪过万不是梦<br/>`)
}
```

分析错误：  没有累加变量会死循环

正确写法：

```js
let num = 1
while (num <= 5) {
    document.write(`月薪过万不是梦<br/>`)
    num ++;
}
```









## for循环

```js
for (let i = 1; i <= 3;) {
    document.write(`月薪过万不是梦 <br/>`)
}
```

分析错误：没有累加变量

正确写法：

```js
for (let i = 1; i <= 3; i++) {
    document.write(`月薪过万不是梦 <br/>`)
}
```







## 遍历数组

```js
// 需求：取出数组中的每一项

let arr = ['马超', '赵云', '张飞', '关羽', '黄忠', '小黑', '小红']

for (let i = 1; i < arr.length; i++) {
    console.log(arr[i])
}
```

分析错误：循环变量初值应该是0

正确写法：

```js
let arr = ['马超', '赵云', '张飞', '关羽', '黄忠', '小黑', '小红']

for (let i = 0; i < arr.length; i++) {
    console.log(arr[i])
}
```







## 修改数组的项

```js
// 需求：将数组中的小白修改成 小灰灰
let arr = ['小黑', '小白', '小红']

arr = '小灰灰'
```

分析错误：没有指出数组中‘小白’的索引

正确写法：

```js
let arr = ['小黑', '小白', '小红']

arr[1] = '小灰灰'
```







## 操作数组

```js
// 需求：在数组arr的最后面添加 blue

let arr = ['red', 'green']

arr.push = 'blue'
```

分析错误：push('blue')

正确写法：

```js
let arr = ['red', 'green']

        arr.push('blue')
```







## 对象

```js
// phone 手机对象

let phone = {
    size = 6.1
    play = function () {
        console.log('走起，吃鸡')
    }
}
```

分析错误    不是=应该是： 中间没有加','

正确写法：

```js
let phone = {
    size : 6.1,
    play : function () {
        console.log('走起，吃鸡')
    }
}
```







## 遍历对象

```js
let obj = {
    uname: '小明',
    age: 18,
    sex: '男',
    height: 200,
}

// 遍历obj对象，取出对象的属性名和属性值
for (let k in obj) {
    console.log(k)
    console.log(obj.k)
}
```

分析错误：  k需要加[]

正确写法：

```js
let obj = {
    uname: '小明',
    age: 18,
    sex: '男',
    height: 200,
}

// 遍历obj对象，取出对象的属性名和属性值
for (let k in obj) {
    console.log(k)
    console.log(obj[k])
}

```









