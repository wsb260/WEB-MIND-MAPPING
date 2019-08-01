### 1.写一个方法把下划线命名转成大驼峰命名

```
// 1.传入参数,判断字符串类型,非返回
// 2.通过split('_')把字符串分割成数组
// 3.遍历数组把每一项开头转换成大写字母,并把每一项都拼接到一起
// 4.返回字符串
function changeStr(str){
  let arr = [];
  let newStr = '';
  if(!str||str===' '|| typeof str !== 'string'){
    return false;
  }
 arr = str.split('_');
 arr.map(item => {
   if(item){ //过滤空字符
      newStr += item.substr(0,1).toUpperCase()+item.substr(1)
   }
 });
 console.log(newStr);
}
changeStr('_abc_ghe_nb_w_') // 输出:AbcGheNbW
```
### 2.写一个把字符串大小写切换的方法
```
// 1.test() 方法用于检测一个字符串是否匹配某个模式,返回Boolean值
// 2.toUpperCase() 转换成大写,toLowerCase()转换成小写
function changeStr(str){
  let ary = [];
  let newStr = '';
  if(!str||str === ''||typeof str !== 'string'){
    return false;
  }
  ary = str.split("");
  ary.map(item => {
    newStr += /[A-Z]/.test(item) ? item.toLowerCase() : item.toUpperCase();
  })
  console.log(newStr)
}

changeStr('aAbBcC') // 输出:AaBbCb
```
```
//$1、$2、...、$99与 regexp 中的第 1 到第 99 个子表达式相匹配的文本
//function（a,b,c）一共可以传入3个参数，第一个为匹配到的字符串，第二个为匹配字符串的起始位置，第三个为调用replace方法的字符串本身,(非全局匹配的情况下/g),下例为多组匹配,s1,s2分别对应$1,$2
function caseConvert(str){
  return str.replace(/([a-z]*)([A-Z]*)/g, function(m,s1,s2){
    return s1.toUpperCase() + s2.toLowerCase()
  })
}
console.log(caseConvert('aSa')) //AsA
```

### 3.统计某一字符或字符串在另一个字符串中出现的次数
```
// 方法1
var str = 'aabbcaacddaabbccdd'
var str2 = 'aa'

const contSvg = (s1,s2) => {
  var arr = [];
  arr = s1.split(s2);
  console.log(arr.length-1);
}

contSvg(str,str2) // 输出3
// 方法2
// eval() 函数可计算某个字符串，并执行其中的的 JavaScript 代码。
const strCount = (str, target) => {
  if (!target) return count
	 return  str.match(eval("/"+target+"/g")).length
}

console.log(strCount('abcdef abcdef a', 'abc')) // 输出2
```
