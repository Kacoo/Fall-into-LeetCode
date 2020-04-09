### 题目描述
给定一个Excel表格中的列名称，返回其相应的列序号。  
例如，  
    A -> 1  
    B -> 2  
    C -> 3  
    ...  
    Z -> 26  
    AA -> 27  
    AB -> 28   
    ...  
### 我的题解
【代码】  
```
/**
 * @param {string} s
 * @return {number}
 */
var titleToNumber = function (s) {
  let map = [
    "A", "B", "C", "D",
    "E", "F", "G", "H",
    "I", "J", "K", "L",
    "M", "N", "O", "P",
    "Q", "R", "S", "T",
    "U", "V", "W", "X",
    "Y", "Z",
  ];
  return s.split("").reduce((prev, cur, curIdx, arr) => {
    let n = map.indexOf(cur) + 1;
    let idx = arr.length - curIdx - 1;
    return prev + n * Math.pow(26, idx);
  }, 0);
};
```
【运行结果】
Accepted  
1000/1000 cases passed (72 ms)  
Your runtime beats 95.52 % of javascript submissions  
Your memory usage beats 18.92 % of javascript submissions (35.7 MB)  
### 我认为比较好的[题解]()
### 结tu语cao
二十六进制转十进制。Kacoo@2020-04-08 周三