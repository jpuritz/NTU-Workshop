#Are you a Linux Master?

Answer these challenges with one line of code:

Question 1-  Put your answers in a text file with your Group’s name on it in the ~/Answers directory
I have put a text file, named file, in the directory “sneaky” that’s within the directory “documents” that’s within the home directory.  Tell me what the contents of the file is.

Answer:
`cat ~/documents/sneaky/file`

The contents were:
`Game of Thrones`

Question 2- Print the first 5 lines of the third column of out.idepth

Answer:	

`cut -f3 ~/COURSE_DATA/out.idepth | head -5`
 
Question 3- Print only the 19th line of the second column of out.idepth

Answer:	
`head -19 ~/COURSE_DATA/out.idepth | cut -f2 | tail -1`

Question 4- Print how many individuals have a MEAN_DEPTH greater than 20.1

Answer:	
`awk '$3 > 20.1' ~/COURSE_DATA/out.idepth | awk '!/MEAN/' | wc -l`

Question 5- Print how many individuals have a MEAN_DEPTH greater than 20.1 but less than 20.4

Answer:	
`awk '$3 > 20.1' ~/COURSE_DATA/out.idepth | awk '$3 < 20.4' | awk '!/MEAN/' | wc -l`

Question 6- Print the average MEAN_DEPTH 

Answer:	
`awk '{sum=sum+$3} END {print sum/NR}' ~/COURSE_DATA/out.idepth`
