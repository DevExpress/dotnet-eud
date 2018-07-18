---
title: Expression Syntax
owner: Mary Sammal
---

# Expression Syntax

The table below contains constants, operators, and functions you can use in [expressions](xref:120091).

## Constants
{|
|-

! Constant
! Description
! Example
|-

| String constants
| Wrap string constants in apostrophes.

If a string contains an apostrophe, double the apostrophe.
| [Country] == 'France'

[Name] == 'O''Neil'

|-

| Date-time constants
| Wrap date-time constants in '#'.
| [OrderDate] &gt;= #2018-03-22 13:18:51.94944#
 
|-

| True
| Represents the Boolean True value.
| [InStock] == True
 
|-

| False
| Represents the Boolean False value.
| [InStock] == False
 
|-

| Enumeration
| Specify an enumeration value using its underlying integer value.
| [Status] == 1

Note that you cannot specify an enumeration value using its qualified name. The following criteria **is incorrect**:

[Status] = Status.InProgress
 
|-

| Guid
| Wrap a Guid constant in curly braces. Use Guid constants in a relational operation with equality or inequality operators only.
| [OrderID] == {513724e5-17b7-4ec6-abc4-0eae12c72c1f}
 
|-

| Numeric
| Specify different numeric constant types in a string form using suffixes:

* Int32 (int) - _1_
* Int16 (short) - _1s_
* Byte (byte) - _1b_
* Double (double) - _1.0_
* Single (float) - _1.0f_
* Decimal (decimal) - _1.0m_
| [Price] == 25.0m
 
|-

| ?
| Represents a null reference that does not refer to any object.

We recommend using the **IsNull** unary operator (for example, "[Region] is null") or the **IsNull** logical function (for example, "IsNull([Region])") instead.
| [Region] != ?
 
|}

You can build parameterized criteria using any number of positional parameters. To do this, add parameter placeholders (question mark characters) to a criteria expression to identify parameter positions and provide a list of parameter values. When building criteria, parameter placeholders are substituted with parameter values in values in the order they are listed.

_CriteriaOperator.Parse("[Name] == ? and [Age] == ?", "John", 33)_

The following two examples are identical, but the second one allows you to avoid formatting errors.

_CriteriaOperator.Parse("[OrderDate] >= #1/1/2009#")_

_CriteriaOperator.Parse("[OrderDate] >= ?", new DateTime(2009, 1, 1))_

When parameters are not specified, a parameter placeholder is substituted with null.

_CriteriaOperator.Parse("[Region] != ?")_

## Operators
{|
|-

! Operator
! Description
! Example
|-

| +
| Adds the value of one numeric expression to another or concatenates two strings.
| [UnitPrice] + 4

[FirstName] + ' ' + [LastName]
 
|-

| -
| Finds the difference between two numbers.
| [Price1] - [Price2]
 
|-

| *
| Multiplies the value of two expressions.
| [Quantity] * [UnitPrice] * (1 - [BonusAmount])
 
|-

| /
| Divides the first operand by the second.
| [Quantity] / 2
 
|-

| %
| Returns the remainder (modulus) obtained by dividing one numeric expression by another.
| [Quantity] % 3
 
|-

| |
| The bitwise OR operator. Compares each bit of its first operand to the corresponding bit of its second operand. If either bit is 1, the corresponding resulting bit is set to 1. Otherwise, the corresponding resulting bit is set to 0.
| [Flag1] | [Flag2]
 
|-

| &amp;
| The bitwise AND operator. Compares each bit of its first operand to the corresponding bit of its second operand. If both bits are 1, the corresponding resulting bit is set to 1. Otherwise, the corresponding resulting bit is set to 0.
| [Flag] &amp; 10
 
|-

| ^
| Performs a logical exclusive OR on two Boolean expressions, or a bitwise exclusive OR on two numeric expressions.
| [Flag1] ^ [Flag2]
 
|-

| ==

=
| Returns true if both operands have the same value; otherwise, it returns false.
| [Quantity] == 10
 
|-

| !=
| Returns true if the operands do not have the same value; otherwise, it returns false.
| [Country] != 'France'
 
|-

| &lt;
| Less than operator. Used to compare expressions.
| [UnitPrice] &lt; 20
 
|-

| &lt;=
| Less than or equal to operator. Used to compare expressions.
| [UnitPrice] &lt;= 20
 
|-

| &gt;=
| Greater than or equal to operator. Used to compare expressions.
| [UnitPrice] &gt;= 30
 
|-

| &gt;
| Greater than operator. Used to compare expressions.
| [UnitPrice] &gt; 30
 
|-

| In (,,,)
| Tests for the existence of a property in an object.
| [Country] In ('USA', 'UK', 'Italy')
|-

| Between (,)
| Specifies a range to test. Returns true if a value is greater than or equal to the first operand and less than or equal to the second operand.
| [Quantity] Between (10, 20)
 
|-

| And

&amp;&amp;
| Performs a logical conjunction on two expressions.
| [InStock] And ([ExtendedPrice]> 100)

[InStock] &amp;&amp; ([ExtendedPrice]> 100)
 
|-

| Or

||
| Performs a logical disjunction on two Boolean expressions.
| [Country]=='USA' Or [Country]=='UK'

[Country]=='USA' \|| [Country]=='UK'
 
|-

| !
| Performs logical negation on an expression.
| ![InStock]
 
|}

