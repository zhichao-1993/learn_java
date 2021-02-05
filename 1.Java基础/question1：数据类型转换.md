   * [数据类型转换问题](#数据类型转换问题)
      * [1.String转char](#1string转char)
      * [2.char转换为String](#2char转换为string)
# 数据类型转换问题
## 1.String转char
1. 使用String.charAt(index)（返回值为char）可以得到String中某一指定位置的char。   
2. 使用String.toCharArray()（返回值为char[]）可以得到将包含整个String的char数组。这样我们就能够使用从0开始的位置索引来访问string中的任意位置的元素。

## 2.char转换为String
1. String s = String.valueOf('c'); //效率最高的方法    

2. String s = String.valueOf(new char[]{'c'}); //将一个char数组转换成String 

3. String s = Character.toString('c');  
// Character.toString(char)方法实际上直接返回String.valueOf(char)    

4. String s = new Character('c').toString();    

5. String s = "" + 'c'; 
// 虽然这个方法很简单，但这是效率最低的方法 
// Java中的String Object的值实际上是不可变的，是一个final的变量。  
// 所以我们每次对String做出任何改变，都是初始化了一个全新的String Object并将原来的变量指向了这个新String。     
// 而Java对使用+运算符处理String相加进行了方法重载。   
// 字符串直接相加连接实际上调用了如下方法： 
// new StringBuilder().append("").append('c').toString();   

6. String s = new String(new char[]{'c'});
