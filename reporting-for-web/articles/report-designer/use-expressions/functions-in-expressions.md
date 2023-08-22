---
title: 'Functions in Expressions'
owner: Sergey Andreev
---
# Functions in Expressions

This topic lists the functions that you can use in an [expression](expressions-overview.md).

## Aggregate Functions

| Function | Description | Example |
|---|---|---|
| Avg(Value) | Evaluates the average of the values in the collection. | [Products].Avg([UnitPrice]) |
| Count() | Returns the number of objects in a collection. | [Products].Count() |
| Exists() | Determines whether the object exists in the collection. | [Categories][[CategoryID] == 7].Exists() |
| Max(Value) | Returns the maximum expression value in a collection. | [Products].Max([UnitPrice]) |
| Min(Value) | Returns the minimum expression value in a collection. | [Products].Min([UnitPrice]) |
| Single() | Returns an object if it is the only element in a collection. | [Accounts].Single() is not null |
| Single(Expression) | You can pass an expression as a parameter: *[Collection][Condition].Single(Expression)*. This function returns the _Expression_ if the _Collection_ contains only one object that meets the specified _Condition_ (optional).  | [Collection].Single([Property1]) - returns the found object's property value.|
| Sum(Value) | Returns the sum of all expression values in the collection. | [Products].Sum([UnitsInStock]) |

## Date and Time Functions

| Function | Description | Example |
|---|---|---|
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
| DateTimeFromParts(Year, Month, Day, Hour, Minute, Second, Millisecond) | Returns a date value constructed from the specified Year, Month, Day, Hour, Minute, Second, and Millisecond. |
| DateTimeFromParts(2018, 5, 5, 20) |
| GetDate(DateTime) | Extracts a date from the defined DateTime. | GetDate([OrderDateTime])   |
| GetDay(DateTime) | Extracts a day from the defined DateTime. | GetDay([OrderDate])   |
| GetDayOfWeek(DateTime) | Extracts a day of the week from the defined DateTime. | GetDayOfWeek([OrderDate])   |
| GetDayOfYear(DateTime) | Extracts a day of the year from the defined DateTime. | GetDayOfYear([OrderDate])   |
| GetHour(DateTime) | Extracts an hour from the defined DateTime. | GetHour([StartTime])   |
| GetMilliSecond(DateTime) | Extracts milliseconds from the defined DateTime. | GetMilliSecond([StartTime]) |
| GetMinute(DateTime) | Extracts minutes from the defined DateTime. | GetMinute([StartTime])   |
| GetMonth(DateTime) | Extracts a month from the defined DateTime. | GetMonth([StartTime])   |
| GetSecond(DateTime) | Extracts seconds from the defined DateTime. | GetSecond([StartTime])   |
| GetTimeOfDay(DateTime) | Extracts the time of day from the defined DateTime in ticks. | GetTimeOfDay([StartTime]) |
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
| LocalDateTimeLastMonth() | Returns a DateTime value corresponding to the first day of the previous month. | AddMonths(LocalDateTimeLastMonth(), 5)   |
| LocalDateTimeLastWeek() | Returns a date-time value corresponding to the first day of the previous week. | AddDays(LocalDateTimeLastWeek(), 5)   |
| LocalDateTimeLastYear() | Returns a DateTime value corresponding to the first day of the previous year. | AddYears(LocalDateTimeLastYear(), 5)   |
| LocalDateTimeNextMonth() | Returns a date-time value corresponding to the first day of the next month. | AddMonths(LocalDateTimeNextMonth(), 5)   |
| LocalDateTimeNextWeek() | Returns a date-time value corresponding to the first day of the following week. | AddDays(LocalDateTimeNextWeek(), 5)   |
| LocalDateTimeNextYear() | Returns a date-time value corresponding to the first day of the following year. | AddYears(LocalDateTimeNextYear(), 5)   |
| LocalDateTimeNow() | Returns a date-time value corresponding to the current moment in time. | AddDays(LocalDateTimeNow(), 5)   |
| LocalDateTimeThisMonth() | Returns a date-time value corresponding to the first day of the current month. | AddMonths(LocalDateTimeThisMonth(), 5)   |
| LocalDateTimeThisWeek() | Returns a date-time value corresponding to the first day of the current week. | AddDays(LocalDateTimeThisWeek(), 5)   |
| LocalDateTimeThisYear() | Returns a date-time value corresponding to the first day of the current year. | AddYears(LocalDateTimeThisYear(), 5)   |
| LocalDateTimeToday() | Returns a date-time value corresponding to Today. | AddDays(LocalDateTimeToday(), 5)   |
| LocalDateTimeTomorrow() | Returns a date-time value corresponding to Tomorrow. | AddDays(LocalDateTimeTomorrow(), 5)   |
| LocalDateTimeTwoMonthsAway() | Returns a DateTime value corresponding to the first day of the following month. | AddMonths(LocalDateTimeTwoMonthAway(), 5)   |
| LocalDateTimeTwoWeeksAway() | Returns a DateTime value corresponding to the first day of the following week. | AddDays(LocalDateTimeTwoWeeksAway(), 5)   |
| LocalDateTimeTwoYearsAway() | Returns a DateTime value corresponding to the first day of the following year. | AddYears(LocalDateTimeTwoYearsAway(), 5)   |
| LocalDateTimeYearBeforeToday() | Returns a DateTime value corresponding to the same date one year ago. | AddYears(LocalDateTimeYearBeforeToday(), 5)   |
| LocalDateTimeYesterday() | Returns a date-time value corresponding to Yesterday. | AddDays(LocalDateTimeYesterday(), 5)   |
| Now() | Returns the current system date and time. | AddDays(Now(), 5)   |
| Today() | Returns the current date. Regardless of the actual time, this function returns midnight of the current date. | AddMonths(Today(), 1)   |
| UtcNow() | Returns the current system date and time, expressed as Coordinated Universal Time (UTC). | AddDays(UtcNow(), 7) |