**Unary Operators**

Unary operators perform operations on a single expression.

| Name | Description | Usage |
|---|---|---|---|
| **BitwiseNot** | Represents the bitwise NOT operator. | "~[Roles] = 251" |
| **Not** | Represents the logical NOT. | "Not [InStock]"   |
| **Minus** | Represents the unary negation (-) operator. | "[Value] = -20"   |
| **Plus** | Represents the unary plus (+) operator. | "[Value] = +10"   |
| **IsNull** | Represents a null reference, one that does not refer to any object. | "[Region] is null"   |


## Functions (Basic)
**Aggregate Functions**

| Function | Description | Example |
|---|---|---|---|
| Avg(Value) | Evaluates the average of the values in the collection. | [Products].Avg([UnitPrice]) |
| Count() | Returns the number of objects in a collection. | [Products].Count() |
| Exists() | Determines whether the object exists in the collection. | [Categories][[CategoryID] == 7].Exists() |
| Max(Value) | Returns the maximum expression value in a collection. | [Products].Max([UnitPrice]) |
| Min(Value) | Returns the minimum expression value in a collection. | [Products].Min([UnitPrice]) |
| Single() | Returns a single object from the collection. | [Accounts].Single() is not null |
| Sum(Value) | Returns the sum of all the expression values in the collection. | [Products].Sum([UnitsInStock]) |

**Date-time Functions**

