# What is parsing?

Data parsing is a method where one string of data gets converted into a different type of data. So let's say you receive your data in raw HTML, a parser will take the said HTML and transform it into a more readable data format that can be easily read and understood.


Value of some other data type is stored as string.
Taking input from a string and returning some other data type is called parsing.

### Examples
#### Parsing an integer
An example would be the parseInt() function. It would take an input such as "123", which would be a string consisting of the char values 1, 2, and 3. Then it would convert this value to the integer 123, which is a simple number that can be stored and manipulated as an integer.

```
Golang
    i, err := strconv.Atoi("-42")
    s := strconv.Itoa(-42)
    b, err := strconv.ParseBool("true")
    f, err := strconv.ParseFloat("3.1415", 64)
    i, err := strconv.ParseInt("-42", 10, 64)
    u, err := strconv.ParseUint("42", 10, 64)
```

```
Java
    public static void main(String args[]) 
    { 
        int decimalExample = Integer.parseInt("20"); 
        int signedPositiveExample = Integer.parseInt("+20"); 
        int signedNegativeExample = Integer.parseInt("-20"); 
        int radixExample = Integer.parseInt("20",16); 
        int stringExample = Integer.parseInt("geeks",29); 
  
        // Uncomment the following code to check 
        // NumberFormatException 
  
        //   String invalidArguments = ""; 
        //   int emptyString = Integer.parseInt(invalidArguments); 
        //   int outOfRangeOfInteger = Integer.parseInt("geeksforgeeks",29); 
        //   int domainOfNumberSystem = Integer.parseInt("geeks",28); 
  
        System.out.println(decimalExample); 
        System.out.println(signedPositiveExample); 
        System.out.println(signedNegativeExample); 
        System.out.println(radixExample); 
        System.out.println(stringExample); 
    }

    https://www.geeksforgeeks.org/string-to-integer-in-java-parseint/#:~:text=The%20method%20generally%20used%20to,as%20a%20signed%20decimal%20integer.
```

#### Parsing a date 
Here is a better example involving parsing a date from a string:

``` 
SimpleDateFormat format = new SimpleDateFormat("yyyy-MM-dd");
Date date = format.parse("2016-04-23");
```
This example shows a date format that actually has recognizable parts:

- yyyy is the year
- "- is a literal dash"
- MM is the month
- "- is another literal dash"
- dd is the day



### Usages
- Parsing is majorly used in compiler design.
- 

### References
- https://www.sohamkamani.com/blog/2017/10/18/parsing-json-in-golang/#:~:text=For%20any%20JSON%20string%2C%20the,%26myStoredVariable)%20%2F%2F...