## Logical Functions

* Iif(Expression1, True_Value1, ..., ExpressionN, True_ValueN, False_Value)  
  Returns one of several specified values depending upon the values of logical expressions.

  The function can take *2N+1* arguments (*N* - the number of specified logical expressions):

  - Each odd argument specifies a logical expression.

  - Each even argument specifies the value that is returned if the previous expression evaluates to **True**.

  - **...**

  - The last argument specifies the value that is returned if the previously evaluated logical expressions yielded **False**.
  ```
  Iif(Name = 'Bob', 1, Name = 'Dan', 2, Name = 'Sam', 3, 4)")
  ```

* IsNull(Value)  
  Returns True if the specified Value is NULL.
  ```
  IsNull([OrderDate])
  ```

* IsNull(Value1, Value2)  
  Returns Value1 if it is not set to NULL; otherwise, Value2 is returned.
  ```
  IsNull([ShipDate], [RequiredDate])
  ```

* IsNullOrEmpty(String)  
  Returns True if the specified String object is NULL or an empty string; otherwise, False is returned.
  ```
  IsNullOrEmpty([ProductName])
  ```

## Math Functions

| Function | Description | Example |
|---|---|---|
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

## Reporting Functions

* Argb(Alpha, Red, Green, Blue)  
  Returns a string defining a color using the Alpha, Red, Green, and Blue color channel values.
  ```
  Argb(1,200, 30, 200)  
  /* Result: '1,200,30,200'*/
  ```

* GetDisplayText(?parameterName)  
  Returns a Display Text for a parameter's lookup value.

  For **non-lookup parameters**, this function returns a value converted to string.
  ```
  /* ?employeeParameter stores static or dynamic predefined values  
  where EmployeeID is a parameter value  
  and EmployeeName is a display text. */  
  GetDisplayText(?employeeParameter)
  ```

* Rgb(Red, Green, Blue)  
  Returns a string defining a color using the Red, Green, and Blue color channel values.
  ```
  Rgb(30,200,150)  
  /* Result: '30,200,150' */
  ```

## String Functions

