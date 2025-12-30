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
| Join() | Concatenates all Expression values in the _Collection_ based on the specified _Condition_ (optional) into a single string separated by the specified _Separator_ (optional). If you do not specify a _Separator_, the function uses a comma.<br>The function has the following overloads:<br>`[Collection][Condition].Join(Expression)`<br>`[Collection][Condition].Join(Expression, Separator)`| The following expression concatenates _CompanyName_ field values within a report grouped by the _CategoryID_ field into a single string separated by a semicolon:<br>`[][[CategoryID] == [^.CategoryID]].Join([CompanyName], ';')`|
| Max(Value) | Returns the maximum expression value in a collection. | [Products].Max([UnitPrice]) |
| Min(Value) | Returns the minimum expression value in a collection. | [Products].Min([UnitPrice]) |
| Single() | Returns an object if it is the only element in a collection. | [Accounts].Single() is not null |
| Single(Expression) | You can pass an expression as a parameter: *[Collection][Condition].Single(Expression)*. This function returns the _Expression_ if the _Collection_ contains only one object that meets the specified _Condition_ (optional).  | [Collection].Single([Property1]) - returns the found object's property value.|
| Sum(Value) | Returns the sum of all expression values in the collection. | [Products].Sum([UnitsInStock]) |

## Date and Time Functions

## Date and Time Functions

