# What is parsing?

Data parsing is a method where one string of data gets converted into a different type of data. So let's say you receive your data in raw HTML, a parser will take the said HTML and transform it into a more readable data format that can be easily read and understood.


Value of some other data type is stored as string.
Taking input from a string and returning some other data type is called parsing.

### Examples
#### Parsing an integer
An example would be the parseInt() function. It would take an input such as "123", which would be a string consisting of the char values 1, 2, and 3. Then it would convert this value to the integer 123, which is a simple number that can be stored and manipulated as an integer.

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

