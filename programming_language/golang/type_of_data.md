



这个练习有 数据变量、程度结构、函数、方法、接口



vi index.go

```go
package main

import "fmt"
func main(){
    fmt.Println("hi,go")
}
```





```shell
go run index.go  # 直接运行

go build index.go  # 编译后二进制文件运行
./index
```



```go
// 单行注释

/*
func itcp(){
	fmt.Println('no')
}
*/
```



```go
var name str = "itcp"  // 常量
const Pi = 3.14	// 常量


a := 1        // 这种是函数体内的局部变量，但必须被使用
//指针
s := "good bye"
var p *string = &s
*p = "ciao"
fmt.Printf("pointer p: %p\n", p) // prints address
fmt.Printf("string *p: %s\n", *p) // prints string
fmt.Printf("string s: %s\n", s) // prints same string
```



类型

```go
type Celsius float64    // 攝氏溫度
type Fahrenheit float64 // 華氏溫度

const (
	AbsoluteZeroC Celsius = -273.15 // 絶對零度
	FreezingC     Celsius = 0       // 結冰點溫度
	BoilingC      Celsius = 100     // 沸水溫度
)

func CToF(c Celsius) Fahrenheit { return Fahrenheit(c*9/5 + 32) }

func FToC(f Fahrenheit) Celsius { return Celsius((f - 32) * 5 / 9) }
```

