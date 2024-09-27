1. mkdir homework3_1  #create a folder with name homework3_1
	[chernym@login509-02-l ~]$  mkdir homework3_1
	[chernym@login509-02-l ~]$
2. cd /home/chernym/homework3_1/ #go to that dirctory
	[chernym@login509-02-l ~]$ cd /home/chernym/homework3_1/
	[chernym@login509-02-l homework3_1]$
3. git clone https://github.com/chernymilena/bioe_homework # extracts the files from github
	[chernym@login509-02-l homework3_1]$ git clone https://github.com/chernymilena/bioe_homework
	Cloning into 'bioe_homework'...
	remote: Enumerating objects: 17, done.
	remote: Counting objects: 100% (17/17), done.
	remote: Compressing objects: 100% (14/14), done.
	remote: Total 17 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
	Receiving objects: 100% (17/17), 16.00 MiB | 14.84 MiB/s, done.
	Resolving deltas: 100% (2/2), done.
	[chernym@login509-02-l homework3_1]$
4. ls bioe_homework # check what is the folder
	[chernym@login509-02-l homework3_1]$ ls bioe_homework
	ncbi_dataset_1.tsv  ncbi_dataset.zip  Readme.txt
5. cd /home/chernym/homework3_1/bioe_homework/ # change to that directory
	[chernym@login509-02-l bioe_homework]$ cd /home/chernym/homework3_1/bioe_homework/
	[chernym@login509-02-l bioe_homework]$
6. unzip ncbi_dataset.zip 	
	[chernym@login509-02-l bioe_homework]$ unzip ncbi_dataset.zip
	Archive:  ncbi_dataset.zip
		inflating: README.md
		inflating: ncbi_dataset/data/data_summary.tsv
		inflating: ncbi_dataset/data/assembly_data_report.jsonl
		inflating: ncbi_dataset/data/GCA_000008525.1/GCA_000008525.1_ASM852v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008605.1/GCA_000008605.1_ASM860v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008625.1/GCA_000008625.1_ASM862v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008745.1/GCA_000008745.1_ASM874v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000027305.1/GCA_000027305.1_ASM2730v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008525.1/GCF_000008525.1_ASM852v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008605.1/GCF_000008605.1_ASM860v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008625.1/GCF_000008625.1_ASM862v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008745.1/GCF_000008745.1_ASM874v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000027305.1/GCF_000027305.1_ASM2730v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000006745.1/GCA_000006745.1_ASM674v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008545.1/GCA_000008545.1_ASM854v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008565.1/GCA_000008565.1_ASM856v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008725.1/GCA_000008725.1_ASM872v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000008785.1/GCA_000008785.1_ASM878v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000006745.1/GCF_000006745.1_ASM674v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008545.1/GCF_000008545.1_ASM854v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008565.1/GCF_000008565.1_ASM856v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008725.1/GCF_000008725.1_ASM872v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000008785.1/GCF_000008785.1_ASM878v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000006825.1/GCA_000006825.1_ASM682v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000006865.1/GCA_000006865.1_ASM686v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000007125.1/GCA_000007125.1_ASM712v1_genomic.fna
		inflating: ncbi_dataset/data/GCA_000091085.2/GCA_000091085.2_ASM9108v2_genomic.fna
		inflating: ncbi_dataset/data/GCF_000006825.1/GCF_000006825.1_ASM682v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000006865.1/GCF_000006865.1_ASM686v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000007125.1/GCF_000007125.1_ASM712v1_genomic.fna
		inflating: ncbi_dataset/data/GCF_000091085.2/GCF_000091085.2_ASM9108v2_genomic.fna
		inflating: ncbi_dataset/data/dataset_catalog.json
		inflating: md5sum.txt
7. cut -f 2 ncbi_dataset_1.tsv | sort -n | tail -n  +2 |  head -n 1 # extract 2nd column, then sort by length, then remove the first line, then take the first line, it gives the smallest size
	[chernym@login509-02-l bioe_homework]$ cut -f 2 ncbi_dataset_1.tsv | sort -n | tail -n  +2 |  head -n 1
	1042519
8.  cut -f 2 ncbi_dataset_1.tsv | sort -n | tail -n 1 # extract 2nd column, then sort by length then take the last line, gives the largest size
	[chernym@login509-02-l bioe_homework]$ cut -f 2 ncbi_dataset_1.tsv | sort -n | tail -n 1
	4033464
9. cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c' # show the all names which satysfies the task
	[chernym@login509-02-l bioe_homework]$ cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c'
	Chlamydia trachomatis D/UW-3/CX
	Chlamydia trachomatis D/UW-3/CX
	Helicobacter pylori J99
	Helicobacter pylori J99
	Pasteurella multocida subsp. multocida str. Pm70
	Pasteurella multocida subsp. multocida str. Pm70
	Chlamydia pneumoniae CWL029
	Chlamydia pneumoniae CWL029
	Helicobacter pylori 26695
	Helicobacter pylori 26695
10. cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c' | wc -l # count the number of lines which satysfies the task
	[chernym@login509-02-l bioe_homework]$ cut -f 1 ncbi_dataset_1.tsv | tail -n +2 | grep -v "coccus" | grep -i 'c.*c' | wc -l
	10
11. cd /home/chernym/homework3_1/bioe_homework/ncbi_dataset/ #change the directory to the folder with files
	[chernym@login509-02-l ncbi_dataset]$ cd /home/chernym/homework3_1/bioe_homework/ncbi_dataset/
	[chernym@login509-02-l ncbi_dataset]$
12. mkdir data1 # create a folder with name data1
13. cp /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data/*/*.fna /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data1/ #copy all fna-files to one directory
	[chernym@login509-02-l ncbi_dataset]$ cp /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data/*/*.fna /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data1/
	[chernym@login509-02-l ncbi_dataset]$
14. cd /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data1/
	[chernym@login509-02-l ncbi_dataset]$ cd /home/chernym/homework3_1/bioe_homework/ncbi_dataset/data1/
	[chernym@login509-02-l data1]$
15. find  -size +3M  #find all files larger than 3 Mb 
	[chernym@login509-02-l data1]$  find  -size +3M
	./GCA_000006745.1_ASM674v1_genomic.fna
	./GCA_000007125.1_ASM712v1_genomic.fna
	./GCA_000008565.1_ASM856v1_genomic.fna
	./GCF_000006745.1_ASM674v1_genomic.fna
	./GCF_000007125.1_ASM712v1_genomic.fna
	./GCF_000008565.1_ASM856v1_genomic.fna
16. find  -size +3M | wc -l #count the number of lines
	[chernym@login509-02-l data1]$ find  -size +3M | wc -l
	6
