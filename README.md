# auditrash
Log-audited recycle bin for Linux with some utilities. Useful if the system is going to be used by several people.

# What will you find?

#### 'auditrash' script

>Welcome to auditrash, currently there are 0 files at the /recyclebin (4,0K)  
>WARNING! auditrash will auto-wipe /recyclebin on 28th every month.  
>---------------------------------------------------------------------------
>1) Llist recycled files	     
>2) Info about recycled file  
>3) Restore recycled file     
>4) Restore by extension
>5) Wipe out /recyclebin now
>6) Check the log files
>7) Exit auditrash  
>Choose an option 1-7:

#### 'del' script

>Usage: del [OPTION]... FILE... [FILE]...  
>REMOVE or RECYCLE files to /recyclebin, generating log files  
>  -f  force remove all the selected files and generate a log  
>  -r  recycle selected files to /recyclebin and generate a log  
>By default, ommiting the control parameter, run -r  
>Manage /recyclebin files and check logs generated by running 'auditrash'  
>AUTHOR: github.com/dam6  

#### 'wipebin' script
>It will auto-execute itself 28th of every month via adding a /etc/crontab line with the 'installer' script.  
>Every time that executes, rename the current.log file to a new MONTH-YEAR.old file and starts a new current.log.  

#### Logs example file
operation : day/month/year : hh.mm : absolute/path/to/file : user  
>recycle:09/07/2022:20.01:/home/dam6/song.mp4:dam6  
>recycle:09/07/2022:20.03:/etc/passwd:impulsado    
>restored:09/07/2022:20.05:/etc/passwd:dam6  
>removal:09/07/2022:20.01:/home/impulsado:dam6  

# Copy this to install:
  
Feel free to modify permissions at installer script to adapt your necessities.
  
`git clone https://github.com/dam6/auditrash.git && cd auditrash && chmod 755 installer && ./installer`  
