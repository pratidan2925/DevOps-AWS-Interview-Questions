 # Shell Script

#### 1) What is Shell?
A shell is a command-line interpreter that provides a user interface to access the operating system's services. It takes commands from the user and executes them.

#### 2) What is Shell Scripting?
Shell scripting refers to writing a series of commands for the shell to execute as a script. It allows automation of tasks, creating complex workflows, and enhancing productivity in a Unix/Linux environment.

#### 3) What is the importance of writing Shell Scripts?
Shell scripts automate repetitive tasks, improve system administration, enable batch processing, and enhance system management. They are essential for managing and controlling the Unix/Linux operating system efficiently.

#### 4) List some of the common and most widely used UNIX commands.
Common Unix commands include ls (list files), cd (change directory), mkdir (make directory), rm (remove files), cp (copy files), mv (move files), grep (search for patterns), sed (stream editor), awk (text processing), cat (concatenate files), chmod (change file permissions), chown (change file owner), ps (process status), kill (terminate processes), etc.

#### 5) Shell programs are stored in which file?
Shell scripts are typically stored in plain text files with a .sh extension. These files contain commands that the shell interpreter executes.
#### 6) What are the different types of Shells available?
- Different types of shells include:
- Bourne Shell (sh): Original Unix shell.
- Bash (Bourne Again Shell): Enhanced version of sh, default on most Linux distributions.
- C Shell (csh): C-like syntax shell.
- Korn Shell (ksh): Enhanced version of sh with more features.
- Z Shell (zsh): Powerful interactive shell with extended features.

#### 7) What are the advantages of C Shell over Bourne Shell?
C Shell (csh) has a syntax similar to the C programming language, making it easier for C programmers to use. It includes features like history mechanism, job control, aliases, and interactive prompts, which were not present in the original Bourne Shell.

#### 8) In a typical UNIX environment how many kernels and shells are available?
A typical Unix/Linux environment has one kernel (the core of the operating system) and several shells that users can choose from for command-line interaction.

#### 9) Is a separate compiler required for executing a shell program?
No, a separate compiler is not required for executing a shell program. Shell scripts are interpreted by the shell itself (e.g., Bash interprets Bash scripts), so you only need the appropriate shell installed on the system.

#### 10) How many shell scripts come with the UNIX operating system?
- The number of shell scripts included with Unix/Linux distributions varies, but typically there are numerous system scripts for managing the OS, plus user-created scripts for various applications and tasks.

#### 11) When should shell programming/scripting not be used?
 - Shell scripting may not be suitable for complex applications requiring high performance or extensive data processing. It may also not be ideal for tasks better suited to compiled languages or where security and performance are critical.

#### 13) Basis of shell program relies on what fact?
- The basis of a shell program relies on interpreting user commands and executing them as system commands or scripts, facilitating interaction with the operating system and automation of tasks.

#### 14) What are the default permissions of a file when it is created?
- The default permissions of a file when it is created are usually determined by the umask (user mask) settings of the user creating the file. Typically, new files have permissions 666 (read and write for owner, group, and others), and directories have permissions 777 (read, write, and execute for owner, group, and others), modified by the umask.

#### 15) What can be used to modify file permissions? 
- The chmod command is used to modify file permissions in Unix/Linux. It allows you to change permissions for the owner, group, and others on a file or directory.

#### 16) How to accomplish any task via shell script?
- You can accomplish tasks via shell script by writing a sequence of commands in a text file, making it executable (chmod +x script.sh), and then executing it (./script.sh). Shell scripts can automate file operations, system administration tasks, data processing, and more.

#### 17) What are Shell Variables?
- Shell variables are placeholders used to store data, such as strings or numbers, for later use within a shell script or session. They facilitate passing information between commands and scripts.

#### 18) What are the two types of Shell Variables? Explain in brief. 
- There are two types of shell variables: - Local variables: These are defined and used within a single shell script or session. - Environment variables: These are inherited by child processes and are accessible globally within the shell environment.

#### 19) How are shell variables stored? Explain with a simple example.
- Shell variables are stored in memory and can be accessed or modified using the variable name prefixed with a dollar sign ($). For example: bash greeting="Hello" echo $greeting

#### 20) What is the lifespan of a variable inside a shell script?
- The lifespan of a variable inside a shell script depends on whether it is a local variable or an environment variable. Local variables exist only within the script or session where they are defined. Environment variables are accessible globally until the shell session ends.

#### 21) How to make variables unchangeable?
- You can make variables read-only (unchangeable) using the readonly built-in command in Bash. For example: bash readonly myvar="immutable"