| Function | Description | Example |
|---|---|---|---|
| AddDays(DateTime, DaysCount) | Returns a date-time value that is the specified number of days from the specified DateTime. | AddDays([OrderDate], 30)   |
| AddHours(DateTime, HoursCount) | Returns a date-time value that is the specified number of hours from the specified DateTime. | AddHours([StartTime], 2)   |
| AddMilliSeconds(DateTime, MilliSecondsCount) | Returns a date-time value that is the specified number of milliseconds from the specified DateTime. | AddMilliSeconds(([StartTime], 5000)) |
| AddMinutes(DateTime, MinutesCount) | Returns a date-time value that is the specified number of minutes from the specified DateTime. | AddMinutes([StartTime], 30)   |
| AddMonths(DateTime, MonthsCount) | Returns a date-time value that is the specified number of months from the specified DateTime. | AddMonths([OrderDate], 1)   |
| AddSeconds(DateTime, SecondsCount) | Returns a date-time value that is the specified number of seconds from the specified DateTime. | AddSeconds([StartTime], 60)   |
| AddTicks(DateTime, TicksCount) | Returns a date-time value that is the specified number of ticks from the specified DateTime. | AddTicks([StartTime], 5000) |
| AddTimeSpan(DateTime, TimeSpan) | Returns a date-time value that is from the specified DateTime for the given TimeSpan. | AddTimeSpan([StartTime], [Duration]) |
| AddYears(DateTime, YearsCount) | Returns a date-time value that is the specified number of years from the specified DateTime. | AddYears([EndDate], -1)   |
| DateDiffDay(startDate, endDate) | Returns the number of day boundaries between two non-nullable dates. | DateDiffDay([StartTime], Now())   |
| DateDiffHour(startDate, endDate) | Returns the number of hour boundaries between two non-nullable dates. | DateDiffHour([StartTime], Now())   |
| DateDiffMilliSecond(startDate, endDate) | Returns the number of millisecond boundaries between two non-nullable dates. | DateDiffMilliSecond([StartTime], Now()) |
| DateDiffMinute(startDate, endDate) | Returns the number of minute boundaries between two non-nullable dates. | DateDiffMinute([StartTime], Now())   |
| DateDiffMonth(startDate, endDate) | Returns the number of month boundaries between two non-nullable dates. | DateDiffMonth([StartTime], Now())   |
| DateDiffSecond(startDate, endDate) | Returns the number of second boundaries between two non-nullable dates. | DateDiffSecond([StartTime], Now())   |
| DateDiffTick(startDate, endDate) | Returns the number of tick boundaries between two non-nullable dates. | DateDiffTick([StartTime], Now()) |
| DateDiffYear(startDate, endDate) | Returns the number of year boundaries between two non-nullable dates. | DateDiffYear([StartTime], Now())   |
| GetDate(DateTime) | Extracts a date from the defined DateTime. | GetDate([OrderDateTime])   |
| GetDay(DateTime) | Extracts a day from the defined DateTime. | GetDay([OrderDate])   |
| GetDayOfWeek(DateTime) | Extracts a day of the week from the defined DateTime. | GetDayOfWeek([OrderDate])   |
| GetDayOfYear(DateTime) | Extracts a day of the year from the defined DateTime. | GetDayOfYear([OrderDate])   |
| GetHour(DateTime) | Extracts an hour from the defined DateTime. | GetHour([StartTime])   |
| GetMilliSecond(DateTime) | Extracts milliseconds from the defined DateTime. | GetMilliSecond([StartTime]) |
| GetMinute(DateTime) | Extracts minutes from the defined DateTime. | GetMinute([StartTime])   |
| GetMonth(DateTime) | Extracts a month from the defined DateTime. | GetMonth([StartTime])   |
| GetSecond(DateTime) | Extracts seconds from the defined DateTime. | GetSecond([StartTime])   |
| GetTimeOfDay(DateTime) | Extracts the time of the day from the defined DateTime in ticks. | GetTimeOfDay([StartTime]) |
| GetYear(DateTime) | Extracts a year from the defined DateTime. | GetYear([StartTime])   |
| IsApril(DateTime) | Returns True if the specified date falls within April. | IsApril([OrderDate])   |
| IsAugust(DateTime) | Returns True if the specified date falls within August. | IsAugust([OrderDate])   |
| IsDecember(DateTime) | Returns True if the specified date falls within December. | IsDecember([OrderDate])   |
| IsFebruary(DateTime) | Returns True if the specified date falls within February. | IsFebruary([OrderDate])   |
| IsJanuary(DateTime) | Returns True if the specified date falls within January. | IsJanuary([OrderDate])   |
| IsJuly(DateTime) | Returns True if the specified date falls within July. | IsJuly([OrderDate])   |
| IsJune(DateTime) | Returns True if the specified date falls within June. | IsJune([OrderDate])   |
| IsLastMonth(DateTime) | Returns True if the specified date falls within the previous month. | IsLastMonth([OrderDate])   |
| IsLastYear(DateTime) | Returns True if the specified date falls within the previous year. | IsLastYear([OrderDate])   |
| IsMarch(DateTime) | Returns True if the specified date falls within March. | IsMarch([OrderDate])   |
| IsMay(DateTime) | Returns True if the specified date falls within May. | IsMay([OrderDate])   |
| IsNextMonth(DateTime) | Returns True if the specified date falls within the next month. | IsNextMonth([OrderDate])   |
| IsNextYear(DateTime) | Returns True if the specified date falls within the next year. | IsNextYear([OrderDate])   |
| IsNovember(DateTime) | Returns True if the specified date falls within November. | IsNovember([OrderDate])   |
| IsOctober(DateTime) | Returns True if the specified date falls within October. | IsOctober([OrderDate])   |
| IsSameDay(DateTime) | Returns True if the specified date/time values fall within the same day. | IsSameDay([OrderDate])   |
| IsSeptember(DateTime) | Returns True if the specified date falls within September. | IsSeptember([OrderDate])   |
| IsThisMonth(DateTime) | Returns True if the specified date falls within the current month. | IsThisMonth([OrderDate])   |
| IsThisWeek(DateTime) | Returns True if the specified date falls within the current week. | IsThisWeek([OrderDate])   |
| IsYearToDate(DateTime) | Returns True if the specified date falls within the year-to-date period. This period starts from the first day of the current year and continues to the current date (including the current date). | IsYearToDate([OrderDate])   |
| IsThisYear(DateTime) | Returns True if the specified date falls within the current year. | IsThisYear([OrderDate])   |
| LocalDateTimeDayAfterTomorrow() | Returns a date-time value corresponding to the day after Tomorrow. | AddDays(LocalDateTimeDayAfterTomorrow(), 5)   |
| LocalDateTimeLastMonth() | Returns the DateTime value corresponding to the first day of the previous month. | AddMonths(LocalDateTimeLastMonth(), 5)   |
| LocalDateTimeLastWeek() | Returns a date-time value corresponding to the first day of the previous week. | AddDays(LocalDateTimeLastWeek(), 5)   |
| LocalDateTimeLastYear() | Returns the DateTime value corresponding to the first day of the previous year. | AddYears(LocalDateTimeLastYear(), 5)   |
| LocalDateTimeNextMonth() | Returns a date-time value corresponding to the first day of the next month. | AddMonths(LocalDateTimeNextMonth(), 5)   |
| LocalDateTimeNextWeek() | Returns a date-time value corresponding to the first day of the following week. | AddDays(LocalDateTimeNextWeek(), 5)   |
| LocalDateTimeNextYear() | Returns a date-time value corresponding to the first day of the following year. | AddYears(LocalDateTimeNextYear(), 5)   |
| LocalDateTimeNow() | Returns a date-time value corresponding to the current moment in time. | AddDays(LocalDateTimeNow(), 5)   |
| LocalDateTimeThisMonth() | Returns a date-time value corresponding to the first day of the current month. | AddMonths(LocalDateTimeThisMonth(), 5)   |
| LocalDateTimeThisWeek() | Returns a date-time value corresponding to the first day of the current week. | AddDays(LocalDateTimeThisWeek(), 5)   |
| LocalDateTimeThisYear() | Returns a date-time value corresponding to the first day of the current year. | AddYears(LocalDateTimeThisYear(), 5)   |
| LocalDateTimeToday() | Returns a date-time value corresponding to Today. | AddDays(LocalDateTimeToday(), 5)   |
| LocalDateTimeTomorrow() | Returns a date-time value corresponding to Tomorrow. | AddDays(LocalDateTimeTomorrow(), 5)   |
| LocalDateTimeTwoMonthsAway() | Returns the DateTime value corresponding to the first day of the following month. | AddMonths(LocalDateTimeTwoMonthAway(), 5)   |
| LocalDateTimeTwoWeeksAway() | Returns the DateTime value corresponding to the first day of the following week. | AddDays(LocalDateTimeTwoWeeksAway(), 5)   |
| LocalDateTimeTwoYearsAway() | Returns the DateTime value corresponding to the first day of the following year. | AddYears(LocalDateTimeTwoYearsAway(), 5)   |
| LocalDateTimeYearBeforeToday() | Returns the DateTime value corresponding to the day one year ago. | AddYears(LocalDateTimeYearBeforeToday(), 5)   |
| LocalDateTimeYesterday() | Returns a date-time value corresponding to Yesterday. | AddDays(LocalDateTimeYesterday(), 5)   |
| Now() | Returns the current system date and time. | AddDays(Now(), 5)   |
| Today() | Returns the current date. Regardless of the actual time, this function returns midnight of the current date. | AddMonths(Today(), 1)   |
| UtcNow() | Returns the current system date and time, expressed as Coordinated Universal Time (UTC). | AddDays(UtcNow(), 7) |

