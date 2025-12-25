---
title: Summarization
author: Natalia Kazakova
legacyId: 117703
---
# Summarization
To obtain numeric values that should be displayed within a dashboard item, Dashboard calculates a summary function against the specified measure.

## <a name="summaryfunctiontypes"/>Summary Function Types
The following summary functions are available.
* **Count** - The number of values (excluding **Null** and **DBNull** values).
	
	This is the only summary type that can be calculated against non-numeric data.
* **Count Distinct** - The number of distinct values.
* **Sum** - The sum of the values.
	
	![func_sum](images/img4460.png)
* **Min** - The smallest value.
* **Max** - The largest value.
* **Average** - The average of the values.
	
	![func_average](images/img4457.png)
* **StdDev** - An estimate of the standard deviation of a population, where the sample is a subset of the entire population.
	
	![func_stddev](images/img4458.png)
* **StdDevP** - The standard deviation of a population, where the population is the entire data to be summarized.
	
	![func_stddevp](images/img4459.png)
* **Var** - An estimate of the variance of a population, where the sample is a subset of the entire population.
	
	![func_var](images/img4461.png)
* **VarP** - The variance of a population, where the population is the entire data to be summarized.
	
	![func_varp](images/img4462.png)

## Changing Summary Type
By default, Dashboard calculates **Sum** for numeric measures and **Count** for measures that contain another type of data.

You can change the summary function type for numeric measures. To do this, invoke the dashboard item [Bindings](../ui-elements/dashboard-item-menu.md) menu and select the required data item. In the drop-down **Summary Type** list, select the desired summary type.

![wdd-change-summary-type](images/img124599.png)