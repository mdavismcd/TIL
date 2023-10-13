# Split Cell Text in Excel

I was creating a spreadsheet for MARC21 fields to import into Alma (Library Services Platform) and it required both the MARC21 element together with its subfield and separate, e.g.,
|650$a|650|a|
|---|---|---|

I learned about the `TEXTSPLIT` function. I did this for all rows with `=TEXTSPLIT(B7, "$")` which split the field from the subfield. It was a simple solution for a potentially time suck.
