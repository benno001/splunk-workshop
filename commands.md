# Splunk command cheat sheet

# Comparison operators

# Aggregation
|command|description|
|---|---|
| stats ***aggregation_operator*** by ***field1,field2*** | Aggregate over ***field1*** and ***field2***. Generates rows for ***field2*** values |
| chart ***aggregation_operator*** by ***field1,field2*** | Aggregate over ***field1*** and ***field2***. Generates columns for ***field2*** values |
| timechart ***aggregation_operator*** by ***field*** span=***time_span*** | Aggregate by one or multiple fields in buckets with a size of 'span' (e.g. 5m)


# Aggregation operators
Check out: http://docs.splunk.com/Documentation/Splunk/7.1.2/SearchReference/CommonStatsFunctions

Some useful aggregation operators (not an exhaustive list):

|operator|description|
|---|---|
|avg ***field***|Returns the average of the values in the field ***field***.|
|count ***field***| 	Returns the number of occurrences where the field that you specify contains any value (is not empty. You can also count the occurrences of a specific value in the field by using the eval command with the count function. For example: count eval(field_name="value"). |
|distinct_count ***field***| 	Returns the count of distinct values in the field ***field***. |
|max ***field***|Returns the maximum value of the field ***field***. If the values of ***field*** are non-numeric, the maximum value is found using lexicographical ordering. This function processes field values as numbers if possible, otherwise processes field values as strings. |
|mean ***field***|Returns the arithmetic mean of the field ***field***. |
|median ***field***|Returns the middle-most value of the field ***field***. |
|min ***field***|Returns the minimum value of the field ***field***. If the values of ***field*** are non-numeric, the minimum value is found using lexicographical ordering. |
|mode ***field***|Returns the most frequent value of the field ***field***. |
|range ***field***| 	Returns the difference between the maximum and minimum values of the field ***field*** ONLY IF the values of ***field*** are numeric. |
|stdev ***field***|Returns the sample standard deviation of the field ***field***. |
|sum ***field***|Returns the sum of the values of the field ***field***. |
|var ***field***|Returns the sample variance of the field ***field***. |