#### 22) How variables can be wiped out?
- Shell variables can be unset (removed) using the unset built-in command followed by the variable name. For example: bash unset myvar

#### 23) What are positional parameters? Explain with an example.
- Positional parameters in shell scripting refer to the arguments passed to a script or function when it is called. They are accessed using variables like $1, $2, etc., where $1 represents the first argument, $2 represents the second, and so on. Here's an example:

- Script: example.sh
- Usage: ./example.sh arg1 arg2
```
  echo "First argument: $1"
  echo "Second argument: $2"
```
#### 23) What does the . (dot) indicate at the beginning of a file name and how should it be listed?
A dot (.) at the beginning of a file name in Unix/Linux indicates that the file is hidden. To list all files, including hidden ones, you can use the -a option with the ls command:
ls -a

#### 24) Generally, each block in UNIX is how many bytes?
In Unix filesystems, each block is typically 4096 bytes (4 KB).

#### 25) By default, a new file and a new directory that is being created will have how many links?
By default, a new file has 1 link (to itself). A new directory has 2 links: one link to itself (.) and one link to its parent directory (..).

#### 26) Explain about file permissions.
File permissions in Unix/Linux determine who can read, write, or execute a file. They are represented by three sets of permissions: owner, group, and others. Each set has three types of permissions: read (r), write (w), and execute (x). Permissions can be viewed and modified using commands like ls -l and chmod.

#### 27) What is a file system?
A file system is a method used by operating systems to organize and store data on storage devices like hard drives. It defines how data is structured, stored, retrieved, and managed. Common file systems include ext4, NTFS, and FAT32.

#### 28) What are the different blocks of a file system? Explain in brief.
- File systems are organized into different blocks:
- Superblock: Contains metadata about the entire file system.
- Inode: Contains metadata about each individual file or directory, including permissions, ownership, and location.
- Data blocks: Store the actual data of files and directories.
- Block groups: Divide the file system into smaller groups for better management and performance.

#### 29) What are the three different security provisions provided by UNIX for a file or data?
- Unix provides three levels of security provisions for files:
- Ownership and Permissions: Assigning ownership (user and group) and setting permissions (read, write, execute).
- Access Control Lists (ACLs): Granting permissions beyond traditional owner, group, and others.
- File Attributes: Using attributes like immutable (chattr +i) or append-only (chattr +a) to restrict changes.

#### 30) What are the three editors available in almost all the versions of UNIX?
- Three common editors in Unix/Linux are:
- vi (Vim): Powerful text editor with modes like command mode and insert mode.
- nano: Simple and user-friendly text editor.
- emacs: Extensible text editor with its own scripting language.

#### 31) What are the three modes of operation of vi editor? Explain in brief.
- Vi editor has three main modes:
- Command mode: Default mode for navigating the file and executing commands.
- Insert mode: Mode for inserting and editing text.
- Ex mode: Mode for executing commands that start with a colon (:).

#### 32) What is the alternative command available to echo and what does it do?
The printf command is an alternative to echo in Unix/Linux. It provides more control over formatting output, allowing for precise control over how data is printed.

#### 33) How to find out the number of arguments passed to the script?
You can find the number of arguments passed to a script using the special variable $#. For example:
```
#!/bin/bash
echo "Number of arguments passed: $#"
```
#### 34) What are control instructions and how many types of control instructions are available in a shell? Explain in brief.
- Control instructions in shell scripting are used to control the flow of execution based on conditions. They include:
- Conditional statements: if, else, elif
- Looping statements: for, while, until
- Control flow modifiers: break, continue, return, exit

#### 35) What are Loops and explain three different methods of loops in brief?
- Loops in shell scripting are used to repeat commands or tasks. Three common types of loops are:
- for loop: Iterates over a list of items.
- while loop: Executes commands as long as a condition is true.
- until loop: Executes commands until a condition becomes true.

#### 36) What is IFS?
IFS stands for Internal Field Separator. It is a special variable in Unix/Linux shells (like Bash) that determines how the shell recognizes fields (words or tokens) in input. By default, it includes spaces, tabs, and newlines as field separators, but you can change it to suit your needs using the IFS variable.
For example:
```
# Setting IFS to comma for CSV processing
IFS=,

```
#### 37) What is a Break statement and what is it used for?
In shell scripting, the break statement is used to exit from a loop prematurely. It is typically used inside loops (like for or while) to terminate the loop early based on certain conditions.

