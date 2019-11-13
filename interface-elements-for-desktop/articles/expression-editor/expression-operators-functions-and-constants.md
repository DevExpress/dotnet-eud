---
title: Expression Operators, Functions and Constants
author: Alexey Zolotarev
legacyId: 8406
---
# Expression Operators, Functions and Constants
This topic lists operators and functions supported by the [Expression Editor](../expression-editor.md). It also provides information on how constants can be specified in expressions.

The following DevExpress products extend and/or override this syntax. The table below lists the articles that explain how to use expressions in these products.

|Product | Article |
|---|---|
|Reporting	| [Expression Constants, Operators, and Functions](../report-designer/report-designer-for-winforms/use-expressions/expression-syntax.md)
|Pivot Grid	| [Pivot Grid Expression Syntax](../pivot-table/data-editing/pivot-grid-expression-syntax.md)

## Operators
| Operator | Description | Example |  XLS(x) Format Export-Friendly [*See Note](#note---restrictions)| 
|---|---|---|---|
| + | Adds the value of one numeric expression to another, or concatenates two strings. | [FirstName] + ' ' + [LastName];  [UnitPrice] + 4 |  Yes |
| - | Finds the difference between two numbers. | [Price1] - [Price2] |  Yes |
| * | Multiplies the value of two expressions. | [Quantity] * [UnitPrice] * (1 - [BonusAmount]) |  Yes |
| / | Divides the first operand by the second. | [Quantity] / 2 |  Yes |
| % | Returns the remainder (modulus) obtained by dividing one numeric expression into another. | [Quantity] % 3 |  Yes |
| \| | Compares each bit of its first operand to the corresponding bit of its second operand. If either bit is 1, the corresponding result bit is set to 1. Otherwise, the corresponding result bit is set to 0. |  [Number] \| [Number] |  Yes |
| &amp; | Performs a bitwise logical AND operation between two integer values. | [Number] &amp; 10 |  Yes |
| ^ | Performs a logical exclusion on two Boolean expressions, or a bitwise exclusion on two numeric expressions. | [Number1] ^ [Number2] |  Yes |
| == (as well as =) | Returns true if both operands have the same value; otherwise, it returns false. | [Quantity] == 10 (as well as [ID] = 11) |  Yes |
| != | Returns true if the operands do not have the same value; otherwise, it returns false. | [Country] != 'France' |  Yes |
| &lt; | Less than operator. Used to compare expressions. | [UnitPrice] &lt; 20 |  Yes |
| &lt;= | Less than or equal to operator. Used to compare expressions. | [UnitPrice] &lt;= 20 |  Yes |
| &gt;= | Greater than or equal to operator. Used to compare expressions. | [UnitPrice] &gt; 30 |  Yes |
| &gt; | Greater than operator. Used to compare expressions. | [UnitPrice] &gt;= 30 |  Yes |
| In (,,,) | Tests for the existence of a property in an object. | [Country] In ('USA', 'UK', 'Italy') |  Yes |
| Like | Compares a string against a pattern. If the value of the string matches the pattern, result is true. If the string does not match the pattern, result is false. If both string and pattern are empty strings, the result is true. | [Name] Like 'An%' |  Yes |
| Between (,) | Specifies a range to test. Returns true if a value is greater than or equal to the first operand and less than or equal to the second operand. | [Quantity] Between (10, 20) |  Yes |
| And | Performs a logical conjunction on two expressions. | [InStock] And ([ExtendedPrice]> 100) |  Yes |
| Or | Performs a logical disjunction on two Boolean expressions. | [Country]=='USA' Or [Country]=='UK' |  Yes |
| Not | Performs logical negation on an expression. | Not [InStock] |  Yes |
| + | Returns a numeric expression's value (a unary operator). | +[Value] = 10|  Yes |
| - | Returns the negative of a numeric expression's value (a unary operator). | -[Value] = 20|  Yes |
| ~ | Performs a bitwise negation on a numeric expression.| ~[Roles] = 251 | - |
| Is null | Returns true if an expression is a null reference, the one that does not refer to any object. | [Region] is null | yes |

## Functions

**Aggregate Functions**

| Function | Description | Example |  XLS(x) Format Export-Friendly [*See Note](#note---restrictions) | 
|---|---|---|---|
| Avg(Value) | Evaluates the average of the values in the collection.| [Products].Avg([UnitPrice])| - |
| Count() | Returns the number of objects in a collection. | [Products].Count() | - |
| Exists() | Determines whether the object exists in the collection. | [Categories][[CategoryID] == 7].Exists() | - |
| Max(Value) | Returns the maximum expression value in a collection. | [Products].Max([UnitPrice]) | - |
| Min(Value) | Returns the minimum expression value in a collection. | [Products].Min([UnitPrice]) | - |
| Single() | Returns a single object from a collection that contains no more than one object. If the collection contains more objects, use the Condition property to specify a condition. The collection must contain only one object that satisfies the condition; otherwise, the function's behavior  is undefined (the function may return an unexpected value or throw an exception). You can pass an expression as a parameter: _[Collection][Condition].Single(Expression)_. The function returns the Expression value evaluated on an object that meets the specified _Condition (optional)_. | [Accounts].Single() is not null [Collection].Single([Property1]) - returns the found object's property value. | - |        
| Sum(Value) | Returns the sum of all the expression values in the collection. | [Products].Sum([UnitsInStock]) | - |
| A custom aggregate function | Returns a custom expression value for a collection, according to a custom aggregate function. You can call the function directly or pass it as a parameter.| Call a Custom Aggregate Function | - |

**Date-time Functions**

| Function | Description | Example | XLS(x) Format Export-Friendly [*See Note](#note---restrictions) |
|---|---|---|---|
| AddDays(DateTime, DaysCount) | Returns a date-time value that is the specified number of days away from the specified DateTime. | AddDays([OrderDate], 30) |  Yes |
| AddHours(DateTime, HoursCount) | Returns a date-time value that is the specified number of hours away from the specified DateTime. | AddHours([StartTime], 2) |  Yes |
| AddMilliSeconds(DateTime, MilliSecondsCount) | Returns a date-time value that is the specified number of milliseconds away from the specified DateTime. | AddMilliSeconds(([StartTime], 5000)) |  - |
| AddMinutes(DateTime, MinutesCount) | Returns a date-time value that is the specified number of minutes away from the specified DateTime. | AddMinutes([StartTime], 30) |  Yes |
| AddMonths(DateTime, MonthsCount) | Returns a date-time value that is the specified number of months away from the specified DateTime. | AddMonths([OrderDate], 1) |  Yes |
| AddSeconds(DateTime, SecondsCount) | Returns a date-time value that is the specified number of seconds away from the specified DateTime. | AddSeconds([StartTime], 60) |  Yes |
| AddTicks(DateTime, TicksCount) | Returns a date-time value that is the specified number of ticks away from the specified DateTime. | AddTicks([StartTime], 5000) |  - |
| AddTimeSpan(DateTime, TimeSpan) | Returns a date-time value that is away from the specified DateTime for the given TimeSpan. | AddTimeSpan([StartTime], [Duration]) |  - |
| AddYears(DateTime, YearsCount) | Returns a date-time value that is the specified number of years away from the specieid DateTime. | AddYears([EndDate], -1) |  Yes |
| DateDiffDay(startDate, endDate) | Returns the number of day boundaries between two non-nullable dates. | DateDiffDay([StartTime], Now()) | Yes |  
| DateDiffHour(startDate, endDate) | Returns the number of hour boundaries between two non-nullable dates. | DateDiffHour([StartTime], Now()) | Yes |  
| DateDiffMilliSecond(startDate, endDate) | Returns the number of millisecond boundaries between two non-nullable dates. | DateDiffMilliSecond([StartTime], Now()) | - |  
| DateDiffMinute(startDate, endDate) | Returns the number of minute boundaries between two non-nullable dates. | DateDiffMinute([StartTime], Now()) | Yes |  
| DateDiffMonth(startDate, endDate) | Returns the number of month boundaries between two non-nullable dates. | DateDiffMonth([StartTime], Now()) | Yes |  
| DateDiffSecond(startDate, endDate) | Returns the number of second boundaries between two non-nullable dates. | DateDiffSecond([StartTime], Now()) | Yes |  
| DateDiffTick(startDate, endDate) | Returns the number of tick boundaries between two non-nullable dates. | DateDiffTick([StartTime], Now()) | - |  
| DateDiffYear(startDate, endDate) | Returns the number of year boundaries between two non-nullable dates. | DateDiffYear([StartTime], Now()) | Yes |  
| GetDate(DateTime) | Extracts a date from the defined DateTime. | GetDate([OrderDateTime]) | 
| GetDay(DateTime) | Extracts a day from the defined DateTime. | GetDay([OrderDate]) |  Yes |
| GetDayOfWeek(DateTime) | Extracts a day of the week from the defined DateTime. | GetDayOfWeek([OrderDate]) |  Yes |
| GetDayOfYear(DateTime) | Extracts a day of the year from the defined DateTime. | GetDayOfYear([OrderDate]) |  Yes |
| GetHour(DateTime) | Extracts an hour from the defined DateTime. | GetHour([StartTime]) |  Yes |
| GetMilliSecond(DateTime) | Extracts milliseconds from the defined DateTime. | GetMilliSecond([StartTime]) | - |
| GetMinute(DateTime) | Extracts minutes from the defined DateTime. | GetMinute([StartTime]) |  Yes |
| GetMonth(DateTime) | Extracts a month from the defined DateTime. | GetMonth([StartTime]) |  Yes |
| GetSecond(DateTime) | Extracts seconds from the defined DateTime. | GetSecond([StartTime]) |  Yes |
| GetTimeOfDay(DateTime) | Extracts the time of the day from the defined DateTime, in ticks. | GetTimeOfDay([StartTime]) |  - |
| GetYear(DateTime) | Extracts a year from the defined DateTime. | GetYear([StartTime]) |  Yes |
| IsApril(DateTime) | Returns True if the specified date falls within April. | IsApril([OrderDate]) | Yes |
| IsAugust(DateTime) | Returns True if the specified date falls within August. | IsAugust([OrderDate]) | Yes |
| IsDecember(DateTime) | Returns True if the specified date falls within December. | IsDecember([OrderDate]) | Yes |
| IsFebruary(DateTime) | Returns True if the specified date falls within February. | IsFebruary([OrderDate]) | Yes |
| IsJanuary(DateTime) | Returns True if the specified date falls within January. | IsJanuary([OrderDate]) | Yes |
| IsJuly(DateTime) | Returns True if the specified date falls within July. | IsJuly([OrderDate]) | Yes |
| IsJune(DateTime) | Returns True if the specified date falls within June. | IsJune([OrderDate]) | Yes |
| IsLastMonth(DateTime) | Returns True if the specified date falls within the previous month. | IsLastMonth([OrderDate]) | Yes |
| IsLastYear(DateTime) | Returns True if the specified date falls within the previous year. | IsLastYear([OrderDate]) | Yes |
| IsMarch(DateTime) | Returns True if the specified date falls within March. | IsMarch([OrderDate]) | Yes |
| IsMay(DateTime) | Returns True if the specified date falls within May. | IsMay([OrderDate]) | Yes |
| IsNextMonth(DateTime) | Returns True if the specified date falls within the next month. | IsNextMonth([OrderDate]) | Yes |
| IsNextYear(DateTime) | Returns True if the specified date falls within the next year. | IsNextYear([OrderDate]) | Yes |
| IsNovember(DateTime) | Returns True if the specified date falls within November. | IsNovember([OrderDate]) | Yes |
| IsOctober(DateTime) | Returns True if the specified date falls within October. | IsOctober([OrderDate]) | Yes |
| IsSameDay(DateTime) | Returns True if the specified date/time values fall within the same day. | IsSameDay([OrderDate]) | Yes |
| IsSeptember(DateTime) | Returns True if the specified date falls within September. | IsSeptember([OrderDate]) | Yes |
| IsThisMonth(DateTime) | Returns True if the specified date falls within the current month. | IsThisMonth([OrderDate]) | Yes |
| IsThisWeek(DateTime) | Returns True if the specified date falls within the current week. | IsThisWeek([OrderDate]) | Yes |
| IsYearToDate(DateTime) | Returns True if the specified date falls within the year-to-date period. This period starts from the first day of the current year and continues to the current date (including the current date).| IsYearToDate([OrderDate]) | Yes |
| IsThisYear(DateTime) | Returns True if the specified date falls within the current year. | IsThisYear([OrderDate]) | Yes |
| LocalDateTimeDayAfterTomorrow() | Returns a date-time value corresponding to the day after Tomorrow. | AddDays(LocalDateTimeDayAfterTomorrow(), 5) | Yes |
| LocalDateTimeLastMonth() | Returns the DateTime value corresponding to the first day of the previous month. | AddMonths(LocalDateTimeLastMonth(), 5) | Yes |
| LocalDateTimeLastWeek() | Returns a date-time value corresponding to the first day of the previous week. | AddDays(LocalDateTimeLastWeek(), 5) | Yes |
| LocalDateTimeLastYear() | Returns the DateTime value corresponding to the first day of the previous year. | AddYears(LocalDateTimeLastYear(), 5) | Yes |
| LocalDateTimeNextMonth() | Returns a date-time value corresponding to the first day of the next month. | AddMonths(LocalDateTimeNextMonth(), 5) | Yes |
| LocalDateTimeNextWeek() | Returns a date-time value corresponding to the first day of the following week. | AddDays(LocalDateTimeNextWeek(), 5) | Yes |
| LocalDateTimeNextYear() | Returns a date-time value corresponding to the first day of the following year. | AddYears(LocalDateTimeNextYear(), 5) | Yes |
| LocalDateTimeNow() | Returns a date-time value corresponding to the current moment in time. | AddDays(LocalDateTimeNow(), 5) | Yes |
| LocalDateTimeThisMonth() | Returns a date-time value corresponding to the first day of the current month. | AddMonths(LocalDateTimeThisMonth(), 5) | Yes |
| LocalDateTimeThisWeek() | Returns a date-time value corresponding to the first day of the current week. | AddDays(LocalDateTimeThisWeek(), 5) | Yes |
| LocalDateTimeThisYear() | Returns a date-time value corresponding to the first day of the current year. | AddYears(LocalDateTimeThisYear(), 5) | Yes |
| LocalDateTimeToday() | Returns a date-time value corresponding to Today. | AddDays(LocalDateTimeToday(), 5) | Yes |
| LocalDateTimeTomorrow() | Returns a date-time value corresponding to Tomorrow. | AddDays(LocalDateTimeTomorrow(), 5) | Yes |
| LocalDateTimeTwoMonthsAway() | Returns the DateTime value corresponding to the first day of the following month. | AddMonths(LocalDateTimeTwoMonthAway(), 5) | Yes |
| LocalDateTimeTwoWeeksAway() | Returns the DateTime value corresponding to the first day of the following week. | AddDays(LocalDateTimeTwoWeeksAway(), 5) | Yes |
| LocalDateTimeTwoYearsAway() | Returns the DateTime value corresponding to the first day of the following year. | AddYears(LocalDateTimeTwoYearsAway(), 5) | Yes |
| LocalDateTimeYearBeforeToday() | Returns the DateTime value corresponding to the day one year ago. | AddYears(LocalDateTimeYearBeforeToday(), 5) | Yes |
| LocalDateTimeYesterday() | Returns a date-time value corresponding to Yesterday. | AddDays(LocalDateTimeYesterday(), 5) | Yes |
| Now() | Returns the current system date and time. | AddDays(Now(), 5) |  Yes |
| Today() | Returns the current date. Regardless of the actual time, this function returns midnight of the current date. | AddMonths(Today(), 1) |  Yes |
| UtcNow() | Returns the current system date and time, expressed as Coordinated Universal Time (UTC). | AddDays(UtcNow(), 7) |  - |

**Logical Functions**

| Function | Description | Example |  XLS(x) Format Export-Friendly [*See Note](#note---restrictions) |
|---|---|---|---| 
| Iif(Expression1, True_Value1, ..., ExpressionN, True_ValueN, False_Value) | Returns one of several specified values depending upon the values of logical expressions. The function can take 2N+1 arguments (N - the number of specified logical expressions): each odd argument specifies a logical expression; each even argument specifies the value that is returned if the previous expression evaluates to true. | Iif(Name = 'Bob', 1, 0) Iif(Name = 'Bob', 1, Name = 'Dan', 2, Name = 'Sam', 3, 0) |  Yes |
| IsNull(Value) | Returns True if the specified Value is NULL. | IsNull([OrderDate]) |  Yes |
| IsNull(Value1, Value2) | Returns Value1 if it is not set to NULL; otherwise, Value2 is returned. | IsNull([ShipDate], [RequiredDate]) |  - |
| IsNullOrEmpty(String) | Returns True if the specified String object is NULL or an empty string; otherwise, False is returned. | IsNullOrEmpty([ProductName]) |  Yes |

**Math Functions**

| Function | Description | Example | XLS(x) Format Export-Friendly [*See Note](#note---restrictions) |
|---|---|---|---|
| Abs(Value) | Returns the absolute, positive value of the given numeric expression. | Abs(1 - [Discount]) |  Yes |
| Acos(Value) | Returns the arccosine of a number (the angle, in radians, whose cosine is the given float expression). | Acos([Value]) |  Yes |
| Asin(Value) | Returns the arcsine of a number (the angle, in radians, whose sine is the given float expression). | Asin([Value]) |  Yes |
| Atn(Value) | Returns the arctangent of a number (the angle, in radians, whose tangent is the given float expression). | Atn([Value]) |  Yes |
| Atn2(Value1, Value2) | Returns the angle whose tangent is the quotient of two specified numbers, in radians. | Atn2([Value1], [Value2]) |  Yes |
| BigMul(Value1, Value2) | Returns an Int64 containing the full product of two specified 32-bit numbers. | BigMul([Amount], [Quantity]) |  - |
| Ceiling(Value) | Returns the smallest integer that is greater than or equal to the given numeric expression. | Ceiling([Value]) |  Yes |
| Cos(Value) | Returns the cosine of the angle defined in radians. | Cos([Value]) |  Yes |
| Cosh(Value) | Returns the hyperbolic cosine of the angle defined in radians. | Cosh([Value]) |  Yes |
| Exp(Value) | Returns the exponential value of the given float expression. | Exp([Value]) |  Yes |
| Floor(Value) | Returns the largest integer less than or equal to the given numeric expression. | Floor([Value]) |  Yes |
| Log(Value) | Returns the natural logarithm of a specified number. | Log([Value]) |  Yes |
| Log(Value, Base) | Returns the logarithm of a specified number in a specified Base. | Log([Value], 2) |  Yes |
| Log10(Value) | Returns the base 10 logarithm of a specified number. | Log10([Value]) |  Yes |
| Max(Value1, Value2) |	Returns the maximum value from the specified values. |	Max([Value1], [Value2])	| Yes
| Min(Value1, Value2) |	Returns the minimum value from the specified values. |	Min([Value1], [Value2]) | Yes
| Power(Value, Power) | Returns a specified number raised to a specified power. | Power([Value], 3) |  Yes |
| Rnd() | Returns a random number that is less than 1, but greater than or equal to zero. | Rnd()*100 |  Yes |
| Round(Value) | Rounds the given value to the nearest integer. | Round([Value]) |  Yes |
| Sign(Value) | Returns the positive (+1), zero (0), or negative (-1) sign of the given expression. | Sign([Value]) |  Yes |
| Sin(Value) | Returns the sine of the angle, defined in radians. | Sin([Value]) |  Yes |
| Sinh(Value) | Returns the hyperbolic sine of the angle defined in radians. | Sinh([Value]) |  Yes |
| Sqr(Value) | Returns the square root of a given number. | Sqr([Value]) |  - |
| Tan(Value) | Returns the tangent of the angle defined in radians. | Tan([Value]) |  Yes |
| Tanh(Value) | Returns the hyperbolic tangent of the angle defined in radians. | Tanh([Value]) |  Yes |
| ToDecimal(Value) | Converts Value to an equivalent decimal number. | ToDecimal([Value]) | - | 
| ToDouble(Value) | Converts Value to an equivalent 64-bit double-precision floating-point number. | ToDouble([Value]) | - | 
| ToFloat(Value) | Converts Value to an equivalent 32-bit single-precision floating-point number. | ToFloat([Value]) | - |  
| ToInt(Value) | Converts Value to an equivalent 32-bit signed integer. | ToInt([Value]) | - |  
| ToLong(Value) | Converts Value to an equivalent 64-bit signed integer. | ToLong([Value]) | - |  

**String Functions**

| Function | Description | Example |  XLS(x) Format Export-Friendly [*See Note](#note---restrictions) |
|---|---|---|---|
| Ascii(String) | Returns the ASCII code value of the leftmost character in a character expression. | Ascii('a') |  - |
| Char(Number) | Converts an integerASCIICode to a character. | Char(65) + Char(51) |  Yes |
| CharIndex(String1, String2) | Returns the starting position of String1 within String2, beginning from the zero character position to the end of a string. | CharIndex('e', 'devexpress') | - |
| CharIndex(String1, String2, StartLocation) | Returns the starting position of String1 within String2, beginning from the StartLocation character position to the end of a string. | CharIndex('e', 'devexpress', 2) | - |
| Concat(String1, ... , StringN) | Returns the result of concatenating two or more string values. | Concat('A', ')', [ProductName]) |  Yes |
|Contains(String1, SubString1) |	Returns True if SubString1 occurs within String1; otherwise, False is returned. |	Contains([ProductName], 'dairy') |	Yes
|EndsWith(String1, SubString1) |	Returns True if the end of String1 matches SubString1; otherwise, False is returned. |	EndsWith([Description], 'The end.') |	Yes
| Insert(String1, StartPosition, String2) | Inserts String2 into String1 at the position specified by StartPositon | Insert([Name], 0, 'ABC-') | - |
| Len(Value) | Returns an integer containing either the number of characters in a string or the nominal number of bytes required to store a variable. | Len([Description]) |  Yes |
| Lower(String) | Returns String in lowercase. | Lower([ProductName]) |  Yes |
| PadLeft(String, Length) | Left-aligns characters in the defined string, padding its left side with white space characters up to a specified total length. |  | - |
| PadLeft(String, Length, Char) | Left-aligns characters in the defined string, padding its left side with the specified Char up to a specified total length. | PadLeft([Name], 30, '&lt;') | - |
| PadRight(String, Length) | Right-aligns characters in the defined string, padding its left side with white space characters up to a specified total length. | PadRight([Name], 30) |  - |
| PadRight(String, Length, Char) | Right-aligns characters in the defined string, padding its left side with the specified Char up to a specified total length. | PadRight([Name], 30, '>') | - |
| Remove(String, StartPosition, Length) | Deletes a specified number of characters from this instance, beginning at a specified position. | Remove([Name], 0, 3) | - |
| Replace(String, SubString2, String3) | Returns a copy of String1, in which SubString2 has been replaced with String3. | Replace([Name], 'The ', '') | - |
| Reverse(String) | Reverses the order of elements within String. | Reverse([Name]) | - |
| StartsWith(String1, SubString1)	 | Returns True if the beginning of String1 matches SubString1; otherwise, False.	| StartsWith([Title], 'The best')	 | Yes
| Substring(String, StartPosition, Length) | Retrieves a substring from String. The substring starts at StartPosition and has the specified Length.. | Substring([Description], 2, 3) |  Yes |
| Substring(String, StartPosition) | Retrieves a substring from String. The substring starts at StartPosition. | Substring([Description], 2) |  - |
| ToStr(Value) | Returns a string representation of an object. | ToStr([ID]) | - |
| Trim(String) | Removes all leading and trailing SPACE characters from String. | Trim([ProductName]) |  Yes |
| Upper(String) | Returns String in uppercase. | Upper([ProductName]) |  Yes |

## Constants

| Constant | Description | Example | XLS(x) Format Export-Friendly [*See Note](#note---restrictions) |
|---|---|---|---|
| String constants | String constants must be wrapped in apostrophes. | [Country] == 'France' |  Yes |
| String constants (with apostrophe) | If a string contains an apostrophe, the apostrophe must be doubled. | [Name] == 'O''Neil' |  Yes |
| Date-time constants | Date-time constants must be wrapped in '#'. | [OrderDate] &gt;= #1/1/2009# |  Yes |
| True | Represents the Boolean True value. | [InStock] == True |  Yes |
| False | Represents the Boolean False value. | [InStock] == False |  Yes |
| ? | Represents a null reference that does not refer to any object. We recommend using the IsNull unary operator (for example, "[Region] is null") or the IsNull logical function (for example, "IsNull([Region])") instead. | [Region] != ? |  Yes |
| Enumeration | Specify an enumeration value using its underlying integer value. | [Status] == 1
| Guid|  Wrap a Guid constant in curly braces. Use Guid constants in a relational operation with equality or inequality operators only. | [OrderID] == {513724e5-17b7-4ec6-abc4-0eae12c72c1f} | Yes |
| Numeric |     Specify different numeric constant types in a string form using suffixes: <br> * Int32 (int)  - _1_ </br> * Int16 (short) - _1s_ </br> * Byte (byte) - _1b_  </br>  * Double (double) - _1.0_ </br> * Single (float) - _1.0f_ </br>  * Decimal (decimal) - _1.0m_ </br>    |  [Price] == 25.0m |  Yes |     

You can build parameterized criteria using any number of positional parameters. To do this, add parameter placeholders (question mark characters) to a criteria expression to identify parameter positions and provide a list of parameter values. When building criteria, parameter placeholders are substituted with parameter values in values in the order they are listed.

_CriteriaOperator.Parse("[Name] == ? and [Age] == ?", "John", 33)_

The following two examples are identical, but the second one allows you to avoid formatting errors.

_CriteriaOperator.Parse("[OrderDate] >= #1/1/2009#")_

_CriteriaOperator.Parse("[OrderDate] >= ?", new DateTime(2009, 1, 1))_

When parameters are not specified, a parameter placeholder is substituted with null.

_CriteriaOperator.Parse("[Region] != ?")_

## Collection Elements Verification

Use brackets "[]" to check if a collection contains an element that satisfies a condition. The following expression returns true if the Accounts collection contains at least one element that satisfies the _[Amount] == 100_ condition:

_[Accounts][[Amount] == 100]_

The following expression returns false if the Accounts collection is empty:

_[Accounts][]_

## Parent Relating Operator

Use the parent relating operator ('^' character) to refer to a parent in expressions written in the context of a child. You can apply this operator successively to navigate multiple parent relationships. In the expression below, the "RegistrationDate" field refers to a Customer (Orders' parent) and the "Date" field refers to Orders. This expression returns true if there is at least one Order that is made on the day the parent Customer is registered:

_"[Orders][[^.RegistrationDate] == Date]"_

## Grouping Clauses with Brackets

It is important to use brackets to ensure that your expression returns the intended results.
For instance, the following expression for objects of the Customer type returns all of the Customers where an Account exists with a Date of 8/25/2006 and where an account exists with an Amount of 100:

_[Accounts][[Date] == #8/25/2006#] && [Accounts][[Amount] == 100]_

Construct the expression as in the following example to search for all Customers that have an Account with both a Date of 8/25/2006 and an Amount of 100:

_[Accounts][[Date] == #8/25/2006# && [Amount] == 100]_

## Operator Precedence

When an expression contains multiple operators, their precedence controls the order in which expression elements are evaluated.

* Literal values
* Parameters
*  Identifiers
* OR (left-associative)
* AND (left-associative)
* '.' relationship qualifier (left-associative)
* ==, !=
* <, >, <=, >=
* -, + (left-associative)
* *, /, % (left-associative)
* NOT
* unary -
* In
* Iif
* Trim(), Len(), Substring(), IsNull()
* '[]' (for set-restriction)
* '()'

The default precedence can be changed by grouping elements with parentheses. For instance, the operators are performed in a default order in the first of the following two code samples. In the second code sample, the addition operation is performed first, because its associated elements are grouped with parentheses, and the multiplication operation is performed last.

_Accounts[Amount == 2 + 48 * 2]_

_Accounts[Amount == (2 + 48) * 2]_

## Case Sensitivity

Operators are case insensitive. Although field values’ case sensitivity depends on the data source.

> [!NOTE]
> A data source affects certain operators' behavior. For instance, by default, the SQL Server Express 2005 is configured as case insensitive. In this case, the following expression always evaluates to **true**:
> 
> _Lower(Name) == Upper(Name)_

## Escaping Keywords
You can mark a keyword&#0045;like field name with an escape character (@ sign). In the expression below, the **CriteriaOperator.Parse** method interprets \@Or as the field named "Or", not the logical operator OR.

_\@Or = 'value'_

## Escape Characters
Use a backslash (&#92;) as an escape character for characters in expressions. Examples:

* \\[
* \\\
* \\'

## Retrieving Reference Properties

Note that while a criteria expression can return an object reference, this is not supported in all scenarios. Returning an object reference by directly referencing a property, as in the following code snippet, is fully supported.

_"Iif(Part is null, MyCustOrderLine.Part, Part)"_

In this code snippet, the Part object, which the Part or MyCustOrderLine.Part property references, is returned correctly. However, retrieving reference properties from functions is not supported. So, the following expression does not work.

_"Iif(Part is null, MyCustOrderLine, MyCustOrderLine2).Part"_

## Note - Restrictions

Note the following restriction when exporting DevExpress Data Grid and Tree List controls (WinForms and WPF) to the XLS(X) format in **Data-Aware Export Mode**:

Only expressions that contain export-friendly functions are exported to XLS(X) format. Refer to the **XLS(x) Format Export-Friendly** column in the tables above to find out if a function can be exported to XLS(x) format.

For more information about data exporting, see [exporting](../pivot-table/exporting-and-printing/exporting-and-printing.md)
