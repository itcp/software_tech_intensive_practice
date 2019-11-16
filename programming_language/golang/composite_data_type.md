

复合数据类型



```go
// 数组
var q [3]int = [3]int{1,2,3}
boev := [...]string{NAME: "boev", AGE: "30", RULE: "coder"}
fmt.Println(RULE, boev[RULE])
fmt.Println(boev[1:])  // 切片

// Map
ages := map[string]int{
	"alice":   31,
	"charlie": 34,
}
fmt.Println(ages["alice"])

// 结构体
type Employee struct {	// 定义结构体类型
	ID        int
	Name      string
	Address   string
	DoB       time.Time
}
var dilbert Employee   // 声明结构体变量
dilbert.Name = "itcp"
dob := &dilbert.DoB
*dob = time.Now().UTC()


```



JSON

```go

```



文本和HTML模板

```go

```



------



函数与方法



```go
// traditional function
func Distance(p, q Point) float64 {
    return math.Hypot(q.X-p.X, q.Y-p.Y)
}


// same thing, but as a method of the Point type
func (p Point) Distance(q Point) float64 {
    return math.Hypot(q.X-p.X, q.Y-p.Y)
}

```



```go
package main
import (
	"fmt"
)

type Shape interface {
    Area() float64
    Perimeter() float64
}

type Rect struct {
    width float64
    height float64
}

func (r Rect) Area() float64 {
    return r.width * r.height
}

func (r Rect) Perimeter() float64{
    return 2 * (r.width + r.height)
}

func main(){
    var s Shape
    s = Rect{5.0, 4.0}
    r := Rect{5.0, 4.0}
    fmt.Printf("type %T\n", s)
    fmt.Printf("value s %v\n", s)
    fmt.Println("area", s.Area())
    fmt.Println("s == r", s == r)
}

```



