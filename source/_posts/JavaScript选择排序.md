---
title: JavaScript实现选择排序算法
tags: JavaScript
categories: web前端
---

## 算法原理
首先在未排序序列中找到最小元素，存放到排序序列的起始位置，然后，再从剩余未排序元素中继续寻找最小元素，然后放到已排序序列末尾。以此类推，直到所有元素均排序完毕。


![选择排序动画效果][1]


## 算法步骤
1. 第一次遍历中，找到最小的数组元素然后用第一个数组元素交换它。

2. 第二次遍历中，找到第二小的数组元素然后用第二个数组元素交换它。
3. 依次类推。如果包含N个元素，那么将在最多N-1次遍历之后完成排序。


## 代码实现

``` stylus
var arr=[6,82,55,78,72,69,98,17];
function selectionSort(arr) {
    var len = arr.length;
    var minIndex, temp;
    for (var i = 0; i < len - 1; i++) {
        minIndex = i;
        for (var j = i + 1; j < len; j++) {
            if (arr[j] < arr[minIndex]) {     // 寻找最小的数
                minIndex = j;                 // 将最小数的索引保存
            }
        }
        temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;
    }
    return arr;
}
selectionSort(arr)
console.log(arr);
alert(arr);
```



  [1]: https://i.loli.net/2017/11/03/59fc796389504.gif