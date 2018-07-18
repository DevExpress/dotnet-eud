|Constant|Description|Example|
|--- |--- |--- |
|String constants|Wrap string constants in apostrophes.
If a string contains an apostrophe, double the apostrophe.|[Country] == 'France'
[Name] == 'O''Neil'|
|Date-time constants|Wrap date-time constants in '#'.|[OrderDate] >= #2018-03-22 13:18:51.94944#|
|True|Represents the Boolean True value.|[InStock] == True|
|False|Represents the Boolean False value.|[InStock] == False|
|Enumeration|Specify an enumeration value using its underlying integer value.|[Status] == 1 <br>
Note that you cannot specify an enumeration value using its qualified name. The following criteria is incorrect:
[Status] = Status.InProgress|
|Guid|Wrap a Guid constant in curly braces. Use Guid constants in a relational operation with equality or inequality operators only.|[OrderID] == {513724e5-17b7-4ec6-abc4-0eae12c72c1f}|
|Numeric|Specify different numeric constant types in a string form using suffixes:<br>

Int32 (int) - 1<br>
Int16 (short) - 1s<br>
Byte (byte) - 1b<br>
Double (double) - 1.0<br>
Single (float) - 1.0f<br>
Decimal (decimal) - 1.0m|[Price] == 25.0m|
|?|Represents a null reference that does not refer to any object.<br>
We recommend using the IsNull unary operator (for example, "[Region] is null") or the IsNull logical function (for example, "IsNull([Region])") instead.|[Region] != ?|
