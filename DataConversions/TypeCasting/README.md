# What is TypeCasting?
Type conversion or typecasting refers to changing an entity of one datatype into another.




# Two common casting styles
There are two common casting styles, each outlined below.

C-style casting
This style of casting is used in C and Java. It follows the form:

                    (type)expression

C++-style casting

Several cast syntaxes are used in C++ (although C-style casting is supported as well). The function-call style follows the form:

                    type(expression)



## Examples

```
Golang - The expression T(v) converts the value v to the type T.

package main

import (
	"fmt"
)

func main() {
	i := 42
	fmt.Printf("%v, %T",i, i)
	f := float64(i)
	fmt.Printf("%v, %T",f, f)
}


https://tour.golang.org/basics/13
```

```
JAVA

public class MyClass {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);
    System.out.println(myDouble);
  }
}

public class MyClass {
  public static void main(String[] args) {
    double myDouble = 9.78;
    int myInt = (int) myDouble; // Explicit casting: double to int

    System.out.println(myDouble);
    System.out.println(myInt);
  }
}

https://www.w3schools.com/java/java_type_casting.asp

```