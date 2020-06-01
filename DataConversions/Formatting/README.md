# What is formatting?

A data format is the arrangement of data fields for a specific shape. After you arrange data fields on a shape, you can save the data format as default or custom.

## Example 
For example, take `time` or `date`. 

DATE contains following fields - (day, week, year)
```
Date can be represented in different shapes like 
- (dd-mm-yy) or 
- (dd-mm-yyyy) or
- (MM/DD/YY) or 
- (YY/MM/DD) etc. 
```
These different shapes are called `Formats`.


## How to format?
Every programming language provides methods to create Date in different formats.

```
JAVA --
    Date date = new Date();  
    SimpleDateFormat formatter = new SimpleDateFormat("MM/dd/yyyy");  
    String strDate = formatter.format(date);  
    System.out.println("Date Format with MM/dd/yyyy : "+strDate);  
  
    formatter = new SimpleDateFormat("dd-M-yyyy hh:mm:ss");  
    strDate = formatter.format(date);  
    System.out.println("Date Format with dd-M-yyyy hh:mm:ss : "+strDate);  
```

```
Golang - 
    func main() {
        today := time.Now();
        fmt.Println("today - ", today)
        fmt.Println("format today - ", today.Format("2006-01-02 15:04:05.999999999 -0700 MST"))
    }

    Different available formats - https://golang.org/src/time/format.go
```



- https://www.tenouk.com/Module5.html