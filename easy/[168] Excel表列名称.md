### 题目描述(2020-04-03)
给定一个正整数，返回它在 Excel 表中相对应的列名称。  
例如，  
    1 -> A  
    2 -> B  
    3 -> C  
    ...  
    26 -> Z  
    27 -> AA  
    28 -> AB   
    ...  
### 我的题解
【代码】  
```
/**
 * @param {number} n
 * @return {string}
 */
var convertToTitle = function (n) {
  let result = "";
  let map = [
    "A", "B", "C", "D", "E",
    "F", "G", "H", "I", "J",
    "K", "L", "M", "N", "O",
    "P", "Q", "R", "S", "T",
    "U", "V", "W", "X", "Y",
    "Z",
  ];
  while (n > 0) {
    --n;
    let temp = n % 26;
    n = Math.floor(n / 26);
    result = map[temp] + result;
  }
  return result;
};
```
【运行结果】
Accepted  
18/18 cases passed (60 ms)  
Your runtime beats 74.64 % of javascript submissions  
Your memory usage beats 68.18 % of javascript submissions (33.8 MB)  
### 我认为比较好的[题解]()
也可以用递归做。  
【】  
### 结tu语cao
简单题，26进制。  
但也要注意一些坑。复习一下Math的函数吧。Kacoo@2020-04-07 周二