---
title: Expression Syntax
owner: Mary Sammal
---

# Expression Constants, Operators, and Functions

The table below contains constants, operators, and functions you can use in [expressions](..\use-expressions.md).

## Constants
<table><tr><th><p>Constant</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>String constants</p>
</td><td><p>Wrap string constants in apostrophes.</p>
<p>If a string contains an apostrophe, double the apostrophe.</p>
</td><td><p>[Country] == &#39;France&#39;</p>
<p>[Name] == &#39;O&#39;&#39;Neil&#39;</p>
</td></tr><tr><td><p>Date-time constants</p>
</td><td><p>Wrap date-time constants in &#39;#&#39;.</p>
</td><td><p>[OrderDate] &gt;= #2018-03-22 13:18:51.94944#</p>
</td></tr><tr><td><p>True</p>
</td><td><p>Represents the Boolean True value.</p>
</td><td><p>[InStock] == True</p>
</td></tr><tr><td><p>False</p>
</td><td><p>Represents the Boolean False value.</p>
</td><td><p>[InStock] == False</p>
</td></tr><tr><td><p>Enumeration</p>
</td><td><p>Specify an enumeration value using its underlying integer value.</p>
</td><td><p>[Status] == 1</p>
<p>You cannot specify an enumeration value using its qualified name. The following criteria <strong>is incorrect</strong>:</p>
<p>[Status] = Status.InProgress</p>
<p>You can use the <see cref="T:DevExpress.Data.Filtering.EnumProcessingHelper"></see> class&#39; static methods to register custom enumerations, and then refer to enumeration values as follows:</p>
<p>Status = ##Enum#MyNamespace.Status,InProgress#</p>
</td></tr><tr><td><p>Guid</p>
</td><td><p>Wrap a Guid constant in curly braces. Use Guid constants in a relational operation with equality or inequality operators only.</p>
</td><td><p>[OrderID] == {513724e5-17b7-4ec6-abc4-0eae12c72c1f}</p>
</td></tr><tr><td><p>Numeric</p>
</td><td><p>Specify different numeric constant types in a string form using suffixes:</p>
<ul>
<li>Int32 (int) - <em>1</em></li>
<li>Int16 (short) - <em>1s</em></li>
<li>Byte (byte) - <em>1b</em></li>
<li>Double (double) - <em>1.0</em></li>
<li>Single (float) - <em>1.0f</em></li>
<li>Decimal (decimal) - <em>1.0m</em></li>
</ul>
</td><td><p>[Price] == 25.0m</p>
</td></tr><tr><td><p>?</p>
</td><td><p>Represents a null reference that does not refer to any object.</p>
<p>We recommend using the <strong>IsNull</strong> unary operator (for example, &quot;[Region] is null&quot;) or the <strong>IsNull</strong> logical function (for example, &quot;IsNull([Region])&quot;) instead.</p>
</td><td><p>[Region] != ?</p>
</td></tr></table>

## Operators

