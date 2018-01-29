# assignment-1
Assignment 1 due January 29
## I. Get the data files
Download the following data files from the internet using the curl command: http://eaton-lab.org/pdsb/test.fastq.gz and http://eaton-lab.org/pdsb/iris-data-dirty.csv. Use the less or zless commands to look at the files. Then use the head command to print the first 5 lines from each file as output.

Answer to I and [link](www.google.com) for any online resources.

```
code
```
```
answer
```

## II. Clean the data
Use grep, uniq, sed. Check that all of the species names are spelled correctly in the file iris-data-dirty.csv. Also check for missing values stored as NA. Create a new file where mispelled names are replaced with the correct values, and lines with NA are excluded, and save it as iris-data-clean.csv. Use cut, sort and uniq to list the number of data values there are for each species in the new cleaned data file.

Answer to II and [link](www.google.com) for any online resources.

```
code
```
```
answer
```
## III. Summarize sequence data file
Find how many lines in the data file test.fastq.gz start with "TGCAG" and end with "GAG"

Answer to III and [link](www.google.com) for any online resources.

```
code
```

```
answer
```

## IV. Summarize sequence data file
Write a for-loop to separate the reads from the file test.fastq.gz based on the taxon name in the label, and write the reads to separately named files in the new directory called sorted_reads/. The answer to this question will require more than a single line. See the lecture materials about using variables in for-loops. This will also be tricky because each read in the data file spans four lines (this is a standard genetic sequence file format), so for each read that you correctly identify you must grab the line with the sequence data below it, as well as the repeat label after that, and the quality information line after that. For a hint, see additional options for the grep command that can be used to select multiple lines.

Answer to IV and [link](www.google.com) for any online resources.

```
code
```
```
answer
```
