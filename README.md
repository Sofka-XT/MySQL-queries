MySQL-queries
=============

I have listed some queries to automate processes such as importing entire data (tables and columns) from a spreadsheet onto MySQL database.

I have a lot of data in Excel sheets. I want the same data to be inserted into my databases, however I do not want to manually perform the entire task. So I used the query (mentioned in this file) to import them using the command line prompt. I agree it is a lot easier on some GUI based applications, however in this process you get greater control over your data and processes.

Things I want to point out:

1.It is important to have the excel sheet data converted into a .csv format. I built this query on an OS X system, so I used '\r' as the line termination symbol. Windows users can directly use '/n'.

2. No need to have the headings in the Excel sheet (you can remove them). It is not so difficult to add them manually in the SQL table itself. 
I have defined the table like this:
  CREATE TABLE january (
    -> Index VARCHAR(30) NOT NULL,
    -> Document VARCHAR(30) NOT NULL,
    -> Words VARCHAR(10) NOT NULL,
    -> Delivered VARCHAR(10) NOT NULL,
    -> Cost VARCHAR(10) NOT NULL);

3. /Users/srayan/Desktop/January.csv in the SQL query is the location of the .csv file. For windows users it can be 'C:/Users/MisterX/files/january.csv'

All in all I hope it works for you.

Srayan Guhathakurta.
www.srayan.tk