| Function | Description | Example |
|---|---|---| 
| IsThisWeek(Date) | Returns `True` if the specified date falls within the current week.| _Example_: `IsThisWeek([OrderDate])` |
|IsThisMonth(Date) | Returns `True` if the specified date falls within the current month. <br>To create the **IsThisMonth** operator using the `Parse` method, use the following syntax: **CriteriaOperator.Parse(“IsThisMonth(StartDate)”)**. | _Example_: `IsThisMonth([OrderDate])` |
|IsThisYear(Date) | Returns `True` if the specified date falls within the current year. | _Example_: `IsThisYear([OrderDate])` |
|LocalDateTimeLastMonth() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is one month before the current date, and the time part of 00:00:00. | _Example_: `AddMonths(LocalDateTimeLastMonth(), 5)` |
|LocalDateTimeLastYear() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is the first day of the previous year, and the time part of 00:00:00. | _Example_: `AddYears(LocalDateTimeLastYear(), 5)` |
|LocalDateTimeTwoMonthsAway() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the month after the next month, and the time part of 00:00:00. | _Example_: `AddMonths(LocalDateTimeTwoMonthAway(), 5)` |
|LocalDateTimeTwoYearsAway() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the year after the next year, and the time part of 00:00:00. | _Example_: `AddYears(LocalDateTimeTwoYearsAway(), 5)` |
|LocalDateTimeYearBeforeToday() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the date one year ago, and the time part of 00:00:00. | _Example_: `AddYears(LocalDateTimeYearBeforeToday(), 5)` |
|InDateRange(Date, FromDate, ToDate) | Returns `True` if the date part of the first operand is greater than or equal to the date part of the second operand and less than or equal to the date part of the third operand. Otherwise, returns `False`. If operands cannot be compared, returns `null`. | _Example_: `InDateRange([OrderDate], #2022-01-01 00:00:00#, #2022-12-31 23:59:59#)` |
|IsJanuary(Date) | Returns True if the specified date falls within January. | _Example_: `IsJanuary([OrderDate])` |
|IsFebruary(Date) | Returns True if the specified date falls within February. | _Example_: `IsFebruary([OrderDate])` |
|IsMarch(Date) | Returns True if the specified date falls within March. | _Example_: `IsMarch([OrderDate])` |
|IsApril(Date) | Returns True if the specified date falls within April. | _Example_: `IsApril([OrderDate])` |
|IsMay(Date) | Returns True if the specified date falls within May. | _Example_: `IsMay([OrderDate])` |
|IsJune(Date) | Returns True if the specified date falls within June. | _Example_: `IsJune([OrderDate])` |
|IsJuly(Date) | Returns True if the specified date falls within July. | _Example_: `IsJuly([OrderDate])` |
|IsAugust(Date) | Returns True if the specified date falls within August. | _Example_: `IsAugust([OrderDate])` |
|IsSeptember(Date) | Returns True if the specified date falls within September. | _Example_: `IsSeptember([OrderDate])` |
|IsOctober(Date) | Returns True if the specified date falls within October. | _Example_: `IsOctober([OrderDate])` |
|IsNovember(Date) | Returns True if the specified date falls within November. | _Example_: `IsNovember([OrderDate])` |
|IsDecember(Date) | Returns True if the specified date falls within December. | _Example_: `IsDecember([OrderDate])` |
|IsLastMonth(Date) | Returns True if the specified date falls within the previous month. | _Example_: `IsLastMonth([OrderDate])` |
|IsLastYear(Date) | Returns True if the specified date falls within the previous year. | _Example_: `IsLastYear([OrderDate])` |
|IsNextMonth(Date) | Returns True if the specified date falls within the next month. | _Example_: `IsNextMonth([OrderDate])` |
|IsNextYear(Date) | Returns True if the specified date falls within the next year. | _Example_: `IsNextYear([OrderDate])` |
|IsYearToDate(Date) | Returns `True` if the specified date falls within the period that starts from the first day of the current year and continues until the current date (including the current date). | _Example_: `IsYearToDate([OrderDate])` |
|IsSameDay(\[Date1\], \[Date2\]) | Returns `True` if the specified date/time value falls within the same day. | _Example_: `IsSameDay([OrderDate], [ShippedDate])` |
|LocalDateTimeDayAfterTomorrow() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is two days after the current date, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeDayAfterTomorrow(), 5)` |
|LocalDateTimeLastWeek() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is 7 days before the start of the current week, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeLastWeek(), 5)` |
|LocalDateTimeNextMonth() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is the first day of the next month, and the time part of 00:00:00. | _Example_: `AddMonths(LocalDateTimeNextMonth(), 5)` |
|LocalDateTimeNextWeek() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that has the date part that is 7 days after the start of the current week, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeNextWeek(), 5)` |
|LocalDateTimeNextYear() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that corresponds to the first day of the next year, and the time part of 00:00:00. | _Example_: `AddYears(LocalDateTimeNextYear(), 5)` |
|LocalDateTimeNow() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that is the current moment in time. | _Example_: `AddDays(LocalDateTimeNow(), 5)` |
|LocalDateTimeThisMonth() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the current month, and the time part of 00:00:00. | _Example_: `AddMonths(LocalDateTimeThisMonth(), 5)` |
|LocalDateTimeThisWeek() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the current week, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeThisWeek(), 5)` |
|LocalDateTimeThisYear() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the current year, and the time part of 00:00:00. | _Example_: `AddYears(LocalDateTimeThisYear(), 5)` |
|LocalDateTimeToday() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the start of the current day, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeToday(), 5)` |
|LocalDateTimeTomorrow() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the next day, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeTomorrow(), 5)` |
|LocalDateTimeTwoWeeksAway() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the first day of the week after the next week, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeTwoWeeksAway(), 5)` |
|LocalDateTimeYesterday() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value with the date part that is the previous day, and the time part of 00:00:00. | _Example_: `AddDays(LocalDateTimeYesterday(), 5)` |
|AddTicks(DateTime, AddTicks) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that is the specified number of ticks before or after a specified start date. | _Example_: `AddTicks([OrderDate], 500000)` |
|AddMilliSeconds(Time, MilliSecondsCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[TimeOnly](https://learn.microsoft.com/dotnet/api/system.timeonly) value that is the specified number of milliseconds before or after a specified start date/time.| _Example_: `AddMilliSeconds([StartTime], 200)` |
|AddSeconds(Time, SecondsCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[TimeOnly](https://learn.microsoft.com/dotnet/api/system.timeonly) value that is the specified number of seconds before or after a specified start date/time. | _Example_: `AddSeconds([StartTime], 120)` |
|AddMinutes(Time, MinutesCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[TimeOnly](https://learn.microsoft.com/dotnet/api/system.timeonly) value that is the specified number of minutes before or after a specified start date/time. | _Example_: `AddMinutes([StartTime], 30)` |
|AddHours(Time, HoursCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[TimeOnly](https://learn.microsoft.com/dotnet/api/system.timeonly) value that is the specified number of hours before or after a specified start date/time. | _Example_: `AddHours([StartTime], 5)` |
|AddDays(Date, DaysCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[DateOnly](https://learn.microsoft.com/dotnet/api/system.dateonly) value that is the specified number of days before or after a specified start date. | _Example_: `AddDays([OrderDate], 10)` |
|AddMonths(Date, MonthsCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[DateOnly](https://learn.microsoft.com/dotnet/api/system.dateonly) value that is the specified number of months before or after a specified start date.| _Example_: `AddMonths([OrderDate], 3)` |
|AddYears(Date, YearsCount) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime)/[DateOnly](https://learn.microsoft.com/dotnet/api/system.dateonly) value that is the specified number of years before or after a specified start date. | _Example_: `AddYears([OrderDate], 2)` |
|AddTimeSpan(DateTime, TimeSpan) | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that differs by a specified amount of time from a specified date. | _Example_: `AddTimeSpan([OrderDate], [Duration])` |
|DateDiffDay(StartDate, EndDate) | Returns the number of day boundaries between the specified dates. | _Example_: `DateDiffDay([OrderDate], Now())` |
|DateDiffMonth(StartDate, EndDate) | Returns the number of month boundaries between the specified dates. | _Example_: `DateDiffMonth([OrderDate], Now())` |
|DateDiffYear(StartDate, EndDate) | Returns the number of year boundaries between the specified dates. | _Example_: `DateDiffYear([OrderDate], Now())` |
|DateDiffMilliSecond(StartTime, EndTime) | Returns the number of millisecond boundaries between the specified dates/times. | _Example_: `DateDiffMilliSecond([StartTime], Now())` |
|DateDiffMinute(StartTime, EndTime) | Returns the number of minute boundaries between the specified dates/times.| _Example_: `DateDiffMinute([StartTime], Now())` |
|DateDiffSecond(StartTime, EndTime) | Returns the number of second boundaries between the specified dates/times.| _Example_: `DateDiffSecond([StartTime], Now())` |
|DateDiffHour(StartTime, EndTime) | Returns the number of hour boundaries between the specified dates/times. | _Example_: `DateDiffHour([StartTime], Now())` |
|DateDiffTick(StartDate, EndDate) | Returns the number of tick boundaries between the specified dates. | _Example_: `DateDiffTick([OrderDate], Now())` |
|GetDate(Date) | Returns the date part of the specified date.| _Example_: `GetDate([OrderDate])` |
|GetYear(Date) | Gets the year in the specified date. | _Example_: `GetYear([OrderDate])` |
|GetMonth(Date) | Gets the month in the specified date. | _Example_: `GetMonth([OrderDate])` |
|GetDay(Date) | Gets the day of the month in the specified date. | _Example_: `GetDay([OrderDate])` |
|GetDayOfYear(Date) | Gets the day of the year in the specified date. | _Example_: `GetDayOfYear([OrderDate])` |
|GetDayOfWeek(Date) | Gets the day of the week in the specified date. | _Example_: `GetDayOfWeek([OrderDate])` |
|GetHour(Time) | Returns the hours value in the specified date/time. | _Example_: `GetHour([StartTime])` |
|GetMinute(Time) | Returns the minutes value in the specified date/time. | _Example_: `GetMinute([StartTime])` |
|GetSecond(Time) | Returns the seconds value in the specified date/time.| _Example_: `GetSecond([StartTime])` |
|GetMilliSecond(Time) | Returns the milliseconds value in the specified date/time. | _Example_: `GetMilliSecond([StartTime])` |
|GetTimeOfDay(DateTime) | Gets the time part of the specified date. | _Example_: `GetTimeOfDay([OrderDate])` |
|Now() | Returns the [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that is the current date and time. | _Example_: `AddDays(Now(), 7)` |
|Today() | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) value that is the current date. The time part is set to 00:00:00. | _Example_: `AddDays(Today(), 3)` |
|UtcNow() | Returns a [DateTime](https://learn.microsoft.com/dotnet/api/system.datetime) object that is the current date and time in Universal Coordinated Time (UTC). | _Example_: `AddDays(UtcNow(), 7)` |
|DateTimeFromParts(Year, Month, Day) | Returns a date value constructed from the specified Year, Month, Day, Hour, Minute, Second, and Millisecond. | _Example_: `DateTimeFromParts([Year], [Month], [Day])` |
|DateTimeFromParts(Year, Month, Day, Hour) | Returns a date value constructed from the specified Year, Month, Day, Hour, Minute, Second, and Millisecond. | _Example_: `DateTimeFromParts([Year], [Month], [Day], [Hour])` |
|DateTimeFromParts(Year, Month, Day, Hour, Minute) | Returns a date value constructed from the specified Year, Month, Day, Hour, Minute, Second, and Millisecond. | _Example_: `DateTimeFromParts([Year], [Month], [Day], [Hour], [Minute])` |
|DateTimeFromParts(Year, Month, Day, Hour, Minute, Second) | Returns a date value constructed from the specified Year, Month, Day, Hour, Minute, Second, and Millisecond. | _Example_: `DateTimeFromParts([Year], [Month], [Day], [Hour], [Minute], [Second])` |
|DateOnlyFromParts(Year, Month, Day) | Returns a [DateOnly](https://learn.microsoft.com/dotnet/api/system.dateonly) value constructed from the specified Year, Month, and Day.| _Example_: `DateOnlyFromParts([Year], [Month], [Day])` |
|TimeOnlyFromParts(Hour, Minute) | Returns a TimeOnly value constructed from the specified hour, minute, seconds (optional), and milliseconds (optional). | _Example_: `TimeOnlyFromParts([Hour], [Minute])` |
|TimeOnlyFromParts(Hour, Minute, Second) | Returns a TimeOnly value constructed from the specified hour, minute, seconds (optional), and milliseconds (optional). | _Example_: `TimeOnlyFromParts([Hour], [Minute], [Second])` |
|TimeOnlyFromParts(Hour, Minute, Second, Millisecond) | Returns a TimeOnly value constructed from the specified hour, minute, seconds (optional), and milliseconds (optional). | _Example_: `TimeOnlyFromParts([Hour], [Minute], [Second], [Millisecond])` |
|AfterMidday(Time) | Returns `True` if the specified time is after 12:00 PM. | _Example_: `AfterMidday([StartTime])` |
|BeforeMidday(Time) | Returns `True` if the specified time is before 12:00 PM. | _Example_: `BeforeMidday([StartTime])` |
|IsAfternoon(Time) | Returns `True` if the specified time falls between 12:00 PM and 6:00 PM. | _Example_: `IsAfternoon([StartTime])` |
|IsEvening(Time) | Returns `True` if the specified time falls between 6:00 PM and 9:00 PM. | _Example_: `IsEvening([StartTime])` |
|IsFreeTime(Time) | Returns `True` if the specified time falls within free time. | _Example_: `IsFreeTime([StartTime])` |
|IsLastHour(Time) | Returns `True` if the specified time falls within the last hour. | _Example_: `IsLastHour([StartTime])` |
|IsLunchTime(Time) | Returns `True` if the specified time falls within the lunch time. | _Example_: `IsLunchTime([StartTime])` |
|IsMorning(Time) | Returns `True` if the specified time falls within between 6:00 AM and 12:00 PM. | _Example_: `IsMorning([StartTime])` |
|IsNextHour(Time) | Returns `True` if the specified time falls within the next hour. | _Example_: `IsNextHour([StartTime])` |
|IsNight(Time) | Returns `True` if the specified time falls between 9:00 PM and 9:00 AM. | _Example_: `IsNight([StartTime])` |
|IsSameHour(Time) | Returns `True` if the specified time falls within the same hour. | _Example_: `IsSameHour([StartTime])` |
|IsSameTime(Time) | Returns `True` if the specified time falls within the same time of day (hour and minute). | _Example_: `IsSameTime([StartTime])` |
|IsThisHour(Time) | Returns `True` if the specified time falls within the hour. | _Example_: `IsThisHour([StartTime])` |
|IsWorkTime(Time) | Returns `True` if the specified time falls within work time. | _Example_: `IsWorkTime([StartTime])` |

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

* CurrentRowIndexInGroup()

   Returns the current row's index within the group.

    The following expression adds row indexes in the group:

    ```CurrentRowIndexInGroup(0) + 1```

* GroupIndex(level)

   Locates the parent group row at the specified nesting level and returns that row's index. 

    The following expression displays indexes of root-level groups:

    ```GroupIndex(1) + 1```  

* NextRowColumnValue(columnName)

    Obtains the next row and returns the value from the specified column.

* PrevRowColumnValue(columnName)

    Obtains the previous row and returns the value from the specified column.  

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

The following functions are used to [bind a report to a stored procedure](../bind-to-data/bind-a-report-to-a-stored-procedure.md):

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