#### 38) What is Continue statement and what is it used for?
The continue statement is used in shell scripting to skip the remaining commands in a loop iteration and jump to the next iteration. It allows you to skip certain iterations based on specific conditions without exiting the loop entirely.

#### 39) What are Metacharacters in a shell? Explain with some examples.

- Metacharacters in shell scripting are special characters that have specific meanings or functions. Some common metacharacters include:
- *: Wildcard character for matching zero or more characters.
- ?: Wildcard character for matching a single character.
- |: Pipe symbol used for piping output of one command to another.
- $: Dollar sign used to reference variables.
- > and <: Redirection symbols for output and input redirection, respectively.
- Example: 
```
# Using * to match files in current directory
ls *.txt
# Piping output of one command to another
cat file.txt | grep "pattern"
# Redirection of output to a file
echo "Hello, World!" > output.txt

```
#### 40) How to execute multiple scripts? Explain with an example.

- You can execute multiple scripts sequentially in a shell script by calling them one after another. Here's an example:
```
#!/bin/bash
# Script: execute_multiple.sh
# Execute script1.sh
./script1.sh
# Execute script2.sh
./script2.sh

```

#### 41) Which command needs to be used to know how long the system has been running?
You can use the uptime command to know how long the system has been running:
uptime

#### 42) How to find the current shell which you are using?
You can find out the current shell you are using with the echo command and the SHELL environment variable:echo $SHELL

#### 43) How to find all the available shells in your system?
You can find all available shells on your system by looking at the /etc/shells file or by using the cat command on it:
cat /etc/shells

#### 44) How to read keyboard inputs in shell scripts?
You can read keyboard inputs in shell scripts using the read command. Here's an example:
```
#!/bin/bash
echo "Enter your name:"
read name
echo "Hello, $name!"
```

#### 45) How many fields are present in a crontab file and what does each field specify?
A crontab file has five fields for specifying the schedule of a job:
```
* * * * * command
```

- Minute (0-59)
- Hour (0-23)
- Day of the month (1-31)
- Month (1-12)
- Day of the week (0-6, where 0 is Sunday)
- command: The command to be executed

#### 46) What are the two files of crontab command?
- The crontab command uses two files:
- System-wide crontab: Located in /etc/crontab, used for system-level cron jobs.
- User-specific crontab: Managed by crontab -e command for individual users.

#### 47) What command needs to be used to take the backup?
- To take a backup in Unix/Linux, you can use tools like tar or cp. For example, to create a backup of a directory:
- tar -czvf backup.tar.gz /path/to/directory

#### 48) What are the different commands available to check the disk usage?
- Different commands to check disk usage include:
- df: Displays disk space usage of filesystems.
- du: Displays disk usage of files and directories.

#### 49) What are the different communication commands available in Unix/Shell?
- Different communication commands in Unix/Shell include:
- write: Send a message to another user.
- wall: Write a message to all users.
- mesg: Control terminal message access.

#### 50) How to find out the total disk space used by a specific user, say for example username is John?
You can find out the total disk space used by a specific user using the du command with grep to filter results. For example:
```
du -sh /home/* | grep 'John'
```

