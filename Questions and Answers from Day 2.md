#Are you a Linux Master?

Answer these challenges with one line of code:

1.  Put your answers in a text file with your Group’s name on it in the ~/Answers directory
I have put a text file, named file, in the directory “sneaky” that’s within the directory “documents” that’s within the home directory.  
Tell me what the contents of the file is

Answer:
```bash
cat ~/documents/sneaky/file
```

The contents were:
`Game of Thrones`


Print the first 5 lines of the third column of out.idepth

Answer:	cut -f3 out.idepth | head -5 
 
Print only the 19th line of the second column of out.idepth

	head -19 ~/COURSE_DATA/out.idepth | cut -f2 | tail -1


Print how many individuals have a MEAN_DEPTH greater than 20.1

	awk '$3 > 20.1' ~/COURSE_DATA/out.idepth | awk '!/MEAN/' | wc -l

Print how many individuals have a MEAN_DEPTH greater than 20.1 but less than 20.4

	awk '$3 > 20.1' ~/COURSE_DATA/out.idepth | awk '$3 < 20.4' | awk '!/MEAN/' | wc -l

Print the average MEAN_DEPTH 

	awk '{sum=sum+$3} END {print sum/NR}' ~/COURSE_DATA/out.idepth
