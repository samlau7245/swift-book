
# 常量、变量

* `let`: 用来声明常量。
* `var`: 用来声明变量。

```swift
let PI = 3.14
var name = 10

// 声明多个常量
let a = 1, b = 2, c = 3
// 声明多个变量
var x = 1, y = 2, z = 3
```

## 类型注解(type annotation)

类型注解: 用于说明常量或者变量中要存储的值的类型。

```swift
func func_1() {
    var welcomeMessage: String // 冒号代表着“是...类型” -> 声明一个类型为 String ，名字为 welcomeMessage 的变量。
    var v1, v2, v3: Double // 一行中定义多个同样类型的变量
}

// 声明全局变量的时候使用类型注解需要有默认值。
// Global 'var' declaration requires an initializer expression or getter/setter specifier
// var var_name: String
```

# 类型

Swift 是一个类型安全的语言。

类型判断

## 基础类型

### 整数

| 类型 | 符号类型 |最小值 | 最大值 |
| --- | --- | --- | --- |
| `Int` | 有符号| `Int.min` | `Int.max` |
| `Int16`| 有符号| `Int16.min` |`Int16.max` |
| `Int32` | 有符号| `Int32.min` | `Int32.max` |
| `Int64` | 有符号| `Int64.min` | `Int64.max` |
| `UInt` | 无符号| `UInt.min` | `UInt.max` |
| `UInt16` | 无符号| `UInt16.min` | `UInt16.max` |
| `UInt32` | 无符号| `UInt32.min` | `UInt32.max` |
| `UInt64` | 无符号| `UInt64.min` | `UInt64.max` |

> 尽量不要使用 `UInt`，除非你真的需要存储一个和当前平台原生字长相同的无符号整数。除了这种情况，最好使用 `Int`，即使你要存储的值已知是非负的。

### 浮点数

| 类型 | 位数
| --- | --- |
| `Double` | 64位浮点数 |
| `Float` | 32位浮点数 |

> `Double` 精确度很高，至少有 `15` 位小数，而 `Float` 只有 `6` 位小数。选择哪个类型取决于你的代码需要处理的值的范围，在两种类型都匹配的情况下，将优先选择 `Double`。

### 布尔值(Bool)

* `Bool`: `true` 和 `false`。

```swift
let sexIsMan = true
    
if sexIsMan {
    print("Men")
} else {
    print("Women")
}
```

> 这里的布尔值类型和OC不一样的地方，OC可以通过数字`0|1`来代替`true` 和 `false`,Swift不行。

```swift
let i = 1
if i {
    // 这个例子不会通过编译，会报错
}
```

### 元组(tuples)

`元组(tuples)`把多个值组合成一个复合值。元组内的值可以是任意类型，并不要求是相同类型。

```swift
let http404Error = (404, "Not Found")
```

### 类型安全(type safe)

`Swift`是一个类型安全的语言，让你清楚的知道代码处理的值的类型；Xcode会在编译代码的时候进行`类型检查`，并且把不匹配的类型标记错误。

### 类型推断

如果没有显示的指定类型时，Swift会通过常量或者变量的赋值来进行类型推断。

```swift
let meaningOfLife = 42 // 常量 meaningOfLife 会被推测为 Int 类型
let pi = 3.14159 // 常量 pi 会被推测为 Double 类型
```

> 当推断浮点数的类型时，Swift 总是会选择 `Double` 而不是 `Float`。

### 数值型字面量

* 一个十进制数，没有前缀。
* 一个二进制数，前缀是 `0b`。
* 一个八进制数，前缀是 `0o`。
* 一个十六进制数，前缀是 `0x`。

```swift
let decimalInteger = 17           // 十进制的17
let binaryInteger = 0b10001       // 二进制的17
let octalInteger = 0o21           // 八进制的17
let hexadecimalInteger = 0x11     // 十六进制的17
```

## 集合类型

































