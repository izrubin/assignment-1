# assignment-1
Assignment 1 due January 29

## I. Get the data files
Download the following data files from the internet using the curl command: http://eaton-lab.org/pdsb/test.fastq.gz and http://eaton-lab.org/pdsb/iris-data-dirty.csv. Use the less or zless commands to look at the files. Then use the head command to print the first 5 lines from each file as output.

I used the [first class lecture](https://github.com/programming-for-bio/1-Shell-Basics/blob/master/1-PDSB-lecture.pdf) as a general resource and this [stackoverflow thread](https://stackoverflow.com/questions/15747912/how-do-i-use-head-and-tail-to-print-specific-lines-of-a-file) as a resource for how to use the head command.

For the first file:

```
>curl http://eaton-lab.org/pdsb/test.fastq.gz
>zless test.fastq.gz
>gunzip test.fastq.gz
>head -5 test.fastq
```

```
@29154_superba.1 GRC13_0027_FC:4:1:12560:1179 length=74
TGCAGGAAGGAGATTTTCGNACGTAGTGNNNNNNNNNNNNNNGCCNTGGATNNANNNGTGTGCGTGAAGAANAN
+29154_superba.1 GRC13_0027_FC:4:1:12560:1179 length=74
IIIIIIIGIIIIIIFFFFF#EEFE<?################################################
@29154_superba.2 GRC13_0027_FC:4:1:15976:1183 length=74
```

For the second file, I would get the error message that no such file exists when I would try to run zless after the curl command. Seeing in the [gitter chatroom](https://gitter.im/programming-for-bio/Lobby) that another student had a similar problem, I tried using wget but received an error. To work around this issue for now, I downloaded the file through my browser, checked with ls -lt that the file had been downloaded, and proceeded with the rest of the question.

```
>curl http://eaton-lab.org/pdsb/iris-data-dirty.csv
>ls -lt
>less iris-data-dirty.csv
>head -n 5 iris-data-dirty.csv
```

```
5.1,3.5,1.4,0.2,Iris-setosa
4.9,3.0,1.4,0.2,Iris-setosa
4.7,3.2,1.3,0.2,Iris-setosa
4.6,3.1,1.5,0.2,Iris-setosa
5.0,3.6,1.4,0.2,Iris-setosa
```

## II. Clean the data
Use grep, uniq, sed. Check that all of the species names are spelled correctly in the file iris-data-dirty.csv. Also check for missing values stored as NA. Create a new file where mispelled names are replaced with the correct values, and lines with NA are excluded, and save it as iris-data-clean.csv. Use cut, sort and uniq to list the number of data values there are for each species in the new cleaned data file.

I referenced [The Linux Juggernaut](https://www.linuxnix.com/sed-delete-a-matched-line-from-a-file/) for how to delete lines containing NA. I am having trouble with the last part of this question, so I going to move on and come back to it later.

```
>cat iris-data-dirty.csv
>cp iris-data-dirty.csv iris-data-clean.csv
>sed -i 's/versicolour/versicolor/g' iris-data-clean.csv
>sed -i 's/setsa/setosa/g' iris-data-clean.csv
>cat iris-data-clean.csv
>grep "..NA.." iris-data-clean.csv
>sed -i '/NA/d' iris-data-clean.csv
>cat iris.data.clean.csv
```

```
answer
```

## III. Summarize sequence data file
Find how many lines in the data file test.fastq.gz start with "TGCAG" and end with "GAG"

I already unzipped the file test.fastq.gz, so here I am using the unzipped file test.fastq. I learned from Vijay Ramesh's message in the [gitter chatroom](https://gitter.im/programming-for-bio/Lobby) that "a . signifies the end of one set of characters and a * signifies the start of another and you need a $ after to show that it is ending with those."

```
>cat test.fastq | grep -c '^TGCAG.*GAG$'
```

```
44
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