#### 51) What is Shebang in a shell script?
The Shebang (#!) is a special character sequence in the first line of a script that tells the operating system which interpreter to use to execute the script. For example:
```
#!/bin/bash
```

#### 52) What is the command to be used to display the shell’s environment variables?
You can display the shell’s environment variables using the env command:
env

#### 53) How to debug the problems encountered in shell script/program?
- You can debug shell scripts using techniques like:
- Adding echo statements to print variable values.
- Using set -x to enable debugging mode.
- Using trap to catch signals and handle errors.

#### 54) How to know the variable length?
- You can find out the length of a variable using the ${#variable} syntax. For example:
```
var="Hello, World!"
echo ${#var}  # Outputs: 13
```
#### 55) What is the difference between = and ==?
- In shell scripting:
- = is used for variable assignment.
- == is used for string comparison in conditional statements (like if).

#### 56) How to open a read-only file in Unix/shell?
You can view the contents of a read-only file using commands like cat, less, more, etc. For example:
cat file.txt

#### 57) How can the contents of a file inside a jar be read without extracting in a shell script?
You can use the jar command with options to list the contents of a jar file without extracting it:
jar tf file.jar

#### 58) What is the difference between diff and cmp commands?
- Both diff and cmp commands are used to compare files:
- diff: Shows line-by-line differences between two files.
- diff file1.txt file2.txt
- cmp: Compares two files byte by byte and reports the first byte that differs.
- cmp file1.txt file2.txt

#### 59) Explain in brief about sed command with an example.
- sed (stream editor) is used for text manipulation in Unix/Linux:
- Example: Replace all occurrences of "old" with "new" in file.txt and print the output to stdout.
- sed 's/old/new/g' file.txt

#### 60) Explain in brief about awk command with an example.
- awk is used for pattern scanning and processing in Unix/Linux:
- Example: Print the second field (column) of each line in file.txt.

```
awk '{print $2}' file.txt
```

#### What is shell script
A shell script is a text file with commands for a Unix-based operating system's shell to execute, automating tasks, and processes. These scripts can use variables, loops, conditionals, and functions, making them powerful for system management. Common shells include Bash, widely used on Linux and macOS.

#### What is Shebang?
- In Linux, a shebang is a special character sequence at the beginning of a script file that specifies the interpreter to be used to execute the script. It consists of a hash character (#) followed by an exclamation mark (!), hence the name "shebang."
- For example, the shebang line #!/bin/bash indicates that the script should be executed using the Bash shell interpreter located at /bin/bash.


#### Explain Korn shell vs bash shell
- Korn shell is older than Bash shell: Korn shell was developed in the 1980s, while Bash shell was developed in the 1990s. As a result, Korn shell is more widely used in older systems, while Bash shell is more common in modern systems.
- Syntax: Both shells have a similar syntax and share many of the same commands. However, there are some differences in syntax, such as the way arrays are declared and indexed.
- Features: Bash shell has more features than Korn shell, including command line editing, history, and tab completion. It also has more advanced programming features such as regular expressions and process substitution.
- Compatibility: Bash shell is backward compatible with the Bourne shell (sh), which means that scripts written for sh can be run with bash without modification. Korn shell is not fully compatible with sh, which means that some sh scripts may need to be modified to run on ksh.


#### 8. What are some limitations of Shell scripting?
Answer: Shell scripting can be less efficient for complex logic and data manipulation compared to other programming languages. It lacks advanced data structures and error-handling features, making it challenging to debug and maintain large scripts. Shell scripts are also platform-dependent and may have compatibility issues across different environments.

#### 31. What are some basic Bash commands?
- Answer: Basic Bash commands include:
- ls: Lists directory contents.
- cd: Changes the directory.
- cp: Copies files or directories.
- mv: Moves or renames files or directories.
- rm: Removes files or directories.
- cat: Displays file contents.
- echo: Prints text to the terminal.
- grep: Searches for patterns in files.

#### 9. What’s the difference between $* and $@ in Bash?
Answer: In Bash, $* treats all positional parameters as a single string, while $@ treats them as separate strings. When quoted, " $* " joins all arguments into a single string with spaces between them, while " $@ " treats each argument as a separate quoted string.

#### 32. How do you access a service from any directory in Linux?
Answer: To access a service from any directory in Linux, ensure that the service's executable is in a directory listed in the PATH environment variable. You can add the directory containing the executable to PATH by modifying your shell's configuration file (e.g., .bashrc or .bash_profile) and then reloading it with source ~/.bashrc.

#### 33. Where should system services be saved?
Answer: System services should be saved in the appropriate directories based on the init system used. For systemd, service files are typically stored in /etc/systemd/system/ for custom services or /lib/systemd/system/ for system-provided services. For SysVinit, service scripts are usually located in /etc/init.d/.

#### 4. What’s the difference between a cron job and running it under sudo?
Answer: A cron job is a scheduled task that runs as the user who created the job. Running a cron job under sudo allows it to execute with elevated privileges, meaning it can perform tasks that require root access, such as system-level operations. Without sudo, the cron job is limited to the permissions of the user who created it.

#### 5. How do you address security issues in cron jobs?
Answer: To address security issues in cron jobs, I ensure that only necessary permissions are granted to the jobs, avoid storing sensitive data in scripts, use secure paths and environment variables, regularly review and audit cron jobs, and run jobs with the least privilege necessary. I also ensure that any output from cron jobs is logged and monitored for anomalies.


#### 23. Write a BASH Script for Prime numbers.
Answer:
```
#!/bin/bash
# Function to check if a number is prime
is_prime() {
    n=$1
    if [ $n -le 1 ]; then
        echo "$n is not a prime number."
        return
    fi
    for (( i=2; i*i<=$n; i++ ))
    do
        if [ $((n % i)) -eq 0 ]; then
            echo "$n is not a prime number."
            return
        fi
    done
    echo "$n is a prime number."
}

# Accept a number from the user
read -p "Enter a number: " num

# Check if the number is prime
is_prime $num

```
