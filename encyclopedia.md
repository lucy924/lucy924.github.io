# My Coding and Commandline Encyclopedia
- [My Coding and Commandline Encyclopedia](#my-coding-and-commandline-encyclopedia)
  - [Intro](#intro)
  - [Adding to PATH](#adding-to-path)
  - [Github blog issues:](#github-blog-issues)
  - [Count how many files in a folder:](#count-how-many-files-in-a-folder)
- [Data Science](#data-science)
  - [R](#r)

## Intro  
This is somewhere to keep all the little tricks and explanations I learn about coding from a newbie's perspective.  
I am starting this several years after I began coding, however I think this will help me explain things better while still remembering what it's like to be completely new at it.  
**NOTE:** This is written from a Linux/MacOS perspective unless otherwise stated.
___
## Adding to PATH
This is necessary when you want to run a program on the commandline without using the full path.
This tells the computer where to look for a program. You will likely come across this when installing and using new programs for the first time.    

You can call/run a program by giving it the full path:
> e.g. `/Users/lucy/programs/bowtie`  

or by adding this to PATH:
> `export PATH=/Users/lucy/programs/bowtie:$PATH`  

and just calling:
> `bowtie`
Note that this command adds to PATH temporarily.

To add it permanently, try this
`echo 'export PATH="$PATH:/Users/lucy/programs/bowtie"' >> ~/.bash_profile`

To see what's already in your path, `echo $PATH`
Many programs that use other programs also require you to ensure their requirements are accessible this way.
For a great explanation on PATH, see astrobiomike's explanation [here](https://astrobiomike.github.io/unix/modifying_your_path)

## Github blog issues:
- Cmd + Opt + r on site to hard reload the page (reload it with no cache)

## Count how many files in a folder:
`ls | wc -l`
in zsh:
`a=(*(DN));echo ${#a}` does it without listing the files
from here: https://stackoverflow.com/a/37175347/17677514

# Data Science
Comparison of table manipulation pandas vs R:
https://datascience-enthusiast.com/R/pandas_datatable.html

## R
`pattern = "csv$"` note the use of a dollarsign to mean end of file name.

To see a small portion of a table:
`Stromal_v2[1:5,1:5]`

To look up help from R console in RStudio
`?Featureselect.V4`

To see inside an object:
object@colname

To subset a matrix
`matrix[rownames, colnames]`
eg: match makes a list (or TRUE/FALSE), then [,] subsets a matrix from that list:
`detP <- detP[match(featureNames(mSetSq),rownames(detP)),]`

RStudio restart R session
https://stackoverflow.com/questions/11579765/how-do-i-clean-up-r-memory-without-restarting-my-pc
`rm(list = ls())`
`.rs.restartR()`

Starter code for taking basenames from the file directory  
```r
test<-as.data.frame(paste(list.files()))
colnames(test) <-"idat"
test2<-as.data.frame(test[grepl('_Red.idat', test$idat),])
colnames(test2) <-"idat"
test3<-gsub("_Red.idat","",test2$idat)
```

Make new directory  
`dir.create('path/to/dir')`  
Check if directory exists  
`dir.exists('path/2/dir')`

'If' statements  
"not" conditional is represented by a '!'  
```r
if (dir.exists('/path/2/existing/dir')){
    print('yes')
    }
if (!dir.exists('/path/2/NOT-existing/dir')){
    print('no')
}
```
