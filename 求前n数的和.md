### 题目描述
> 求1+2+3+...+n，要求不能使用乘除法、for、while、if、else、switch、case等关键字及条件判断语句（A?B:C）。

### 代码
```
function SumSolution(n) {
  return n && Sum_Solution(n - 1) + n;
}
```