| Function | Description | Example |
|---|---|---|
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
| PadRight(String, Length) | Right-aligns the defined string�s characters, padding its left side with empty space characters up to a specified total length. | PadRight([Name], 30) |
| PadRight(String, Length, Char) | Right-aligns the defined string�s characters, padding its left side with the specified Char up to a specified total length. | PadRight([Name], 30, '>') |
| Remove(String, StartPosition) | Deletes all the characters from this instance, beginning at a specified position. | Remove([Name], 3) |
| Remove(String, StartPosition, Length) | Deletes a specified number of characters from this instance, beginning at a specified position. | Remove([Name], 0, 3) |
| Replace(String1, SubString2, String3) | Returns a copy of String1, in which SubString2 has been replaced with String3. | Replace([Name], 'The ', '') |
| Reverse(String) | Reverses the order of elements within String. | Reverse([Name]) |
| StartsWith(String1, SubString1) | Returns True if the beginning of String1 matches SubString1; otherwise, False. | StartsWith([Title], 'The best')   |
| Substring(String, StartPosition, Length) | Retrieves a substring from String. The substring starts at StartPosition and has a specified Length. | Substring([Description], 2, 3) |
| Substring(String, StartPosition) | Retrieves a substring from String. The substring starts at StartPosition. | Substring([Description], 2) |
| ToStr(Value) | Returns a string representation of an object. | ToStr([ID]) |
| Trim(String) | Removes all leading and trailing SPACE characters from String. | Trim([ProductName])   |
| Upper(String) | Returns String in uppercase. | Upper([ProductName])   |

## Functions for Expression Bindings and Calculated Fields

Below is a list of functions that are used to construct [expression bindings](data-binding-modes.md) and [calculated fields](../shape-report-data/use-calculated-fields/calculated-fields-overview.md):

* NewLine()  
  Returns the newline string defined for the current environment.
  ```
  [CategoryName]+NewLine()+[Description]
  /*
  Result:
  Beverages
  Soft drinks, coffees, teas, beers and ales.
  /*
  ```

* FormatString(Format, Value1, ... , ValueN)  
  Returns the specified string with formatted field values.  
  See the following topic for details: [Format Data](../shape-report-data/format-data.md).
  ```
  FormatString('{0:$0.00}', [UnitPrice])
  /*
  Result: $45.60
  */
  ```

* Rgb(Red, Green, Blue)  
  Returns a string defining a color using the Red, Green, and Blue color channel values.
  ```
  Rgb(30,200,150)
  /*
  Result: '30,200,150'
  */
  ```

* Join()  
  Concatenates the [multi-value report parameter](../use-report-parameters/multi-value-report-parameters.md)'s values into a string. This function is useful when you [bind a multi-value parameter to a label](../use-report-parameters/create-a-report-parameter.md) to display the parameter's values in a report.

  This function has two overloads:

  * Join(parameter) - concatenates the specified parameter's values using a comma as a separator.
  * Join(parameter, separator) - concatenates the specified parameter's values using the specified separator.
  ```
  Join(?CategoriesParameter)
  /*
  Result: Beverages, Condiments
  */
  Join(?CategoriesParameter, newline())
  /*
  Result:
  Beverages
  Condiments
  */

## Functions for Stored Procedures

The following functions are used to bind a report to a stored procedure:

* Join()  
  Concatenates the [multi-value report parameter](../use-report-parameters/multi-value-report-parameters.md)'s values into a string. This function can be used when mapping multi-value report parameters to query parameters generated from a stored procedure's parameters. Refer to the following topic for more information: [Query Parameters](../bind-to-data/specify-query-parameters.md).

  This function has two overloads:

  * Join(parameter) - concatenates the specified parameter's values using a comma as a separator.
  * Join(parameter, separator) - concatenates the specified parameter's values using the specified separator.
  ```
  Join(?Parameter1)
  ```

* CreateTable(Column1, ..., ColumnN)  
  Creates a table from several multi-value parameters' values. This function can be used when mapping multi-value report parameters to the query parameter that is generated from a stored procedure's [User Defined Table Type](https://docs.microsoft.com/en-us/sql/relational-databases/tables/use-table-valued-parameters-database-engine) parameter. Refer to the following topic for more information: [Query Parameters](../bind-to-data/specify-query-parameters.md).
  ```
  CreateTable(?Parameter1, ..., ?ParameterN)
  ```

## Functions for Summary Expression Editor

Use the following functions when you [calculate a summary](../shape-report-data/calculate-summaries.md) across a report and its groups:

* sumAvg(Expression)  
  Calculates the average of all values within the specified summary region (group, page, or report).
  ```
  sumAvg([UnitPrice])
  ```

* sumCarryoverSum(Expression)
  
  Calculates the carried forward and brought forward totals.

  ```
  sumCarryoverSum([Amount])
  ```

* sumCount(Expression)  
  Counts the number of values within the specified summary region (group, page, or report). In a simple scenario, you may not pass a parameter.

  When using this function in a [master-detail report](../create-reports/master-detail-reports-with-detail-report-bands.md)'s master band and passing a detail field as a parameter, the function counts the number of records within the detail band.

  See also:
  * [Count the Number of Records in a Report or Group](../shape-report-data/count-elements-and-values/count-the-number-of-records-in-a-report-or-group.md)
  * [Count the Number of Groups in a Report](../shape-report-data/count-elements-and-values/count-the-number-of-groups-in-a-report.md)
  ```
  sumCount([UnitPrice])
  ```

* sumDAvg(Expression)  
  Calculates the average of all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDAvg([UnitPrice])
  ```

