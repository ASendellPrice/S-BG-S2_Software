# S-BG-S2: Training Activity 1

## Details
Use Linux command line and command line tools to:
- Count the number of lines in a file
- Change the content of a file
- Change a file owner and permissions
- Identify the process taking up the most memory
- Check file system disk space usage

## Count the number of lines in a file
To demonstrate counting the number of lines in a file I will create and manipulate a gene "blacklist" - a text file containing a list of genes to be excluded from an analysis.

First let's create a blacklist containing three genes (MEN1, BRCA1, and MLH1):

```
echo -e "MEN1\nBRCA1\nMLH1" > gene_blacklist.txt
```

Now let's count the number of lines using the wc command:
```
count=$(cat gene_blacklist.txt | wc -l)
echo "The black list contains" $count "genes"
```



 