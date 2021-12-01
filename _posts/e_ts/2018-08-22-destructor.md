---
layout:     post
title:      Typescript 析构表达式
summary: 
categories: Ts
technique: true
---

## | 析构表达式

```typescript
function getStock(){
  return {
    code:"IBM",
    price:100
  }
}
var { code , price } = getStock();
// {} 中 code，price 必须与 getStock 返回对象的属性名称相同

// 若更改名字，如下：
var { code: codeX, price } = getStock();

// 获取嵌套对象的属性
function getStock(){
  return {
    code:"IBM",
    price:{
      price1:100,
      price2::200
    }
  }
}
var { code , price:{price2} } = getStock();  // "IBM" 200
// 针对对象的析构表达式用{}，针对数组的用[];   
```

使用泛型指定数组只能放一个类型的数据，不能放其他类型的数据； Array<People>

参数类型推断：第一次赋值时，默认类型。

参数默认值：函数带默认值的参数放最后；可选参数必须放在必选参数后 