**Logical Functions**

{|
|-

! Function
! Description
! Example
|-

| Iif(Expression, TruePart, FalsePart)
| Returns one of several specified values depending upon the values of logical expressions.

The function can take _n_ operands of the **CriteriaOperator** class:

1 - determines the first logical expression;

2 &#0045; specifies the value that is returned if the first logical expression evaluates to **true**;

**...**

n&#0045;2 &#0045; determines the _n-2_ logical expression;

n&#0045;1 &#0045; specifies the value that is returned if the _n-2_ logical expression evaluates to **true**;

n &#0045; specifies the value that is returned if the previously evaluated logical expressions yielded **false**.
| Iif(Name = 'Bob', 1, Name = 'Dan', 2, Name = 'Sam', 3, 4)")
 
|-

| IsNull(Value)
| Returns True if the specified Value is NULL.
| IsNull([OrderDate])
 
|-

| IsNull(Value1, Value2)
| Returns Value1 if it is not set to NULL; otherwise, Value2 is returned.
| IsNull([ShipDate], [RequiredDate])
|-

| IsNullOrEmpty(String)
| Returns True if the specified String object is NULL or an empty string; otherwise, False is returned.
| IsNullOrEmpty([ProductName])
 
|}

**Math Functions**

| Function | Description | Example |
|---|---|---|---|
| Abs(Value) | Returns the given numeric expression's absolute, positive value. | Abs(1 - [Discount])   |
| Acos(Value) | Returns a number's arccosine (the angle in radians, whose cosine is the given float expression). | Acos([Value])   |
| Asin(Value) | Returns a number's arcsine (the angle in radians, whose sine is the given float expression). | Asin([Value])   |
| Atn(Value) | Returns a number's arctangent (the angle in radians, whose tangent is the given float expression). | Atn([Value])   |
| Atn2(Value1, Value2) | Returns the angle whose tangent is the quotient of two specified numbers in radians. | Atn2([Value1], [Value2])   |
| BigMul(Value1, Value2) | Returns an Int64 containing the full product of two specified 32-bit numbers. | BigMul([Amount], [Quantity]) |
| Ceiling(Value) | Returns the smallest integer that is greater than or equal to the numeric expression. | Ceiling([Value])   |
| Cos(Value) | Returns the angle's cosine, in radians. | Cos([Value])   |
| Cosh(Value) | Returns the angle's hyperbolic cosine, in radians. | Cosh([Value])   |
| Exp(Value) | Returns the float expression's exponential value. | Exp([Value])   |
| Floor(Value) | Returns the largest integer less than or equal to the numeric expression. | Floor([Value])   |
| Log(Value) | Returns a specified number's natural logarithm. | Log([Value])   |
| Log(Value, Base) | Returns the logarithm of a specified number in a specified Base. | Log([Value], 2)   |
| Log10(Value) | Returns a specified number's base 10 logarithm. | Log10([Value])   |
| Max(Value1, Value2) | Returns the maximum value from the specified values. | Max([Value1], [Value2])   |
| Min(Value1, Value2) | Returns the minimum value from the specified values. | Min([Value1], [Value2])   |
| Power(Value, Power) | Returns a specified number raised to a specified power. | Power([Value], 3)   |
| Rnd() | Returns a random number that is less than 1, but greater than or equal to zero. | Rnd()*100   |
| Round(Value) | Rounds the given value to the nearest integer. | Round([Value])   |
| Round(Value, Precision) | Rounds the given value to the nearest integer, or to a specified number of decimal places. | Round([Value], 2)   |
| Sign(Value) | Returns the positive (+1), zero (0), or negative (-1) sign of the given expression. | Sign([Value])   |
| Sin(Value) | Returns the sine of the angle defined in radians. | Sin([Value])   |
| Sinh(Value) | Returns the hyperbolic sine of the angle defined in radians. | Sinh([Value])   |
| Sqr(Value) | Returns the square root of a given number. | Sqr([Value]) |
| Tan(Value) | Returns the tangent of the angle defined in radians. | Tan([Value])   |
| Tanh(Value) | Returns the hyperbolic tangent of the angle defined in radians. | Tanh([Value])   |
| ToDecimal(Value) | Converts Value to an equivalent decimal number. | ToDecimal([Value]) |
| ToDouble(Value) | Converts Value to an equivalent 64-bit double-precision floating-point number. | ToDouble([Value]) |
| ToFloat(Value) | Converts Value to an equivalent 32-bit single-precision floating-point number. | ToFloat([Value]) |
| ToInt(Value) | Converts Value to an equivalent 32-bit signed integer. | ToInt([Value]) |
| ToLong(Value) | Converts Value to an equivalent 64-bit signed integer. | ToLong([Value]) |

