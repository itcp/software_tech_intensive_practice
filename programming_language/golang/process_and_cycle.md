

switch ...

```go
   var x interface{}
     
   switch i := x.(type) {
      case nil:  
         fmt.Printf(" x 的类型 :%T",i)                
      case int:  
         fmt.Printf("x 是 int 型")                      
      case float64:
         fmt.Printf("x 是 float64 型")          
      case func(int) float64:
         fmt.Printf("x 是 func(int) 型")                      
      case bool, string:
         fmt.Printf("x 是 bool 或 string 型" )      
      default:
         fmt.Printf("未知型")    
   } 
```



if .. else...

```go
   /* 局部变量定义 */
   var a int = 100;
 
   /* 判断布尔表达式 */
   if a < 20 {
       /* 如果条件为 true 则执行以下语句 */
       fmt.Printf("a 小于 20\n" );
   } else {
       /* 如果条件为 false 则执行以下语句 */
       fmt.Printf("a 不小于 20\n" );
   }
   fmt.Printf("a 的值为 : %d\n", a);
```



for ..

```go
// 如其他编程语言中的 while
var i int = 5
for i >= 0 {
    i = i - 1
    fmt.Printf("The variable i is now: %d\n", i)
}

// continue 语句指向 LABEL1,当执行到该语句的时候,就会跳转到 LABEL1 标签的位置
LABEL1:
for i := 0; i <= 5; i++ {
    for j := 0; j <= 5; j++ {
        if j == 4 {
            continue LABEL1
        }
        fmt.Printf("i is: %d, and j is: %d\n", i, j)
    }
}

// goto 语句通常与条件语句配合使用。可用来实现条件转移， 构成循环，跳出循环体等功能。
func main() {
   var a int = 10

   /* 循环 */
   LOOP: for a < 20 {
      if a == 15 {
         /* 跳过迭代 */
         a = a + 1
         goto LOOP
      }
      fmt.Printf("a的值为 : %d\n", a)
      a++
   }  
}

```



