---
title: convert excel spreadsheet to markdown table
module: misc
types: [tutorial,] 
---



## Introduction


Often you are working in excel and want to output to a markdown table.

1. In excel, add a row under the top row.  fill each element with a dash character, ```-```.
1. To the right of the table, add a new formula to concatenate each column of that row together, separated by a vertical line character, ```|```.  For the first row composed of three columns, it should look like this:
  
    ```
    =A1&"|"&B1&"|"&C1
    ```

    [![](../../figures/excel-to-markdown.png){width="50%"}](../../figures/excel-to-markdown.png)

1. Fill the rest of that column with the same equation either by copying and pasting or by using the "fill down" keystroke (ctrl+d).
1. Copy the contents of that column into markdown.  

It should look like this:

```
Column 1|Column 2|Column 3
-|-|-
Value 11|Value 12|Value 13
Value 21|Value 22|Value 23
Value 31|Value 32|Value 33
```

And will compile into this:

Column 1|Column 2|Column 3
-|-|-
Value 11|Value 12|Value 13
Value 21|Value 22|Value 23
Value 31|Value 32|Value 33

## Template File

[excel template used in this example](../../assets/excel-to-markdown.xlsx)

## External Resources

* [Github-flavored Markdown Spec](https://github.github.com/gfm/)
* [Mastering Markdown Guide](https://guides.github.com/features/mastering-markdown/)
* <https://docs.github.com/en/github/writing-on-github/organizing-information-with-tables>