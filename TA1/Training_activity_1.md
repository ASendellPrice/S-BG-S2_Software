# S-BG-S2: Training Activity 1
Ashley Sendell-Price

## Details
Use Linux command line and command line tools to:
- Count the number of lines in a file
- Change the content of a file
- Change a file owner and permissions
- Identify the process taking up the most memory
- Check file system disk space usage

## Count the number of lines in a file
To demonstrate counting the number of lines in a file I have created a list of "green" genes from the R142 gene panel [Growth failure in early childhood (Version 3.96)](https://panelapp.genomicsengland.co.uk/panels/473/). This gene list can be previewed using the `less` command:

![](gifs/preview_genes.gif)

As each line in this file represents a gene, the number of genes can easily be determined by counting the number of lines within the file using the `wc` command. Below I assign the number of lines to the variable "count" which I then use to print the number of lines to the screen using the `echo` command:

![](gifs/count_lines.gif)


## Change the content of a file
To demonstrate changing the contents of a file, below I use the command line text editor `nano` to remove the BRCA2 gene from the list of green genes. The BRCA2 gene is associated with an increased risk of breast and ovarian cancer. In pediatric referrals, this gene might be removed from the green list if a pathogenic variant is known to occur within the child's family. This precaution is taken to avoid revealing the child's BRCA2 status during childhood.

![](gifs/change_file_content_nano.gif)

An alternative method of making this change to the file would be to use the sed command to find and replace the text as shown in the screencast below. I also make use of the pattern matching command grep to show that BRCA2 has been removed from the list of green genes.

![](gifs/change_file_content_sed.gif)


## Change a file owner and permissions
## Identify the process taking up the most memory
## Check file system disk space usage





 