**String Functions**

| Function | Description | Example |
|---|---|---|---|
| Ascii(String) | Returns the ASCII code value of the leftmost character in a character expression. | Ascii('a') |
| Char(Number) | Converts an integerASCIICode to a character. | Char(65) + Char(51)   |
| CharIndex(String1, String2) | Returns the starting position of String1 within String2, beginning from the zero character position to the end of a string. | CharIndex('e', 'devexpress') |
| CharIndex(String1, String2, StartLocation) | Returns the starting position of String1 within String2, beginning from the StartLocation character position to the end of a string. | CharIndex('e', 'devexpress', 2) |
| Concat(String1, ... , StringN) | Returns a string value containing the concatenation of the current string with any additional strings. | Concat('A', ')', [ProductName])   |
| Contains(String1, SubString1) | Returns True if SubString1 occurs within String1; otherwise, False is returned. | Contains([ProductName], 'dairy')   |
| EndsWith(String1, SubString1) | Returns True if the end of String1 matches SubString1; otherwise, False is returned. | EndsWith([Description], 'The end.')   |
| Insert(String1, StartPosition, String2) | Inserts String2 into String1 at the position specified by StartPositon | Insert([Name], 0, 'ABC-') |
| Len(Value) | Returns an integer containing either the number of characters in a string or the nominal number of bytes required to store a variable. | Len([Description])   |
| Lower(String) | Returns String in lowercase. | Lower([ProductName])   |
| PadLeft(String, Length) | Left-aligns the defined string's characters, padding its left side with white space characters up to a specified total length. | PadLeft([Name], 30) |
| PadLeft(String, Length, Char) | Left-aligns the defined string's characters, padding its left side with the specified Char up to a specified total length. | PadLeft([Name], 30, '&lt;') |
| PadRight(String, Length) | Right-aligns the defined string’s characters, padding its left side with empty space characters up to a specified total length. | PadRight([Name], 30) |
| PadRight(String, Length, Char) | Right-aligns the defined string’s characters, padding its left side with the specified Char up to a specified total length. | PadRight([Name], 30, '>') |
| Remove(String, StartPosition) | Deletes all the characters from this instance, beginning at a specified position. | Remove([Name], 3) |
| Remove(String, StartPosition, Length) | Deletes a specified number of characters from this instance, beginning at a specified position. | Remove([Name], 0, 3) |
| Replace(String, SubString2, String3) | Returns a copy of String1, in which SubString2 has been replaced with String3. | Replace([Name], 'The ', '') |
| Reverse(String) | Reverses the order of elements within String. | Reverse([Name]) |
| StartsWith(String1, SubString1) | Returns True if the beginning of String1 matches SubString1; otherwise, False. | StartsWith([Title], 'The best')   |
| Substring(String, StartPosition, Length) | Retrieves a substring from String. The substring starts at StartPosition and has a specified Length. | Substring([Description], 2, 3) |
| Substring(String, StartPosition) | Retrieves a substring from String. The substring starts at StartPosition. | Substring([Description], 2) |
| ToStr(Value) | Returns a string representation of an object. | ToStr([ID]) |
| Trim(String) | Removes all leading and trailing SPACE characters from String. | Trim([ProductName])   |
| Upper(String) | Returns String in uppercase. | Upper([ProductName])   |

