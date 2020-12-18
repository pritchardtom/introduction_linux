# Linux Commands Cheatsheet

## Navigating the System
### Where am I?

Use the `pwd` command to print the current directory you're in:

```
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

In the above example, `input_files` and `output_files` are folders.  On Sunbird, these are often coloured blue (or equivalent) to highlight they're folders.  

However, on some systems this might not come up and you cannot immediately tell from the output .  As we covered in the demo, however, lots of Linux commands can take flags (or options) to change this behaviour.

[s.a.username@sl2 ~]$

###

#

[s.a.username@sl2 ~]$
