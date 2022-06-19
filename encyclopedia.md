# My Coding and Commandline Encyclopedia
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
