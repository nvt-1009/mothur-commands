# mothur-commands

Helpful tip - within mothur, you can do shell operations with system command. For example:
```shell
system(ls) # this is for when mothur is already running
```

First, start mothur. Navigate to mothur directory and type:
```shell
./mothur
```

Set input and output directories
```shell
set.dir(input=../path/goes/here)
set.dir(output=../path/goes/here)
```

Make input file that has read information. This makes stability.files file, which makes a table with three columns: sample_ID R1 R2
```shell
make.file(input=../path/to/reads) # if gzipped, do (input=../path, type=gz)
```

Now, make contigs from reads using make.contigs command. This prints out a list of sequence IDs and counts.
```shell
make.contigs(file=stability.files, processors=3)
