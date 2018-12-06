---
title: Summarization
author: Natalia Kazakova
legacyId: 16529
---
# Summarization
To obtain numeric values that should be displayed within a dashboard item, Dashboard calculates a summary function against the specified measure.

![Charts_DataBinding_Values](../../../images/img18722.png)

This topic describes how to specify which summary function should be calculated against a particular measure.

The following sections are available.
* [Summary Function Types](#summaryfunctiontypes)
* [Changing Summary Type](#changingsummarytype)

## <a name="summaryfunctiontypes"/>Summary Function Types
The following summary functions are available.
* **Count** - The number of values (excluding **Null** and **DBNull** values).
	
	This is the only summary type that can be calculated against non-numeric data.
* **Count Distinct** - The number of distinct values.
* **Sum** - The sum of the values.
	
	![func_sum](../../../images/img4460.png)
* **Min** - The smallest value.
* **Max** - The largest value.
* **Average** - The average of the values.
	
	![func_average](../../../images/img4457.png)
* **StdDev** - An estimate of the standard deviation of a population, where the sample is a subset of the entire population.
	
	![func_stddev](../../../images/img4458.png)
* **StdDevP** - The standard deviation of a population, where the population is the entire data to be summarized.
	
	![func_stddevp](../../../images/img4459.png)
* **Var** - An estimate of the variance of a population, where the sample is a subset of the entire population.
	
	![func_var](../../../images/img4461.png)
* **VarP** - The variance of a population, where the population is the entire data to be summarized.
	
	![func_varp](../../../images/img4462.png)
* **Median** - The _median_ of the values (excluding **Null** and **DBNull** values).  A _median_ is the number separating the higher half of a value range from the lower half.

## <a name="changingsummarytype"/>Changing Summary Type
By default, Dashboard calculates **Sum** for numeric measures and **Count** for measures that contain another type of data.

You can change the summary function type for numeric measures. To do this in the Designer, invoke the data item menu and select the desired summary type. Less common summary types are organized in the **More** submenu.

![DataShaping_SummaryTypeMenu](../../../images/img19326.png)