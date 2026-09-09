### 1. Creating and Renaming Files/Directories
1. Create a directory named test_dir using mkdir

**Mkdir**: mkdir (Make Directory) is used to create one or more new directories (folders) in your file system. By default, it creates the folder in your current working directory unless you specify a different path.

```
$ mkdir test_dir
```
![mkdir_s.png](/screenshots/mkdir_s.png)

You can also use the -p flag to create nested parent and child directories all at once (e.g., mkdir -p folder1/folder2).
```
$ mkdir -p test_dir1/ test_dir2/ test_dir3
```
![mkdir-p_s.png](/screenshots/mkdir-p_s.png)

2. Inside test_dir, create an empty file called example.txt

**Touch**: touch is primarily used to create new, empty files instantly if they do not already exist. If the file already exists, running the command updates its access and modification timestamps to the current time without changing its contents.
```
$ touch example.txt 
```
![touch_s.png](/screenshots/touch_s.png)

3. Rename example.txt to renamed_example.txt using mv.

**Mv**: mv (Move) is used to move files or directories from one location to another in your file system. It is also the standard command used to rename a file or folder by moving it to the same directory with a new name.
```
$ mv example.txt renamed_exapmle.txt
```
![rename_s.png](/screenshots/rename_s.png)

### 2. Viewing File Contents
1. Use cat to display the contents of /etc/passwd.

**Cat**: cat (Concatenate) is used to display the entire contents of one or more text files directly in the terminal without opening an editor. It is also commonly used to combine multiple files into a single new file or to append text to an existing file using redirection operators (> or >>).
```
$ cat /etc/passwd
```
![cat_s.png](/screenshots/cat_s.png)

2. Display only the first 5 lines of /etc/passwd using head.

**Head**: head is used to display the beginning (the first few lines) of one or more text files directly in the terminal. By default, it outputs the first 10 lines of the specified file, which helps you quickly inspect a file's structure.

You can change the number of lines displayed by using the -n flag followed by the desired count (e.g., head -n 5 filename.txt).
```
$ head -n 5 /etc/passwd
```
![head_s.png](/screenshots/head-5_s.png)

3. Display only the last 5 lines of /etc/passwd using tail.

**Tail**: tail is used to display the end (the last few lines) of one or more text files directly in the terminal. By default, it outputs the last 10 lines of the specified file, which is helpful for reading the most recent entries in data files.

You can also use the -f (follow) flag to monitor a file in real-time as new lines are appended, which is commonly used for viewing live log files.

```
$ tail -n 5 /etc/passwd
```

### 3. Searching for Patterns
1. Use grep to find all lines containing the word “root” in /etc/passwd

**Grep**: grep (Global Regular Expression Print) is used to search for specific text patterns or matching strings within one or more files. It scans the file line by line and prints every line that contains the specified keyword or regular expression.

You can use flags like -i to ignore case sensitivity, -r to search recursively through directories, and -n to display line numbers with the results.
```
$ cat /etc/passwd | grep “root”
```
![tail-5_s.png](/screenshots/tail-5_s.png)

### 4. Zipping and Unzipping
1. Compress the test_dir directory into a file named test_dir.zip using zip.

**Zip**: zip is used to compress one or more files and directories into a single archive file, reducing overall file size and saving storage space. It packages the files together while preserving their directory structures, making them easier to share or backup.

You can use the -r flag to recursively compress an entire directory and all of its contents.
```
$ zip -r test_dir.zip test_dir
```
![zip_s.png](/screenshots/zip_s.png)

2. Unzip test_dir.zip into a new directory named unzipped_dir.

**Unzip**: unzip is used to extract, decompress, and unpack files from a .zip archive file into your current directory. It automatically restores the original file sizes, properties, and directory structures that were created during compression.

You can use the -d flag to extract the contents into a specific destination folder instead of the current one.
```
$ unzip test_dir.zip -d unzipped_dir
```
![unzip_s.png](/screenshots/unzip_s.png)

### 5. Downloading Files

**Wget**: wget (World Wide Web Get) is a network utility used to download files, pages, and assets directly from the internet using HTTP, HTTPS, or FTP protocols. It runs entirely in the background, allowing you to close your terminal session or log off while large downloads continue.

You can use the -c flag to resume a partially downloaded file after a connection interruption, or the -r flag to download entire websites recursively.
```
$ wget https://github.com/ishandevani/Finance-Banking---Advanced-Threat-Intelligence-Platform-TIP-Dynamic-Policy-Enforcer/blob/main/screenshots/Mongo4.png
```
![wget_s.png](/screenshots/wget_s.png)

### 6. Changing Permissions
**Chmod**: chmod (Change Mode) is used to modify the read, write, and execute permissions of files and directories for owners, groups, and other users. You can change these access levels using either symbolic notation (like u+x to add execute permissions) or octal numbers (like 755 for standard web folders).

```
$ sudo chmod 444 secure.txt
$ ls -la
```
![chmod_s.png](/screenshots/chmod_s.png)

### 7. Working with Environment Variables
**Export**: export is used to set environment variables in the Linux shell, making them available to any child processes or scripts started from that session. Without it, a newly created variable is only local and cannot be read by commands run inside that terminal.

```
$ export MY_VAR="Hello, Linux!"
$ Echo $MY_VAR
```
![export_s.png](/screenshots/export_s.png)