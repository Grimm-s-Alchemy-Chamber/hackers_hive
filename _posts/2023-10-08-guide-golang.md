## Getting Started with Golang (Go)

1. `Installation` Start, by installing the Go programming language on your computer/laptop. You can download the installer from the Go website (`https://golang.org/dl/`). Follow the installation instructions for your specific operating system.

2. `Create your Go program` usually starting with a "Hello World!" example. Open a text editor and write the following code;
   ```
   $ mkdir go_hello_world
   $ cd go_hello_world
   $ go mod init example/hello

   Create a file called "main.go"
   $ touch main.go

   Copy and Paste the below given example 1: show Hello World

   To execute the go
   $ go run main.go
   The output will be:
   Hello World!

- examples
  ```
  // example 1: show Hello World
  
    package main

    import "fmt"

    func main() {
      fmt.Println("Hello World!")
    }
  ```
  ```

  // example 2: calculate the addition and subtraction of two numbers
  
    package main

    import "fmt"

    func main() {
	    a := 10
	    b := 5

	    addition := a + b
	    subtract := a - b

	    fmt.Println("The addition of a & b is", addition)
	    fmt.Println("The subtract of a & b is", subtract)
    }
  ```
  ```
  // example 3: prints numbers from 1 to 5
  
    package main

    import "fmt"

    func main() {
      for i := 1; i <= 5; i++ {
          fmt.Println(i)
      }
    }
  ```

# Fundamental Concepts
| step | name | what needs to be covered |
|----------|----------|----------|
| 1 | Go Basics | Variables, Constants, Conditional Statements | 
| 2 | Data Types | integers, strings, and arrays |
| 3 | Functions | Function declaration and syntax, Function without return value, Function with return value, Function as a variable, Anonymous functions, Higher-order functions,  Variadic functions |
| 4 | data structures | Structs, Arrays, Slices |
| 5 | Loops | for loop, Infinite loop, range loop, Nested loop, Loop Control Statements |
| 6 | Pointers | Memory Address, Declaration, Initialization, Dereferencing, Nil Pointers,  Pointers to Functions, Pointer Arithmetic, Pointers and Slices/Maps, Garbage Collection |
| 7 | Concurrency | Goroutines, Channels, Select Statement, Mutexes, Wait Groups |

# Framework
![go-framework](https://github.com/devkishor8007/hackers_hive/assets/73419211/3bc0c8fb-aef6-453b-aadb-3c541f984ed1)
| id | framework name | website | 
|----------|----------|----------|
| 1 | Gin | https://gin-gonic.com/docs/ |
| 2 | Echo | https://echo.labstack.com/docs/quick-start |
| 3 | Mux | https://github.com/gorilla/mux |
| 4 | Fiber | https://docs.gofiber.io/ |
| 5 | Revel | https://revel.github.io/  |
| 6 | Iris | https://www.iris-go.com/docs/#/ |
| 7 | goji  | https://goji.io/ |
| 8 | buffalo | https://gobuffalo.io/documentation/  |
| 9 | Beego | https://github.com/beego/beego |
| 10 | Martini | https://github.com/go-martini/martini |
| 11 | Go zero | https://github.com/zeromicro/go-zero 

# Resources
| id | topic | website |
|----------|----------|----------|
| 1 | Uber Go Style Guide | https://github.com/uber-go/guide/blob/master/style.md#uber-go-style-guide |
| 2 | Awsome Go | https://github.com/avelino/awesome-go |
| 3 | Go Code Review Comments | https://github.com/golang/go/wiki/CodeReviewComments |
| 4 | Go Standard library | https://pkg.go.dev/std |

# Types Of Project Can be built in Go
| id | name | 
|----------|----------|
| 1 | Web Applications and APIs
| 2 | Microservices |
| 3 | Command-Line Tools |
| 4 | Networking Applications |
| 5 | Blockchain and Cryptocurrency Projects | 
| 6 | System Programming | 
| 7 | IoT (Internet of Things) |

## Tips
To start I recommend referring to the Go website located at [golang](https://golang.org/). It offers documentation and a language tour that will help you begin your journey, with Go. Another useful resource is the Go Tour, which can be accessed at [Go Tour](https://go.dev/tour/list). This interactive platform provides a way to grasp the fundamentals of Go.
            
When choosing on a framework, we have to consider into different aspects including performance, security, community support, documentation and the unique needs of your project. It's also advisable to experiment with frameworks to determine which one suits your coding style and personal preferences the most.
