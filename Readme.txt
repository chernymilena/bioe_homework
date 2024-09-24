1. mkdir homework3 
2. cd /home/chernym/homework3/
3. Download from GitHub with  git clone https://github.com/chernymilena/bioe_homework # extracts the files from github
4. ls bioe_homework
5. cd /home/chernym/homework3/bioe_homework/
6. unzip ncbi_dataset.zip
7. cut -f 2 ncbi_dataset_1.tsv | sort -n | head -n 2 # extract 2nd column, then sort by length then take first two lines, gives the smallest size
8.  cut -f 2 ncbi_dataset_1.tsv | sort -n | tail -n 1 # extract 2nd column, then sort by length then take first two lines, gives the largest size
9. cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c' # show the all names which satysfies the task
10. cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c' | wc -l # count the number of lines which satysfies the task
11. cd /home/chernym/homework3/bioe_homework/ncbi_dataset/
12. mkdir data1
13. cp /home/chernym/homework3/bioe_homework/ncbi_dataset/data/*/*.fna /home/chernym/homework3/bioe_homework/ncbi_dataset/data1/ #move all files to one directory
14. cd /home/chernym/homework3/bioe_homework/ncbi_dataset/data1/
15. find  -size +3M  #find all files larger than 3 Mb 
16. find  -size +3M | wc -l #count the number of lines


