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
<p>Note that you cannot specify an enumeration value using its qualified name. The following criteria <strong>is incorrect</strong>:</p>
<p>[Status] = Status.InProgress</p>
<p>For enumerations registered using static  class methods, the corresponding criteria values can be serialized in the following way.</p>
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