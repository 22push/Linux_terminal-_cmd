# 📁 Linux Command Cheat Sheet

A handy reference for commonly used Linux terminal commands with explanations.

---

## 📖 General Commands

### `man`
Shows the manual page (help documentation) for any command.
```bash
man ls
```

---

## 📂 Listing Files and Directories

### `ls`
Lists files and directories in the current directory.
```bash
ls
```

### `ls /bin`
Lists the contents of the `/bin` directory.

### `ls -al`
Lists all files (including hidden files) in long format.

### `ls -l`
Shows files in long listing format (excluding hidden files).

### `ls -a`
Shows all files including hidden ones (starting with `.`).

---

## 📁 Navigation (cd, pwd)

### `cd file_name`
Change directory to `file_name`.

### `cd ..`
Go one directory up (parent folder).

### `cd`
Go back to the home directory.

### `cd ~/file_name`
Go to a folder using its absolute path from the home directory.

### `pwd`
Print the current directory path.

---

## 🏗️ Creating and Managing Directories

### `mkdir file_name`
Create a new directory.

### `mkdir f1 f2`
Create multiple directories at once.

### `mkdir -p fruits/apples`
Create nested folders (`fruits` and inside it `apples`) using the `-p` option.

---

## ❌ Deleting Folders

### `rmdir file_name`
Delete an empty folder.

### `rmdir f1 f2`
Delete multiple empty folders.

### `rm -rf f1 f2`
Delete folders with files inside using `rm` with `-r` (recursive) and `-f` (force) options.

---

## 📄 File Operations

### `touch filename.txt`
Create a new empty file in the current directory.

### `mv pear new_pear`
Move (or rename) the file `pear` to the folder or file name `new_pear`.

### `cp file_name`
Copy a file to the current directory (or specified location).

### `cp -r folder_name`
Recursively copy a folder and all its contents.

---

## 🔍 Using `find` Command

### `find . -name '*.js'`
Find all `.js` files in the current directory and its subdirectories.

### `find . -type d -name src`
Find all directories named `src`.

### `find folder1 folder2 -name filename.txt`
Search for `filename.txt` inside `folder1` and `folder2`.

### `find . -type d -name node_modules -or -name public`
Find directories named `node_modules` **or** files/directories named `public`.

> ✅ Tip: For clarity, use parentheses:
```bash
find . \( -type d -name node_modules -or -type d -name public \)
```

### `find . -type f -size +100c`
Find files larger than 100 bytes.

### `find . -type f -size +100k -size -1M`
Find files with size between 100KB and 1MB.

### `find . -type f -mtime +3`
Find files modified more than 3 days ago.

### `find . -type f -mtime -1`
Find files modified in the last 24 hours.

### `find . -type f -mtime -1 -delete`
Find and delete files modified in the last 24 hours.

### `find . -type f -exec cat {} \;`
Print the contents of all found files using `cat`.

---

📌 **Note**: Always test destructive commands (like `-delete` or `rm -rf`) carefully before use.
