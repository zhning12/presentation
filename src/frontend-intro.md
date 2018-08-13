title: 前端生态简介
speaker: 张一宁
theme: colors
transition: slide2
headFiles: /assets/style.css

[slide]

# JavaScript
## 张一宁
[slide]

## 开发工具

- 编辑器和IDE
	- Visual Studio Code（微软开源的神器）
	- WebStorm（JetBrains开发）
	- 其他
- 调试工具
	- Chrome Dev Tools（浏览器自带）
	- Firebug（Firefox专用）

[slide]

## 可视化

- Echarts（百度）/Hightcharts，[Demo](http://gallery.echartsjs.com/editor.html?c=xrJHCfsfE-)
- Canvas
- SVG:D3/Snap.svg，[Demo](http://snapsvg.io/demos/#game)
- WebGL/Three.JS，[Demo](http://webglsamples.org/aquarium/aquarium.html)，[Demo](https://beinternetawesome.withgoogle.com/en/interland/landing/mindful-mountain)

[slide]

## 第一题

- 题目描述：输入两个整数x, y，在函数内交换这两个数的值后输出x，y
- 测试用例：

```
示例一：
输入：
1 2
输出：
2
1

示例二：
输入：
-1 1000
输出：
1000
-1
```

[slide]

## 第一题 `{:&.moveIn}`

- 代码模板

```javascript
function swap(a,b){
	//请填写代码
}
swap(1,2);
swap(-1,1000);
```

- 答案

```javascript
function swap(a,b){
	var c = a;
	a = b;
	b = c;
	console.log(a);
	console.log(b);
}
swap(1,2);
swap(-1,1000);
```

[slide]

## 第二题

- 题目描述：读入三个整数给a、b、c，然后在函数中交换它们中的数，把a中原来的值给b，把b中原来的值给c，把c中原来的值给a，然后输出a、b、c
- 测试用例：

```
示例一：
输入：
1 2 3
输出：
3
1
2

示例二：
输入：
-1 -500 1000
输出：
1000
-1
-500
```

[slide]

## 第二题 `{:&.moveIn}`

- 代码模板

```javascript
function swap(a,b,c){
	//请填写代码
}
swap(1,2,3);
swap(-1,-500,1000);
```

- 答案

```javascript
function swap(a,b,c){
	var d = a;
	a = c;
	c = b;
	b = d;
	console.log(a);
	console.log(b);
	console.log(c);
}
swap(1,2,3);
swap(-1,-500,1000);
```

[slide]

## 第三题

- 题目描述：输入一个数，判别它是否能被3整除。若能被3整除，打印YES；不能被3整除，打印NO
- 测试用例：

```
示例一：
输入：5
输出：NO

示例二：
输入：0
输出：YES

示例三：
输入：-6
输出：YES

```

[slide]

## 第三题 `{:&.moveIn}`

- 代码模板

```javascript
function division(num){
	//请填写代码
}
division(5);
division(0);
division(-6);
```

- 答案

```javascript
function division(num){
	if(num % 3 == 0){
		console.log("YES");
	}else{
		console.log("NO");
	}
}
division(5);
division(0);
division(-6);
```

[slide]

## 第四题

- 题目描述：计算斐波那契数列，直到某项大于1000为止，并输出该项的值。（斐波那契数列的每一项等于前两项的和，数列的前10项为：1, 1, 2, 3, 5, 8, 13, 21, 34, 55, ...）
- 测试用例：

```
输出：1597
```

[slide]

## 第四题 `{:&.moveIn}`

- 代码模板

```javascript
function fibonacci(){
	//请填写代码
}
fibonacci();
```

- 答案

```javascript
function fibonacci(){
	var arr=[1,1];
	for(var i=2 ; arr[i-1]<=1000;i++){
		arr[i]=arr[i-1]+arr[i-2];
	}
	console.log(arr[arr.length-1]);
}
fibonacci();
```

[slide]

## 第五题

- 题目描述：使用双层for循环打印如下由星号组成的三角图形：

```
*******
*****
***
*
```

[slide]

## 第五题 `{:&.moveIn}`

- 代码模板

```javascript
function triangle(){
	//请填写代码
}
triangle();
```

- 答案

```javascript
function triangle(){
	for(var i=0;i<4;i++){
		var res = '';
		for(var j=7-i*2;j>0;j--){
			res += 'x';
		}
		console.log(res);
	}
}
triangle();
```

[slide]

## 第六题

- 题目描述：实现函数判断一字符串是否是回文。若是回文，则打印1；否则打印0。回文是顺读和倒读都一样的字符串
- 测试用例：

```
示例一：
输入：abcba
输出：1

示例二：
输入：abcac
输出：0

示例三：
输入：ababab
输出：0

示例四：
输入：aaaaaa
输出：1

```

[slide]

## 第六题 `{:&.moveIn}`

- 代码模板

```javascript
function palindrome(str){
	//请填写代码
}
palindrome('abcba');
palindrome('abcac');
palindrome('ababab');
palindrome('aaaaaa');
```

- 答案

```javascript
function palindrome(str){
	var len = str.length;
	for(var i=0; i<len ; i++){
		if(str[i]!=str[len-1-i]){
			console.log(0);
			return
		}
	}
	console.log(1);
}
palindrome('abcba');
palindrome('abcac');
palindrome('ababab');
palindrome('aaaaaa');
```

[slide]

# 感谢倾听