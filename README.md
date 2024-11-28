# flutterapp
assignment


SELECT SUBSTRING(
    your_column, 
    CHARINDEX('_', your_column, CHARINDEX('_', your_column, CHARINDEX('_', your_column) + 1) + 1) + 1, 
    CHARINDEX('_', your_column + '_', CHARINDEX('_', your_column, CHARINDEX('_', your_column, CHARINDEX('_', your_column) + 1) + 1) + 1) 
    - CHARINDEX('_', your_column, CHARINDEX('_', your_column, CHARINDEX('_', your_column) + 1) + 1) - 1
) AS word_after_third
FROM your_table;