<table><tr><th><p>Operator</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>+</p>
</td><td><p>Adds the value of one numeric expression to another or concatenates two strings.</p>
</td><td><p>[UnitPrice] + 4</p>
<p>[FirstName] + &#39; &#39; + [LastName]</p>
</td></tr><tr><td><p>-</p>
</td><td><p>Finds the difference between two numbers.</p>
</td><td><p>[Price1] - [Price2]</p>
</td></tr><tr><td><p>*</p>
</td><td><p>Multiplies the value of two expressions.</p>
</td><td><p>[Quantity] * [UnitPrice] * (1 - [BonusAmount])</p>
</td></tr><tr><td><p>/</p>
</td><td><p>Divides the first operand by the second.</p>
</td><td><p>[Quantity] / 2</p>
</td></tr><tr><td><p>%</p>
</td><td><p>Returns the remainder (modulus) obtained by dividing one numeric expression by another.</p>
</td><td><p>[Quantity] % 3</p>
</td></tr><tr><td><p>|</p>
</td><td><p>Performs a bitwise inclusive OR on two numeric expressions. Compares each bit of its first operand to the corresponding bit of its second operand. If either bit is 1, the corresponding resulting bit is set to 1. Otherwise, the corresponding resulting bit is set to 0.</p>
</td><td><p>[Number] | [Number]</p>
</td></tr><tr><td><p>&amp;</p>
</td><td><p>The bitwise AND operator. Compares each bit of its first operand to the corresponding bit of its second operand. If both bits are 1, the corresponding resulting bit is set to 1. Otherwise, the corresponding resulting bit is set to 0.</p>
</td><td><p>[Number] &amp; 10</p>
</td></tr><tr><td><p>^</p>
</td><td><p>Performs a bitwise exclusive OR on two numeric expressions.</p>
</td><td><p>[Number] ^ [Number]</p>
</td></tr><tr><td><p>==</p>
<p>=</p>
</td><td><p>Returns true if both operands have the same value; otherwise, it returns false.</p>
</td><td><p>[Quantity] == 10</p>
</td></tr><tr><td><p>!=</p>
</td><td><p>Returns true if the operands do not have the same value; otherwise, it returns false.</p>
</td><td><p>[Country] != &#39;France&#39;</p>
</td></tr><tr><td><p>&lt;</p>
</td><td><p>Less than operator. Used to compare expressions.</p>
</td><td><p>[UnitPrice] &lt; 20</p>
</td></tr><tr><td><p>&lt;=</p>
</td><td><p>Less than or equal to operator. Used to compare expressions.</p>
</td><td><p>[UnitPrice] &lt;= 20</p>
</td></tr><tr><td><p>&gt;=</p>
</td><td><p>Greater than or equal to operator. Used to compare expressions.</p>
</td><td><p>[UnitPrice] &gt;= 30</p>
</td></tr><tr><td><p>&gt;</p>
</td><td><p>Greater than operator. Used to compare expressions.</p>
</td><td><p>[UnitPrice] &gt; 30</p>
</td></tr><tr><td><p>In (,,,)</p>
</td><td><p>Tests for the existence of a property in an object.</p>
</td><td><p>[Country] In (&#39;USA&#39;, &#39;UK&#39;, &#39;Italy&#39;)</p>
</td></tr><tr><td><p>Between (,)</p>
</td><td><p>Specifies a range to test. Returns true if a value is greater than or equal to the first operand and less than or equal to the second operand.</p>
</td><td><p>[Quantity] Between (10, 20)</p>
</td></tr><tr><td><p>And </p>
<p>&amp;&amp;</p>
</td><td><p>Performs a logical conjunction on two Boolean expressions.</p>
</td><td><p>[InStock] And ([ExtendedPrice]&gt; 100)</p>
<p>[InStock] &amp;&amp; ([ExtendedPrice]&gt; 100)</p>
</td></tr><tr><td><p>Or</p>
<p>||</p>
</td><td><p>Performs a logical disjunction on two Boolean expressions.</p>
</td><td><p>[Country]==&#39;USA&#39; Or [Country]==&#39;UK&#39;</p>
<p>[Country]==&#39;USA&#39; || [Country]==&#39;UK&#39;</p>
</td></tr><tr><td><p>~</p>
</td><td><p>Performs a bitwise negation on a numeric expression.</p>
</td><td><p>~[Roles] = 251</p>
</td></tr><tr><td><p>Not</p>
<p>!</p>
</td><td><p>Performs a logical negation on a Boolean expression.</p>
</td><td><p>Not [InStock]</p>
<p>![InStock]</p>
</td></tr><tr><td><p>+</p>
</td><td><p>Returns a numeric expression&#39;s value (a unary operator).</p>
</td><td><p>+[Value] = 10</p>
</td></tr><tr><td><p>-</p>
</td><td><p>Returns the negative of a numeric expression&#39;s value (a unary operator).</p>
</td><td><p>-[Value] = 20</p>
</td></tr><tr><td><p>Is Null</p>
</td><td><p>Returns true if an expression is a null reference, the one that does not refer to any object.</p>
</td><td><p>[Region] is null</p>
</td></tr></table>

## Functions (Basic)

### Aggregate Functions

| Function | Description | Example |
|---|---|---|---|
| Avg(Value) | Evaluates the average of the values in the collection. | [Products].Avg([UnitPrice]) |
| Count() | Returns the number of objects in a collection. | [Products].Count() |
| Exists() | Determines whether the object exists in the collection. | [Categories][[CategoryID] == 7].Exists() |
| Max(Value) | Returns the maximum expression value in a collection. | [Products].Max([UnitPrice]) |
| Min(Value) | Returns the minimum expression value in a collection. | [Products].Min([UnitPrice]) |
| Single() | Returns a single object from the collection. | [Accounts].Single() is not null |
| Sum(Value) | Returns the sum of all the expression values in the collection. | [Products].Sum([UnitsInStock]) |

### Date-time Functions

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

### Logical Functions

<table><tr><th><p>Function</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>Iif(Expression1, True_Value1, ..., ExpressionN, True_ValueN, False_Value)</p>
</td><td><p>Returns one of several specified values depending upon the values of logical expressions.</p>
<p>The function can take <em>2N+1</em> arguments (<em>N</em> - the number of specified logical expressions):</p>
<ul>
<li><p>Each odd argument specifies a logical expression;</p>
</li>
<li><p>Each even argument specifies the value that is returned if the previous expression evaluates to <strong>true</strong>; </p>
</li>
<li><p><strong>...</strong></p>
</li>
<li><p>The last argument specifies the value that is returned if the previously evaluated logical expressions yielded <strong>false</strong>.</p>
</li>
</ul>
</td><td><p>Iif(Name = &#39;Bob&#39;, 1, Name = &#39;Dan&#39;, 2, Name = &#39;Sam&#39;, 3, 4)&quot;)</p>
</td></tr><tr><td><p>IsNull(Value)</p>
</td><td><p>Returns True if the specified Value is NULL.</p>
</td><td><p>IsNull([OrderDate])</p>
</td></tr><tr><td><p>IsNull(Value1, Value2)</p>
</td><td><p>Returns Value1 if it is not set to NULL; otherwise, Value2 is returned.</p>
</td><td><p>IsNull([ShipDate], [RequiredDate])</p>
</td></tr><tr><td><p>IsNullOrEmpty(String)</p>
</td><td><p>Returns True if the specified String object is NULL or an empty string; otherwise, False is returned.</p>
</td><td><p>IsNullOrEmpty([ProductName])</p>
</td></tr></table>

### Math Functions

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

### String Functions

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

Below is a list of functions that are used to construct [expression bindings](..\bind-to-data\data-binding-modes.md) and [calculated fields](..\shape-report-data\use-calculated-fields.md):

<table><tr><th><p>Function</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>NewLine()</p>
</td><td><p>Returns the newline string defined for the current environment.</p>
</td><td><p>[CategoryName]+NewLine()+[Description]</p>
<p>Result:</p>
<p><em>Beverages</em></p>
<p><em>Soft drinks, coffees, teas, beers and ales.</em></p>
</td></tr><tr><td><p>FormatString(Format, Value1, ... , ValueN)</p>
</td><td><p>Returns the specified string with formatted field values. See <a class="xref" href="..\shape-report-data\shape-data-data-bindings\format-data.html">Format Data</a> for details.</p>
</td><td><p>FormatString(&#39;{0:$0.00}&#39;, [UnitPrice])</p>
<p>Result: <em>$45.60</em></p>
</td></tr><tr><td><p>Rgb(Red, Green, Blue)</p>
</td><td><p>Returns a string defining a color using the Red, Green, and Blue color channel values.</p>
</td><td><p>Rgb(30,200,150)</p>
<p>Result: <em>&#39;30,200,150&#39;</em></p>
</td></tr><tr><td><p>Argb(Alpha, Red, Green, Blue)</p>
</td><td><p>Returns a string defining a color using the Alpha, Red, Green, and Blue color channel values.</p>
</td><td><p>Argb(1,200, 30, 200)</p>
<p>Result: <em>&#39;1,200,30,200&#39;</em></p>
</td></tr><tr><td><p>Join()</p>
</td><td><p>Concatenates the <a class="xref" href="..\shape-report-data\use-report-parameters\create-multi-value-and-cascading-parameters.html">multi-value report parameter</a>&#39;s values into a string. This function is useful when you <a class="xref" href="..\shape-report-data\use-report-parameters\parameters-overview.html">bind a multi-value parameter to a label</a> to display the parameter&#39;s values in a report.</p>
<p>This function has two overloads:</p>
<ul>
<li>Join(parameter) - concatenates the specified parameter&#39;s values using comma as a separator.</li>
<li>Join(parameter, separator) - concatenates the specified parameter&#39;s values using the specified separator.</li>
</ul>
</td><td><p>Join([Parameters.CategoriesParameter])</p>
<p>Result: <em>Beverages, Condiments</em></p>
<p>Join([Parameters.CategoriesParameter], newline())</p>
<p>Result: </p>
<p><em>Beverages</em></p>
<p><em>Condiments</em></p>
</td></tr></table>

## Functions for Stored Procedure Binding

The following functions are specific for [binding reports to a stored procedure](..\bind-to-data\bind-a-report-to-a-stored-procedure.md):

<table><tr><th><p>Function</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>Join()</p>
</td><td><p>Concatenates the <a class="xref" href="..\shape-report-data\use-report-parameters\create-multi-value-and-cascading-parameters.html">multi-value report parameter</a>&#39;s values into a string. This function can be used when mapping multi-value report parameters to query parameters generated from a stored procedure&#39;s parameters. Refer to the <a class="xref" href="..\shape-report-data\use-report-parameters\use-query-parameters.html">Query Parameters</a> topic for more information.</p>
<p>This function has two overloads:</p>
<ul>
<li>Join(parameter) - concatenates the specified parameter&#39;s values using comma as a separator.</li>
<li>Join(parameter, separator) - concatenates the specified parameter&#39;s values using the specified separator.</li>
</ul>
</td><td><p>Join([Parameters.Parameter1])</p>
</td></tr><tr><td><p>CreateTable(Column1, ..., ColumnN)</p>
</td><td><p>Creates a table from several multi-value parameters&#39; values. This function can be used when mapping multi-value report parameters to the query parameter that is generated from a stored procedure&#39;s <a href="https://docs.microsoft.com/en-us/sql/relational-databases/tables/use-table-valued-parameters-database-engine">User Defined Table Type</a> parameter. Refer to the <a class="xref" href="..\shape-report-data\use-report-parameters\use-query-parameters.html">Query Parameters</a> topic for more information.</p>
</td><td><p>CreateTable([Parameters.Parameter1], ..., [Parameters.ParameterN])</p>
</td></tr></table>

## <a name="summary-expression-editor">Functions for Summary Expression Editor</a>

Use the following functions when [calculating summaries](..\shape-report-data\shape-data-expression-bindings\calculate-a-summary.md) across a report and its groups:

<table><tr><th><p>Function</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>sumAvg(Expression)</p>
</td><td><p>Calculates the average of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumAvg([UnitPrice])</p>
</td></tr><tr><td><p>sumCount(Expression)</p>
</td><td><p>Counts the number of values within the specified summary region (group, page or report). In a simple scenario, you may not pass a parameter.</p>
<p>  When using this function in a <a class="xref" href="..\create-popular-reports\create-a-master-detail-report-use-detail-report-bands.html">master-detail report</a>&#39;s master band and passing a detail&#39;s field as a parameter, it counts the number of records within the detail&#39;s band.</p>
<p>  See also: <a class="xref" href="..\shape-report-data\shape-data-data-bindings\count-the-number-of-records-in-a-report-or-group.html">Counting the Number of Records in a Report or Group</a>, <a class="xref" href="..\shape-report-data\shape-data-data-bindings\count-the-number-of-groups-in-a-report.html">Counting the Number of Groups in a Report</a></p>
</td><td><p>sumCount([UnitPrice])</p>
</td></tr><tr><td><p>sumDAvg(Expression)</p>
</td><td><p>Calculates the average of all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDAvg([UnitPrice])</p>
</td></tr><tr><td><p>sumDCount(Expression)</p>
</td><td><p>Counts the number of <strong>distinct</strong> values within the specified summary region (group, page or report). In a simple scenario, you may not pass a parameter.</p>
</td><td><p>sumDCount([UnitPrice])</p>
</td></tr><tr><td><p>sumDStdDev(Expression)</p>
</td><td><p>Calculates the standard deviation of all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDStdDev([UnitPrice])</p>
</td></tr><tr><td><p>sumDStdDevP(Expression)</p>
</td><td><p>Calculates the standard population deviation of all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDStdDevP([UnitPrice])</p>
</td></tr><tr><td><p>sumDSum(Expression)</p>
</td><td><p>Calculates the total of all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDSum([UnitPrice])</p>
</td></tr><tr><td><p>sumDVar(Expression)</p>
</td><td><p>Calculates the amount of variance for all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDVar([UnitPrice])</p>
</td></tr><tr><td><p>sumDVarP(Expression)</p>
</td><td><p>Calculates the population variance of all the <strong>distinct</strong> values within the specified summary region (group, page or report).</p>
</td><td><p>sumDVarP([UnitPrice])</p>
</td></tr><tr><td><p>sumMax(Expression)</p>
</td><td><p>Calculates the maximum of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumMax([UnitPrice])</p>
</td></tr><tr><td><p>sumMedian(Expression)</p>
</td><td><p>Finds the middle number within a sequence.</p>
<p>  Note that if the total number of elements is odd, this function returns the value of the middle number in a sequence. If the total number of elements is even, this function returns the arithmetical mean of the two middle numbers.</p>
</td><td><p>sumMedian([UnitPrice])</p>
</td></tr><tr><td><p>sumMin(Expression)</p>
</td><td><p>Calculates the minimum of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumMin([UnitPrice])</p>
</td></tr><tr><td><p>sumPercentage(Expression)</p>
</td><td><p>Calculates the percent ratio of the current data row&#39;s value to the total of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumPercentage([UnitPrice])</p>
</td></tr><tr><td><p>sumRecordNumber(Expression)</p>
</td><td><p>Returns the current record number in the specified summary region (group, page or report). This means for instance, if the summary is calculated for a group, then the record number is calculated only within that group, and is reset every time a new group is started.</p>
<p>  In a simple scenario, you may not pass a parameter.</p>
<p>  See also: <a class="xref" href="..\shape-report-data\shape-data-data-bindings\display-row-numbers-in-a-report-group-or-page.html">Displaying Row Numbers in a Report, Group or Page</a></p>
</td><td><p>sumRecordNumber()</p>
</td></tr><tr><td><p>sumRunningSum(Expression)</p>
</td><td><p>Summarizes all the values, which were printed before the current data row, with the current data row&#39;s value.</p>
</td><td><p>sumRunningSum([UnitPrice])</p>
</td></tr><tr><td><p>sumStdDev(Expression)</p>
</td><td><p>Calculates the standard deviation of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumStdDev([UnitPrice])</p>
</td></tr><tr><td><p>sumStdDevP(Expression)</p>
</td><td><p>Calculates the standard population deviation of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumStdDevP([UnitPrice])</p>
</td></tr><tr><td><p>sumSum(Expression)</p>
</td><td><p>Calculates the total of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumSum([UnitsInStock])</p>
</td></tr><tr><td><p>sumVar(Expression)</p>
</td><td><p>Calculates the amount of variance for all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumVar([UnitPrice])</p>
</td></tr><tr><td><p>sumVarP(Expression)</p>
</td><td><p>Calculates the population variance of all the values within the specified summary region (group, page or report).</p>
</td><td><p>sumVarP([UnitPrice])</p>
</td></tr></table>

## Report Items In Expressions

A report's elements are displayed in the Report Designer's Report Explorer. You can access these elements and their properties in expressions. The following example demonstrates how to set a label's BackColor property to the other label's BackColor property value.

*[ReportItems].[xrLabel2].[BackColor]*

> [!Tip]
> **[ReportItems]** is a list that provides access to all report items.

> [!Note]
> You cannot use the ReportItems collection in a [Calculated Field](..\shape-report-data\use-calculated-fields.md)'s expression. 




## Variables

<table><tr><th><p>Variable</p>
</th><th><p>Description</p>
</th><th><p>Example</p>
</th></tr><tr><td><p>DataSource.RowCount</p>
</td><td><p>Returns the total amount of data rows in a data source.</p>
</td><td><p>[DataSource.RowCount] != 0</p>
<p>Result: When using this expression for a control&#39;s Visible property, the control is not displayed if there is no data in the data source.</p>
</td></tr><tr><td><p>DataSource.CurrentRowIndex</p>
</td><td><p>Returns a zero-based index of the current data row in a data source.</p>
</td><td><p>Iif([DataSource.CurrentRowIndex] % 2 = 0, &#39;red&#39;, &#39;green&#39;)</p>
<p>Result: When this expression is used for a table row&#39;s BackColor property, odd rows are colored in red and even rows - in green.</p>
</td></tr></table>

> [!Note]
> These variables are not valid when the report includes a [table or contents](..\add-navigation\add-a-table-of-contents.md).

## Report Parameters

Use the following syntax conventions to utilize [report parameters](..\shape-report-data\use-report-parameters.md) in the [Expression Editor](..\use-expressions.md):

* Insert [report parameters](..\shape-report-data\use-report-parameters.md) using the "Parameters." prefix before their names.

  _[Parameters.parameter1]_
* When referencing [report parameters](..\shape-report-data\use-report-parameters.md) in the [Filter Editor](..\shape-report-data\filter-data\filter-data-at-the-report-level.md) and using [query parameters](..\shape-report-data\use-report-parameters\use-query-parameters.md) in data source queries, type a question mark before the parameters' names. 

  _?parameter1_

## Collection Elements Verification
Use brackets "[]" to check if a collection contains an element that satisfies a condition. The following expression returns _true_ if the Accounts collection contains at least one element that satisfies the _[Amount] == 100_ condition:

_[Accounts][[Amount] == 100]_

The following expression returns _false_ if the Accounts collection is empty:

_[Accounts][]_

Refer to the [](..\shape-report-data\use-calculated-fields\calculate-an-aggregate-function.md) topic to see an example how to use this syntax.

## Parent Relating Operator
Use the parent relating operator ('^' character) to refer to a parent in expressions written in the context of a child. You can apply this operator successively to navigate multiple parent relationships. 

You can use this operator to refer to the currently processed report group. This allows you to calculate aggregates within groups using expressions like the following:

_[][[^.CategoryID] == [CategoryID]].Sum([UnitPrice])_

Refer to the [](..\shape-report-data\use-calculated-fields\calculate-an-aggregate-function.md) topic for details.

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

## Escape Characters
 
Use a backslash (\) as an escape character for characters in expressions. Examples:

- \[
- \\
- \'