* sumDCount(Expression)  
  Counts the number of **distinct** values within the specified summary region (group, page, or report). In a simple scenario, you may not pass a parameter.
  ```
  sumDCount([UnitPrice])
  ```

* sumDStdDev(Expression)  
  Calculates the standard deviation of all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDStdDev([UnitPrice])
  ```

* sumDStdDevP(Expression)  
  Calculates the standard population deviation of all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDStdDevP([UnitPrice])
  ```

* sumDSum(Expression)  
  Calculates the total of all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDSum([UnitPrice])
  ```

* sumDVar(Expression)  
  Calculates the amount of variance for all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDVar([UnitPrice])
  ```

* sumDVarP(Expression)  
  Calculates the population variance of all **distinct** values within the specified summary region (group, page, or report).
  ```
  sumDVarP([UnitPrice])
  ```

* sumMax(Expression)  
  Calculates the maximum of all values within the specified summary region (group, page, or report).
  ```
  sumMax([UnitPrice])
  ```

* sumMedian(Expression)  
  Finds the middle number within a sequence.

  If the total number of elements is odd, this function returns the value of the middle number in a sequence. If the total number of elements is even, this function returns the arithmetical mean of the two middle numbers.
  ```
  sumMedian([UnitPrice])
  ```

* sumMin(Expression)  
  Calculates the minimum of all values within the specified summary region (group, page, or report).
  ```
  sumMin([UnitPrice])
  ```

* sumPercentage(Expression)  
  Calculates the percent ratio of the current data row's value to the total of all the values within the specified summary region (group, page, or report).
  ```
  sumPercentage([UnitPrice])
  ```

* sumRecordNumber(Expression)  
  Returns the current record number in the specified summary region (group, page, or report). This means, for instance, if the summary is calculated for a group, then the record number is calculated only within that group, and is reset every time a new group is started.

  In a simple scenario, you may not pass a parameter.

  See also: [Display Row Numbers on a Report, Group, or Page](../shape-report-data/count-elements-and-values/display-row-numbers-in-a-report-group-or-page.md)
  ```
  sumRecordNumber()
  ```

* sumRunningSum(Expression)  
  Calculates the sum of all previous values displayed before the current data row with the current data row value.
  ```
  sumRunningSum([UnitPrice])
  ```

* sumStdDev(Expression)  
  Calculates the standard deviation of all values within the specified summary region (group, page, or report).
  ```
  sumStdDev([UnitPrice])
  ```

* sumStdDevP(Expression)  
  Calculates the standard population deviation of all values within the specified summary region (group, page, or report).
  ```
  sumStdDevP([UnitPrice])
  ```

* sumSum(Expression)  
  Calculates the total of all values within the specified summary region (group, page, or report).
  ```
  sumSum([UnitsInStock])
  ```

* sumVar(Expression)  
  Calculates the amount of variance for all values within the specified summary region (group, page, or report).
  ```
  sumVar([UnitPrice])
  ```

* sumVarP(Expression)  
  Calculates the population variance of all values within the specified summary region (group, page, or report).
  ```
  sumVarP([UnitPrice])
  ```

* sumWAvg(Expression, Expression)  
  Calculates the weighted average of all values within the specified summary region (group, page, or report). This summary type returns the result of the following operation: Sum(Expression1 * Expression2) / Sum(Expression2).
  ```
  sumWAvg([UnitPrice])
  ```
