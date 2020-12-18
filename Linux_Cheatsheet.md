# Linux Commands Cheatsheet

## Navigating the System
### Where am I?

Use the `pwd` command to print the current directory you're in:

```bash
[s.a.username@sl2 ~]$ pwd
/home/s.a.username

[s.a.username@sl2 ~]$ pwd
/home/s.a.username/slurm_scripts/output
```

### Change Directories

Use the `cd` command to change the directory you are in.  

Let's say we're currently in `/home/s.a.username/slurm_scripts/output` and you want to go to `/home/s.a.username/slurm_scripts`.  You can do this by typing it all out:

```
[s.a.username@sl2 ~]$ cd /home/s.a.username/slurm_scripts
[s.a.username@sl2 ~]$ pwd
/home/s.a.username/slurm_scripts
```

But a better way, because we just want to go up one directory is to use the `..` notation:

```
[s.a.username@sl2 ~]$ cd ..
[s.a.username@sl2 ~]$ pwd
/home/s.a.username/slurm_scripts

```

We can also chain together `..` to move up more than one directory.  For example:

```
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2020/December
[s.a.username@sl2 ~]$ cd ../../
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results

[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2020/December
[s.a.username@sl2 ~]$ cd ../../2019/january
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2019/january
```

Wherever you are on the system, entering just `cd` will take you back to your home directory:

```
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2020/December
[s.a.username@sl2 ~]$ cd
[s.a.username@sl2 ~]$ pwd
/home/s.a.username
```

### What's Here?

Use the `ls` command to list the contents of folders.

```
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2020/December
[s.a.username@sl2 ~]$ ls
input_files  output_files  readme.txt
```

In the above example, `input_files` and `output_files` are folders.  On Sunbird, these are often coloured blue (or equivalent) to highlight they're folders.  However, on some systems this colourisation of folders might not be set up, meaning you cannot immediately tell they are folders.  As we covered in the demo, however, lots of Linux commands can take flags (or options) to change this behaviour.

Adding the `-F` flag/option to our `ls` command will add a `/` to anything that is a folder:

```
[s.a.username@sl2 ~]$ pwd
/scratch/s.a.username/Rscripts/results/2020/December
[s.a.username@sl2 ~]$ ls -F
input_files/  output_files/  readme.txt
```

#### Common Flags/Options for `ls`

- `ls -l`    --> long listing format.
- `ls -a`    --> list all files, including hidden files.
- `ls -t`    --> list files by time
- `ls -h`    --> display file sizes in human-readable format, not in bytes.

We can use multiple flags/options at once.  So for example, `ls -lhtF` will output the result in a list format, with human-readable file sizes, ordered by modification time (newest first), with a trailing `/` to indicate folders:

```
[s.a.username@sl2 ~]$ ls -lhtF
drwxrwxr-x. 5 s.a.username s.a.username 4.0K Dec 18 12:54 slurm_scripts/
-rw-rw-r--. 1 s.a.username s.a.username   43 Dec 18 12:04 new.txt
-rw--w----. 1 s.a.username s.a.username   70 Dec 18 12:03 test_new.sh
drwxrwxr-x. 2 s.a.username s.a.username 4.0K Dec 18 12:00 testy/
-rw-------. 1 s.a.username s.a.username  67M Oct 17  2019 ascomycota_odb9.zip
```


###

#

[s.a.username@sl2 ~]$
