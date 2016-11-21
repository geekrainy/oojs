# oojs

## 第 2 章 基本数据类型、数组、循环及条件表达式

### 字符串转换

将数字字符串转换为数字：

```javascript
var s = "1994";
typeof s;  // "string"
s = s * 1;
typeof s;  // "number"
```

将其他类型转换为字符串：

```javascript
var n = 1994;
typeof n;  // "number"
n = n + "";
typeof n;  // "string"
```

### 逻辑运算符转换

> falsy 值："", null, undefined, 0, NaN, false

#### 惰性求值

```javascript
true || false || true;  // true

var a = 1;
true || (a = 2);  // true
a;  // 1
true && (a = 2);  // 2
a;  // 2

var a = a || 3;
a;  // 2

// 当变量值为 falsy 值，总是会被赋予候补值
a = 0;
var a = a || 3;
a;  // 3

var b = b || 3;
b;  // 3

var b = null || 4;
b;  // 4
```

#### 转换任何值为 Boolean 值

```javascript
!!null;  // false
!!"string";  // true
!!1994;  // true
```

