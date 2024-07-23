# S-BG-S2: Training Activity 1
**Author:** Ashley Sendell-Price

### Count the number of lines in a file
To demonstrate counting the number of lines in a file I have created a list of "green" genes from the R142 gene panel [Growth failure in early childhood (Version 3.96)](https://panelapp.genomicsengland.co.uk/panels/473/). This gene list can be previewed using the `less` command:

![preview file](gifs/preview_genes.gif)

As each line in this file represents a gene, the number of genes can easily be determined by counting the number of lines within the file using the `wc` command. Below I assign the number of lines to the variable "count" which I then use to print the number of lines to the screen using the `echo` command:

![count lines](gifs/count_lines.gif)

### Change the content of a file
To demonstrate changing the contents of a file, below I use the command line text editor `nano` to remove the BRCA2 gene from the list of green genes. The BRCA2 gene is associated with an increased risk of breast and ovarian cancer. In pediatric referrals, this gene might be removed from the green list if a pathogenic variant is known to occur within the child's family. This precaution is taken to avoid revealing the child's BRCA2 status during childhood.

![change file contents](gifs/change_file_content_nano.gif)

An alternative method of making this change to the file would be to use the `sed` command to find and replace the text as shown in the screencast below. I also make use of the pattern matching command `grep` to show that BRCA2 has been removed from the list of green genes.

![pattern matching and replacing](gifs/change_file_content_sed.gif)

### Change a file owner and permissions
File permissions refers to whether a file can be read, written (changed), or executed by the file owner, group, or other users. In some instances it may be appropriate to limit file permissions such as making a file read only. Making a file read only helps to ensure that the file is not accidently deleted, modified, or overwritten. Below I use the `chmod` command to make the list of green genes read only. I also make use of the `ls -l` command to confirm that file permisions have been changed. The file permission notation `-r--r--r--` indicates that the file owner, group, and other user permissions are all set to read only. If the file permissions are set to allow the owner to read, write, and execute, while the group and others can only read, the notation would be `-rwxr--r--`.

![change file permissions](gifs/chmod.gif)

Below I use the `chown` command to change the file owner to a user called 'awmgs'. Note that changing the owner requires superuser (root) privileges using `sudo`.

![change file owner](gifs/chown.gif)


### Identify the process taking up the most memory
To identify the process consuming the most memory, below I use the `top` command with the `-o` flag set to sort by memory usage (%MEM). This revealed that process 2036 (gnome-shell) was using 1.2% of the available physical memory (RSS).

![top memory](gifs/top_memory.gif)


### Check file system dis`k space usage
The disk space usage of the file system can be checked, use the `df` command. The -H option provides human-readable output.

![disk usage](gifs/disk_usage.gif)

## Reflection
Having worked with the command line for several years, I am already familiar with many of the commands used in this training activity. However, this exercise provided an excellent opportunity to refresh and reinforce my knowledge of fundamental commands such as `ls`, `wc`, `less`, `nano`, `sed`, and `grep`. The activity also deepened my understanding of file permissions and ownership, and introduced me to important system monitoring commands like `top` and `df`. These tools are essential for managing and tracking system resources effectively.

I performed this activity on my development laptop, which allowed me to practice these commands in a controlled environment. Moving forward, as I transition to using shared compute resources in my role as a trainee clinical bioinformatician, I will need to ensure that I manage these resources efficiently and responsibly. To ensure I am well-prepared for this, my primary action plan is to complete additional in-house training that focuses on the specific requirements and best practices for using these shared systems effectively. This training will equip me with the necessary skills to handle shared resources in a professional and responsible manner.

## Action Plan
- Complete in-house training on shared compute system "WREN"
- Review best practices for managing shared compute resources
- Apply knowledge from training to daily tasks

