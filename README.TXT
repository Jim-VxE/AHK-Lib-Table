AutoHotkey Version:    1.0.48.05
Language:              English
Encoding:              ANSI
Created On:            2010/11/15
Author:                [VxE]
Lib Version:           0.27
Available @:           http://www.autohotkey.com/forum/viewtopic.php?t=66290

These functions require a specific table format to function properly. A table must use a single
newline character to separate table rows from each other and from the table header. Each table
row must contain exactly the same number of tab characters as the table header. Any table that
does not conform to these restrictions is unlikely to work correctly with these functions.

Referencing Conventions:

When referencing columns or cells, functions in this library use the name of the column of
interest. To override this behavior and force the functions to reference columns or cells by
their ordinal position ( 1 = the first / leftmost ), precede the parameter's value with a
single tab character. Similarly, when referencing rows, functions in this library use the
contents of the first column of the row. To override this and use the row's ordinal position
instead ( 1 = the row just after the header ), precede the parameter's value with a single tab.
All comparisons are string-based* so be careful about using numeric row identifiers.
(*) NOTE: the following functions will perform non-string comparisons if comparing non-string
data: Table_GetRowIndex, Table_Between

Function List:

Table_Aggregate    - Returns table metadata, typicaly derived from a single table column.
Table_Append       - Appends rows, columns, or both to a table. Also manipulates table columns.
Table_Between      - A simple QUERY. Removes table rows that don't satisfy an inequality.
Table_ColToList    - Extracts a single column from the table in the form of a delimited list.
Table_Decode       - Replaces character entities for tabs and newlines with the actual characters.
Table_Deintersect  - Returns the input table with rows that match the criteria removed.
Table_Encode       - Replaces tabs and newlines with character entities (similar to html entities).
Table_FromCSV      - Converts a CSV table to a 9/10 table (literal tabs and newlines are encoded).
Table_FromHTML     - Converts an HTML table into a 9/10 table
Table_FromINI      - Converts the text of an INI file into a 2-column table (Section/Key,Value).
Table_FromListview - Returns a table with the contents of the default gui's active listview.
Table_FromLvHwnd   - Returns a table with the contents of the listview and its header.
Table_FromXMLNode  - Converts an XML node array into a 9/10 table (not a lossless conversion).
Table_FormatTime   - Converts the values in the indicated column using the FormatTime command.
Table_GetCell      - Returns the value of one cell in the table.
Table_GetColName   - Returns the name of the table column at the given position.
Table_GetRowIndex  - Returns a row's ordinal position in the table.
Table_Header       - Returns the table's header. (The counterpart, 'Table_Decapitate', was removed)
Table_Intersect    - Returns the input table with rows that don't match the criteria removed.
Table_Invert       - Inverts the table so that the first column becomes the new header.
Table_Join         - Adds columns from one table to another, arranging rows to match.
Table_Len          - Returns the number of rows in the table.
Table_RemCols      - Removes table columns, either by name or index.
Table_RemRows      - Removes table rows, either by id or by index.
Table_Reverse      - Reverses the row order of the table.
Table_RotateL      - Rotates a table 90 degrees to the left.
Table_SetCell      - Replaces the contents of one cell in the table and returns the modified table.
Table_SpacePad     - Converts a 9/10 table into a space-padded table.
Table_Sort         - Sorts the table based on the contents of one column and some user options.
Table_SubTable     - Removes some rows from the table.
Table_ToCSV        - Converts a table to CSV format. Tab and newline character entities are decoded.
Table_ToListview   - Modifies the current listview using the given table.
Table_ToLvHWND     - Modifies a listview using the given table.
Table_Transpose    - Flips a table along its main diagonal.
Table_Update       - Updates certain cells in a table using data from another table.
Table_UpdateAppend - Updates a table, then appends rows that didn't have a match in the table.
Table_Width        - Returns the number of columns in the table.