## Functions for Expression Bindings and Calculated Fields

Below is a list of functions that are used to construct [expression bindings](xref:119236) and [calculated fields](xref:4801):

{|
|-

! Function
! Description
! Example
|-

| NewLine()
| Returns the newline string defined for the current environment.
| [CategoryName]+NewLine()+[Description]

Result:

_Beverages_

_Soft drinks, coffees, teas, beers and ales._
|-

| FormatString(Format, Value1, ... , ValueN)
| Returns the specified string with formatted field values. See [Formatting Data](xref:5327) for details.
| FormatString('{0:$0.00}', [UnitPrice])

Result: _$45.60_
|-

| Rgb(Red, Green, Blue)
| Returns a string defining a color using the Red, Green, and Blue color channel values.
| Rgb(30,200,150)

Result: _'30,200,150'_
|-

| Argb(Alpha, Red, Green, Blue)
| Returns a string defining a color using the Alpha, Red, Green, and Blue color channel values.
| Argb(1,200, 30, 200)

Result: _'1,200,30,200'_
|-

| Join()
| Concatenates the [multi-value report parameter](xref:9998)'s values into a string. This function is useful when you [bind a multi-value parameter to a label](xref:9997) to display the parameter's values in a report.

This function has two overloads:

* Join(parameter) - concatenates the specified parameter's values using comma as a separator.
* Join(parameter, separator) - concatenates the specified parameter's values using the specified separator.
| Join([Parameters.CategoriesParameter])

Result: _Beverages, Condiments_

Join([Parameters.CategoriesParameter], newline())

Result: 

_Beverages_

_Condiments_
|}

## Functions for Stored Procedure Binding

The following functions are specific for [binding reports to a stored procedure](xref:10555):

