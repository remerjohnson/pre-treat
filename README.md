# Pre-Treat

In order to generate linked data sets, your metadata needs to be _very_ clean. Current tools like [OpenRefine](https://openrefine.org/) are the "power tools" for cleaning messy data.  

But often, some cleaning has to be performed on your tabular data before it's even ready for those tools. That's where Pre-Treat comes in.  

Pre-Treat performs simple yet powerful cleaning operations on spreadsheets in a GUI interface with a simple input/output operation. The idea is that catching these data anomalies early isn't just cleaning, but leads into data validation, things that are much harder to do once the data is more mature, or has gone through several transformations.  

## Special Note on Development

This repo has been in stasis since I left the library where these data needs originated.  

If you would like a great GUI-based program that has similar ideas to Pre-Treat (and is much better!), I highly recommend [DataHarmonizer](https://github.com/cidgoh/DataHarmonizer) 

## Features 

### Entire dataset space trimming 

Dirty spreadsheets often have spaces surrounding values, and can be impossible to find. OpenRefine can fix this for CSV sheets, but not Excel. Pre-Treat will trim those spaces for Excel sheets!  

### Entire dataset double space collapsing 

Double spaces within values are also a pain to find in large Excel sheets. Pre-Treat will collapse these into a single space for the entire sheet.  

### Replace value delimiter with pipe characters (Optional)

Excel sheets often have delimiters within "Subject" cells that are problematic, like commas and semicolons. Pre-Treat will look for a `Subject:topic` column, and replace the delimiters with a clean set of pipe `|` characters.  

### Date inference (under development) 

Metadata often needs "structured" dates with "begin date" and "end date" ranges. Pre-Treat will attempt to structure your dates automagically. It analyzes your date column, and adds appropriate Begin Date and End Date columns. If it's a single specific date, it will simply add both.  
