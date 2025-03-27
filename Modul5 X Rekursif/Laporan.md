<h1 align="center" > Laporan Praktikum Modul 5 X Rekursif</h1>
___
<p align="center">Julian Saputra - 103112400260</p>
___

Soal 1 :
```go
package main

import "fmt"

func fibonacci(n int) int {
    if n == 0 {
        return 0
    } else if n == 1 {
        return 1
    } else {
        return fibonacci(n-1) + fibonacci(n-2)
    }
}

func main() {
    for i := 0; i <= 10; i++ {
        fmt.Printf("Fibonacci(%d) = %d\n", i, fibonacci(i))
    }
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal1.png)

___

Soal 2 :
```go
package main

import "fmt"

func printStars(n int) {
    if n == 0 {
        return
    }
    fmt.Print("*")
    printStars(n - 1)
}

func printPattern(n, current int) {
    if current > n {
        return
    }
    printStars(current)
    fmt.Println()      
    printPattern(n, current+1)
}

func main() {
    var n int
    for {
        fmt.Print("Masukkan nilai N : ")
        fmt.Scan(&n)
        printPattern(n, 1)
        fmt.Println()
    }
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal2.png)

___

Soal 3 :
```go
package main

import "fmt"

func findFactors(n, i int) {
    if i > n {
        return
    }
    if n%i == 0 {
        fmt.Print(i, " ")
    }
    findFactors(n, i+1)
}

func main() {
    var n int
    fmt.Print("Masukkan bilangan N: ")
    fmt.Scan(&n)

    fmt.Print("Faktor dari ", n, ": ")
    findFactors(n, 1)
    fmt.Println()
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal3.png)

___

Soal 4 : 
```go
package main

import "fmt"

func printDescending(n, current int) {
    if current < 1 {
        return
    }
    fmt.Print(current, " ")
    printDescending(n, current-1)
}

func printAscending(n, current int) {
    if current > n {
        return
    }
    fmt.Print(current, " ")
    printAscending(n, current+1)
}
 
func main() {
    var n int
    fmt.Print("Masukkan bilangan N: ")
    fmt.Scan(&n)

    printDescending(n, n)
    printAscending(n, 2)

    fmt.Println()
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal4.png)

___

Soal 5 : 
```go
package main

import "fmt"

func printOddNumbers(n, current int) {
    if current > n {
        return
    }
    fmt.Print(current, " ")
    printOddNumbers(n, current+2)
}

func main() {
    var n int
    fmt.Print("Masukkan bilangan N: ")
    fmt.Scan(&n)

    fmt.Print("Bilangan ganjil dari 1 hingga ", n, ": ")
    printOddNumbers(n, 1)
    fmt.Println()
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal5.png)

___

Soal 6 : 
```go
package main

import "fmt"

func power(x, y int) int {
    if y == 0 {
        return 1
    }
    return x * power(x, y-1)
}

func main() {
    var x, y int
    fmt.Print("Masukkan bilangan x dan y: ")
    fmt.Scan(&x, &y)
  
    result := power(x, y)
    fmt.Printf("Hasil %d pangkat %d adalah: %d\n", x, y, result)
}
```

Output : 
![](Modul5%20X%20Rekursif/output/Soal6.png)