{|
|-

! Function
! Description
! Example
|-

| Join()
| Concatenates the [multi-value report parameter](xref:9998)'s values into a string. This function can be used when mapping multi-value report parameters to query parameters generated from a stored procedure's parameters. Refer to the [Query Parameters](xref:17387) topic for more information.

This function has two overloads:

* Join(parameter) - concatenates the specified parameter's values using comma as a separator.
* Join(parameter, separator) - concatenates the specified parameter's values using the specified separator.
| Join([Parameters.Parameter1])
|-

| CreateTable(Column1, ..., ColumnN)
| Creates a table from several multi-value parameters' values. This function can be used when mapping multi-value report parameters to the query parameter that is generated from a stored procedure's [User Defined Table Type](https://docs.microsoft.com/en-us/sql/relational-databases/tables/use-table-valued-parameters-database-engine) parameter. Refer to the [Query Parameters](xref:17387) topic for more information.
| CreateTable([Parameters.Parameter1], ..., [Parameters.ParameterN])
|}

## <a name="summary-expression-editor">Functions for Summary Expression Editor</a>

Use the following functions when [calculating summaries](xref:119436) across a report and its groups:

{|
|-

! Function
! Description
! Example
|-

| sumAvg(Expression)
| Calculates the average of all the values within the specified summary region (group, page or report).
| sumAvg([UnitPrice])
|-

| sumCount(Expression)
| Counts the number of values within the specified summary region (group, page or report). In a simple scenario, you may not pass a parameter.

  When using this function in a [master-detail report](xref:4785)'s master band and passing a detail's field as a parameter, it counts the number of records within the detail's band.

  See also: <xref:119445>, <xref:119476>
| sumCount([UnitPrice])
|-

| sumDAvg(Expression)
| Calculates the average of all the **distinct** values within the specified summary region (group, page or report).
| sumDAvg([UnitPrice])
|-

| sumDCount(Expression)
| Counts the number of **distinct** values within the specified summary region (group, page or report). In a simple scenario, you may not pass a parameter.
| sumDCount([UnitPrice])
|-

| sumDStdDev(Expression)
| Calculates the standard deviation of all the **distinct** values within the specified summary region (group, page or report).
| sumDStdDev([UnitPrice])
|-

| sumDStdDevP(Expression)
| Calculates the standard population deviation of all the **distinct** values within the specified summary region (group, page or report).
| sumDStdDevP([UnitPrice])
|-

| sumDSum(Expression)
| Calculates the total of all the **distinct** values within the specified summary region (group, page or report).
| sumDSum([UnitPrice])
|-

| sumDVar(Expression)
| Calculates the amount of variance for all the **distinct** values within the specified summary region (group, page or report).
| sumDVar([UnitPrice])
|-

| sumDVarP(Expression)
| Calculates the population variance of all the **distinct** values within the specified summary region (group, page or report).
| sumDVarP([UnitPrice])
|-

| sumMax(Expression)
| Calculates the maximum of all the values within the specified summary region (group, page or report).
| sumMax([UnitPrice])
|-

| sumMedian(Expression)
| Finds the middle number within a sequence.



  Note that if the total number of elements is odd, this function returns the value of the middle number in a sequence. If the total number of elements is even, this function returns the arithmetical mean of the two middle numbers.
| sumMedian([UnitPrice])
|-

| sumMin(Expression)
| Calculates the minimum of all the values within the specified summary region (group, page or report).
| sumMin([UnitPrice])
|-

| sumPercentage(Expression)
| Calculates the percent ratio of the current data row's value to the total of all the values within the specified summary region (group, page or report).
| sumPercentage([UnitPrice])
|-

| sumRecordNumber(Expression)
| Returns the current record number in the specified summary region (group, page or report). This means for instance, if the summary is calculated for a group, then the record number is calculated only within that group, and is reset every time a new group is started.

  In a simple scenario, you may not pass a parameter.

  See also: <xref:119444>
| sumRecordNumber()
|-

| sumRunningSum(Expression)
| Summarizes all the values, which were printed before the current data row, with the current data row's value.
| sumRunningSum([UnitPrice])
|-

| sumStdDev(Expression)
| Calculates the standard deviation of all the values within the specified summary region (group, page or report).
| sumStdDev([UnitPrice])
|-

| sumStdDevP(Expression)
| Calculates the standard population deviation of all the values within the specified summary region (group, page or report).
| sumStdDevP([UnitPrice])
|-

| sumSum(Expression)
| Calculates the total of all the values within the specified summary region (group, page or report).
| sumSum([UnitsInStock])
|-

| sumVar(Expression)
| Calculates the amount of variance for all the values within the specified summary region (group, page or report).
| sumVar([UnitPrice])
|-

| sumVarP(Expression)
| Calculates the population variance of all the values within the specified summary region (group, page or report).
| sumVarP([UnitPrice])
|-
|}

## Variables for Event-Related Expressions

You can specify expressions for the [XRControl.BeforePrint](xref:DevExpress.XtraReports.UI.XRControl.BeforePrint) and [XRControl.PrintOnPage](xref:DevExpress.XtraReports.UI.XRControl.PrintOnPage) events when the <xref:DevExpress.XtraReports.Configuration.UserDesignerOptions.DataBindingMode> property is set to *[DataBindingMode.ExpressionsAdvanced](xref:DevExpress.XtraReports.UI.DataBindingMode)*.

Use the following variables when constructing expressions the [XRControl.BeforePrint](xref:DevExpress.XtraReports.UI.XRControl.BeforePrint) event resolves:

{|
|-

! Variable
! Description
! Example
|-

| DataSource.RowCount
| Returns the total amount of data rows in a data source.
| [DataSource.RowCount] != 0

Result: When using this expression for a control's Visible property, the control is not displayed if there is no data in the data source.
|-

| DataSource.CurrentRowIndex
| Returns a zero-based index of the current data row in a data source.
| Iif([DataSource.CurrentRowIndex] % 2 = 0, 'red', 'green')

Result: When this expression is used for a table row's BackColor property, odd rows are colored in red and even rows - in green.
|}


Use the following variables when constructing expressions the [XRControl.PrintOnPage](xref:DevExpress.XtraReports.UI.XRControl.PrintOnPage) event resolves:

{|
|-

! Variable
! Description
! Example
|-

| Arguments.PageIndex
| Returns a zero-based index of the currently generated report document page.
| [Arguments.PageIndex] % 2 = 0


Result: The control is displayed on odd pages only when this expression is used for a control's Visible property.
|-

| Arguments.PageCount
| Returns the page count in the report document.

> [!Note]
> The **PageCount** property value is not valid if you use the <xref:DevExpress.XtraPrinting.Caching.CachedReportSource> component to generate a report document
| Iif(([Arguments.PageIndex] = [Arguments.PageCount] - 1), 'The last page!', '')


  Result: When using this expression for a label's Text property, the 'The last page!' string is displayed on the last page.

|}

> [!Note]
> The **Arguments.PageIndex** and **Arguments.PageCount** variables are not valid in the following scenarios:
>* when the report is [merged](xref:3320) with another report;
>* when the report includes a [table or contents](xref:115661).


## Report Parameters

Use the following syntax conventions to utilize [report parameters](xref:4812) in the [Expression Editor](xref:120091):

* Insert [report parameters](xref:4812) using the "Parameters." prefix before their names.

  _[Parameters.parameter1]_
* When referencing [report parameters](xref:4812) in the [Filter Editor](xref:4803) and using [query parameters](xref:17387) in data source queries, type a question mark before the parameters' names. 

  _?parameter1_

## Collection Elements Verification
Use brackets "[]" to check if a collection contains an element that satisfies a condition. The following expression returns _true_ if the Accounts collection contains at least one element that satisfies the _[Amount] == 100_ condition:

_[Accounts][[Amount] == 100]_

The following expression returns _false_ if the Accounts collection is empty:

_[Accounts][]_

Refer to the <xref:12441> topic to see an example how to use this syntax.

## Parent Relating Operator
Use the parent relating operator ('^' character) to refer to a parent in expressions written in the context of a child. You can apply this operator successively to navigate multiple parent relationships. 

You can use this operator to refer to the currently processed report group. This allows you to calculate aggregates within groups using expressions like the following:

_[][[^.CategoryID] == [CategoryID]].Sum([UnitPrice])_

Refer to the <xref:12441> topic for details.

## Grouping Clauses with Brackets
It is important to use brackets to ensure that your expression returns the intended results.

For instance, the following expression for objects of the Customer type returns all of the Customers where an Account exists with a Date of 8/25/2006 and where an account exists with an Amount of 100:

_[Accounts][[Date] == #8/25/2006#] &amp;&amp; [Accounts][[Amount] == 100]_

Construct the expression as in the following example to search for all Customers that have an Account with both a Date of 8/25/2006 and an Amount of 100:

_[Accounts][[Date] == #8/25/2006# &amp;&amp; [Amount] == 100]_

## Operator Precedence
When an expression contains multiple operators, their precedence controls the order in which expression elements are evaluated.

* Literal values
* Parameters
* Identifiers
* OR (left-associative)
* AND (left-associative)
* '.' relationship qualifier (left-associative)
* ==, !=
* &lt;, &gt;, &lt;=, &gt;=
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





