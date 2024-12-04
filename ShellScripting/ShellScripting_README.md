 # Shell Script

#### What is shell script
A shell script is a text file with commands for a Unix-based operating system's shell to execute, automating tasks, and processes. These scripts can use variables, loops, conditionals, and functions, making them powerful for system management. Common shells include Bash, widely used on Linux and macOS.

#### What is Shebang?
In Linux, a shebang is a special character sequence at the beginning of a script file that specifies the interpreter to be used to execute the script. It consists of a hash character (#) followed by an exclamation mark (!), hence the name "shebang."
For example, the shebang line #!/bin/bash indicates that the script should be executed using the Bash shell interpreter located at /bin/bash.


#### Explain Korn shell vs bash shell
       Korn shell is older than Bash shell: Korn shell was developed in the 1980s, while Bash shell was developed in the 1990s. As a result, Korn shell is more widely used in older systems, while Bash shell is more common in modern systems.
    Syntax: Both shells have a similar syntax and share many of the same commands. However, there are some differences in syntax, such as the way arrays are declared and indexed.
Features: Bash shell has more features than Korn shell, including command line editing, history, and tab completion. It also has more advanced programming features such as regular expressions and process substitution.
   Compatibility: Bash shell is backward compatible with the Bourne shell (sh), which means that scripts written for sh can be run with bash without modification. Korn shell is not fully compatible with sh, which means that some sh scripts may need to be modified to run on ksh.


#### 8. What are some limitations of Shell scripting?
Answer: Shell scripting can be less efficient for complex logic and data manipulation compared to other programming languages. It lacks advanced data structures and error-handling features, making it challenging to debug and maintain large scripts. Shell scripts are also platform-dependent and may have compatibility issues across different environments.
#### 31. What are some basic Bash commands?
Answer: Basic Bash commands include:
ls: Lists directory contents.
cd: Changes the directory.
cp: Copies files or directories.
mv: Moves or renames files or directories.
rm: Removes files or directories.
cat: Displays file contents.
echo: Prints text to the terminal.
grep: Searches for patterns in files.
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


23. Write a BASH Script for Prime numbers.
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
