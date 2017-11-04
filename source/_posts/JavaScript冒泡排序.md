---
title: JavaScript实现冒泡排序算法
tags: JavaScript
categories: web前端
---


## 算法原理
 对相邻的数进行两两比较，如果第一个比第二个大，就交换他们两个。小数在前，大数在后，这样一趟下来，最小的数就被排在了第一位，第二趟也是如此，如此类推，直到所有的数据排序完成。

 ![冒泡排序动画效果][1]
 
 ## 算法步骤
1.  比较相邻的元素。如果第一个比第二个大，就交换他们两个。
2. 对每一对相邻元素作同样的工作，从开始第一对到结尾的最后一对。这时，最后的元素应该会是最大的数。
4. 针对所有的元素重复以上的步骤，除了最后一个。
5. 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。
## 代码实现

``` stylus
function sortarr(arr){
    for(i=0;i<arr.length-1;i++){
        for(j=0;j<arr.length-1-i;j++){
            if(arr[j]>arr[j+1]){      //相邻元素比较
                var temp=arr[j];     //交换位置 
                arr[j]=arr[j+1];
                arr[j+1]=temp;
            }
        }
    }
    return arr;
}
var examplearr=[3,84,55,78,72,69,98,17];
sortarr(examplearr);
console.log(examplearr);
alert(examplearr);
```


  [1]: https://i.loli.net/2017/11/02/59fb19580a409.gif