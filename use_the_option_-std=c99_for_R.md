# [How use the option -std=c99 for installing R packages](https://stackoverflow.com/questions/35198301/how-use-the-option-std-c99-for-installing-r-packages)

## ![Questions]("_std=c99.png")


## Answer
If not already existing, create a directory in your $HOME (/home/mousavian/.R in your case). Inside, create a Makevars file (no extension). Edit this file with your favorite editor and write:
    
    CC = gcc -std=c99
    
Then, save it and after starting R, simply run

    install.packages("plyr", dependencies = TRUE)
    
It should compile with gcc -std=c99.
