# Module 05: Command Line Skills

> **Course:** NDG Linux Essentials  
> **Status:** 🔄 In Progress  
> **Objective:** Understand the Linux command line interface, shells, and prompt structure.

---

## 📖 Lesson 5: Command Line Skills

### 5.1 Command Line Skills

#### Introduction
- Most consumer operating systems are designed to shield the user from the ins and outs of the CLI. the linux community is different in that it positively celebrates the CLI for its power, speed and ability to accomplish a vast array of tasks with a single command line instruction.
- When a user first encounters the CLI, they can find it challenging because it requires memorizing a dizzying amount of commands and their options. however, once a user has learned the structure of how commands are used, where the necessary files and directories are located and how to navigate the hierarchy of a file system, they can be immensely productive. This capability provides more precise control, greater speed and the ability to automate tasks more easily through scripting.
- Furthermore, by learning the CLI, a user can easily be productive almost instantly on any flavor or distribution of linux, reducing the amount of time needed to familiarize themselves with a system because of variations in a GUI.

#### Why is knowing command line important?
- Flexibility and mobility!

### 5.2 Shell
- Once a user has entered a command the terminal then accepts what the user has typed and passes it to a shell. the shell is the command line interpreter that translates commands entered by a user into actions to be performed by the operating system. If output is produced by the command, then text is displayed in the terminal. If problems with the command are encountered, an error message is displayed.
- the linux environment allows the use of many different shells, some of which have been around for many years. the most commonly used shell for this course is called the Bash shell. Bash provides many advanced features, such as the command history and inline editing, which allows a user to easily re execute previously executed commands or a variation of them via simple editing.
- the Bash shell also has other popular features, a few of which are listed below:
  - **scripting:** the ability to place commands in a file and then interpret (effectively use Bash to execute the contents of) the file, resulting in all of the commands being executed. this feature also has some programming features, such as conditional statements and the ability to create functions (AKA subroutines).
  - **Aliases:** the ability to create short nicknames for longer commands.
  - **Variables:** Used to store information for the Bash shell and for the user. these variables can be used to modify how commands and features work as well as provide vital system information.
- Bash has an extensive feature list; this is only a sampling of its capabilities.
- When a terminal application is run, and a shell appears, displaying an important part of the interface - the prompt. Not only is the prompt where to indicate that commands can be run, but it also provides useful information to the user. The prompt is fully configurable, and can be as sparse or as full-featured as is practical and useful.
- the structure of the prompt may vary between distributions, but typically contains information about the user and the system. Below is a common prompt structure:

```text
sysadmin@localhost:~$
```
*(username: sysadmin, systemname: localhost, current directory: ~)*

- the prompt shown contains the following information: username, systemname, and current directory.
- the ~ symbol is used as shorthand for the user's home directory. typically the home directory for the user is under the /home directory and named after the user account name, for example, /home/sysadmin

### 5.3 Commands
- what is a command? the simplest answer is that a command is a software program that, when executed on the CLI, performs an action on the computer.
- To execute a command, the first step is to type the name of the command.

**Example:**
```text
sysadmin@localhost:~$ ls
```
**Note:**
- By itself, the ls commands lists files and directory contained in the current working directory.
- Many commands can be used by themselves with no further input. Some commands require additional input to run correctly. This additional input comes in two forms: options and arguments.
- The typical format for a command is as follows:
```text
command [options] [arguments]
```
- options are used to modify the core behaviour of a command while arguments are used to provide additional information (such as a file name or a username). Each option and argument is normally seperated by a space, although options can be often combined.
- Keep in mind that linux is case-sensitive. commands, options, arguments, variables, and file names must be entered exactly as shown.

#### 5.3.1 Arguments
```text
command [options] [arguments]
```
- An argument can be used to specify something for the command to act upon. If the ls command is given the name of a directory as an argument, it lists the contents of that directory. In the following example, the /etc/ppp directory is used as an argument; the following resulting output is a list of files contained in that directory:

```text
sysadmin@localhost:~$ ls /etc/ppp
ip-down.d   ip-up.d
```
*(ip-down.d and ip-up.d are files in the directory)*

- The ls command also accepts multiple arguments. To list the contents of both the /etc/ppp and /etc/ssh directories, pass them both as arguments:

```text
sysadmin@localhost:~$ ls /etc/ppp /etc/ssh
/etc/ppp:
ip-down.d   ip-up.d
/etc/ssh:
moduli                  ssh-host-dsa_key.pub
ssh_host_ecdsa_key      ssh_host_rsa_key.pub
ssh_host_dsa_key        ssh_host_ecdsa_key.pub
ssh_host_rsa_key        sshd_config
ssh_import_id
```
*(2 ls commands at once on /etc/ppp and /etc/ssh)*

#### 5.3.2 Options
```text
command [options] [arguments]
```
- Options can be used with commands to expand or modify the way command behaves. For example, using the -l option of the ls command results in a long listing, providing additional information about the files that are listed, such as the permissions, the size of the file and other information:
- Note that, in the command, -l is a lowercase letter "L". An easy way to remember this is -l is a mnemonic (easy to memorize programming code) for long listing.

```text
sysadmin@localhost:~$ ls -l
total 0
drwxr-xr-x 1 sysadmin sysadmin 0 Jan 29
20:13 Desktop
```
- Often the character is chosen to be mnemonic for its purpose, like choosing the letter l for long or r for reverse. By default, the ls command prints the results in alphabetical order, and so by adding the -r option, it prints the results in reverse alphabetical order.

```text
sysadmin@localhost:~$ ls -r
Videos Templates Public Pictures Music
Downloads Documents Desktop
```
- In most cases, options can be used in conjunction with other options. They can be given as separate options, as in -l -r, or combined, as in -lr. the combination of these two options would result in a long listing output in reverse alphabetical order.

```text
sysadmin@localhost:~$ ls -lr
total 32
drwxr-xr-x 2 sysadmin sysadmin 4096
Oct 31 20:13 Downloads
drwxr-xr-x 2 sysadmin sysadmin 4096
Oct 31 20:13 Documents
drwxr-xr-x 2 sysadmin sysadmin 4096
Oct 31 20:13 Desktop
```
- The order of the combined options isn't important. the output of all these examples would be the same:
```text
ls -l -r
ls -rl
ls -lr
```
- By default the -l option of the ls command displays files sizes in bytes:
```text
sysadmin@localhost:~$ ls -l /usr/bin/perl
-rwxr-xr-x 2 root root 10376 Feb 4
2018 /usr/bin/perl
```
- If the -h option is added, the file sizes will be displayed in human readable format:
```text
sysadmin@localhost:~$ ls -lh /usr/bin/perl
-rwxr-xr-x 2 root root 11K Feb 4
2018 /usr/bin/perl
```
- Options are often single letters; however, sometimes they are words or phrases as well. Typically, older commands use single letters while newer commands use complete words for options.
- Single-letter options are preceded by a single dash - character, like the -h option. Full-word options are preceded by two dash -- characters. the -h option also has an equivalent full-word form: the --human-readable option.

```text
sysadmin@localhost:~$ ls -l
--human-readable /usr/bin/perl
-rwxr-xr-x 2 root root 11K Feb 4
2018 /usr/bin/perl
```

#### 5.3.3 History
- when a command is executed in the terminal, it is stored in a history list. this is designed to make it easy to execute the same command later eliminating the need to retype the entire command.
- Pressing the Up Arrow ↑ key the previous command on the prompt line. The entire history of commands run in the current session can be displayed by pressing UP repeatedly to move back through the history of commands that have been run. Pressing the Enter key runs the displayed command again.
- When the desired command is located, the Left Arrow ← and Right Arrow → keys can position the cursor for editing.
- Other useful keys include the Home, End, Backspace and Delete keys.
- To view the history list of a terminal, use the history command:

```text
sysadmin@localhost:~$ date
Wed Dec 12 04:28:12 UTC 2018

sysadmin@localhost:~$ ls
Desktop Documents Downloads Music
Pictures Public Templates Videos

sysadmin@localhost:~$ cal 05 2030
```
*(calendar of May (5) month year 2030)*

```text
                    May 2030
su  mo  tu  we  th  fr  sa
                       1   2   3   4
 5   6   7   8   9  10  11
12  13  14  15  16  17  18
19  20  21  22  23  24  25
26  27  28  29  30  31

sysadmin@localhost:~$ history
    1   date
    2   ls
    3   cal 05 2030
    4   history
```
*(commands history numbered from first to last based on execution)*

- If the desired command is in the list that the history command generates, it can be executed by typing an exclamation point ! character and then the number next to the command. For example, to execute the cal command again:

```text
sysadmin@localhost:~$ !3
cal 5 2030

                    May 2030
su  mo  tu  we  th  fr  sa
                       1   2   3   4
 5   6   7   8   9  10  11
12  13  14  15  16  17  18
19  20  21  22  23  24  25
26  27  28  29  30  31
```

- If the history command is passed a number as an argument, it outputs that number of previous commands from the history list. For example, to show the last three commands:

```text
sysadmin@localhost:~$ history 3
    6   date
    7   ls /home
    8   history 3
```

- To execute the nth command from the bottom of the history list, type !-n and hit Enter. For example, to execute the third command from the bottom of the history list execute the following:

```text
sysadmin@localhost:~$ !-3
date
Wed Dec 12 04:31:55 UTC 2018
```
- To execute the most recent command type !! and hit Enter.

```text
sysadmin@localhost:~$ date
Wed Dec 12 04:32:36 UTC 2018

sysadmin@localhost:~$ !!
date
Wed Dec 12 04:32:38 UTC 2018
```
- To execute the most recent iteration of a specific command, type ! followed by the name of the command and hit Enter. For example, to execute the most recent ls command:

```text
sysadmin@localhost:~$ !ls
ls /home
sysadmin
```

### 5.4 Variables
- A variable is a feature that allows the user or the shell to store data.
- this data can be used to provide critical system information or to change the behaviour of how the Bash shell (or other commands) work. variables are given names and stored temporarily in memory. there are two types of variables used in the bash shell : local and environment.

#### 5.4.1 local variables
- local or shell variables exist only in the current shell, and cannot affect other commands or applications. when the user closes a terminal window or shell, all of the variable are lost.
- They are often associated with user-based tasks and are lowercase by convention.
- To set the variable value, use the following assignment expression. If the variable already exists, the value of the variable is modified. If the variable name does not already exist, the shell creates a new local variable and sets the value:

```text
[ variable = value ]
```

- the following example creates a local variable named variable1 and assign it's a value of something :

```text
sysadmin@localhost:~$ variable1='something'
```
- the echo command is used to display output in the terminal. to display value of the variable, use a dollar sign $ character followed by the variable name as an argument to the echo command:

```text
sysadmin@localhost:~$ echo $variable1
> something
```

#### 5.4.2 Environment variables
- Environment variables, also called global variables, are available system-wide, in all shells used by Bash when interpreting commands and performing tasks.
- the system automatically recreates environment variables when a new shell is opened. example includes the PATH, HOME and HISTSIZE variables. the HISTSIZE variable defines how many previous commands to store in the history list. the command in the example below displays the value of the HISTSIZE variable :

```text
sysadmin@localhost:~$ echo $HISTSIZE
> 1000
```

- to modify the value of an existing variable, use the assignment expression :

```text
sysadmin@localhost:~$ HISTSIZE=500
sysadmin@localhost:~$ echo $HISTSIZE
> 500
```

- many variables are available for the Bash shell, as well as variables that affect different linux commands. A discussion of all variables is beyond the scope of this chapter; however, more shell variables will be covered as this course progresses.
- when run without arguments, the env command outputs a list of the environment variables. Because the output of the env command quite long, the following example use a text search to filter that output.
- in a previous example variable1 was created as a local variable, so the following search in the environment variable results in no output.

```text
sysadmin@localhost:~$ env | grep variable1
```

- the pipe character (|) passes the output of the env command to the grep command, which searches the output.
- Note: This text filtering technique will be covered in detail later in the course.
- the export command is used to turn a local variable into an environment variable.

```text
[ export variable ]
```

- After exporting variable1, it is now an environment variable. It is now found in the search through the environment variables :

```text
sysadmin@localhost:~$ export variable1
sysadmin@localhost:~$ env | grep variable1
> variable1=something
```

- the export command can also be used to make a variable an environment variable upon its creation by using the assignment expression as the argument:

```text
sysadmin@localhost:~$ export variable2='Else'
sysadmin@localhost:~$ env | grep variable 2
> variable2=Else
```

- to change the value of an environment variable, use the assignment expression:

```text
sysadmin@localhost:~$ variable1='$variable1' '$variable2'
sysadmin@localhost:~$ echo $variable1
> something Else
```

- Exported variables can be removed using the unset command:

```text
[ sysadmin@localhost:~$ unset variable2 ]
```

#### 5.4.3 PATH Variable
- One of the most important Bash shell variables to understand is the PATH variables. It contains a list that defines which directories the shell looks in to find commands.
- If a valid command is entered and the shell returns a "command not found" error, it is because the Bash shell was unable to locate a command by that name in any of the directories included in the PATH. The following command displays the PATH of the current shell:

```text
sysadmin@localhost:~$ echo $PATH
> /home/sysadmin/bin:/usr/local/sbin:
/usr/local/bin:/usr/sbin:/usr/bin:/sbin:
/bin:/usr/games
```
*(this the directories where you find commands inside the $PATH variable.)*

- Each directory in the list is seperated by a colon : character. Based on the preceding output, the PATH contains the following directories. The shell will check the directories in the order they are listed.

```text
/home/sysadmin/bin
/usr/local/sbin
/usr/local/bin
/usr/sbin
/usr/bin
/sbin
/bin
/usr/games
```

- Each of these directories is represented by a path. A path is a list of directories seperated by the / character. If you think of the filesystem as a map, paths are the directory addresses, which include step-by-step navigation directions; they can be used to indicate the location of any file within the system. For example, /home/sysadmin is a path to the home directory.
- If the command is not found in any directory listed in the PATH variable, the shell returns an error:

```text
sysadmin@localhost:~$ zed
> bash: zed: command not found
```

- If the custom software is installed on the system it may be necessary to modify the PATH to make it easier to execute these commands. For example, the following will add and verify the /usr/bin/custom directory to the PATH variable:

```text
sysadmin@localhost:~$ PATH = /usr/bin/custom : $PATH
sysadmin@localhost:~$ echo $PATH
> /usr/bin/custom:/home/sysadmin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games
```

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Command Line Skills & Introduction
![Handwritten notes on command line skills and introduction](./assets/handwritten-notes-1.jpg)

### Image 2: Shell & Bash Features
![Handwritten notes on shell and bash features](./assets/handwritten-notes-2.jpg)

### Image 3: Variables & Prompt Structure
![Handwritten notes on variables and prompt structure](./assets/handwritten-notes-3.jpg)

### Image 4: Commands & Arguments
![Handwritten notes on commands and arguments](./assets/handwritten-notes-4.jpg)

### Image 5: Arguments & Multiple Directories
![Handwritten notes on arguments and multiple directories](./assets/handwritten-notes-5.jpg)

### Image 6: Options
![Handwritten notes on options](./assets/handwritten-notes-6.jpg)

### Image 7: Options (ls -l, ls -r)
![Handwritten notes on ls -l and ls -r](./assets/handwritten-notes-7.jpg)

### Image 8: Combined Options & Human Readable
![Handwritten notes on combined options and human readable](./assets/handwritten-notes-8.jpg)

### Image 9: Single vs Full-word Options & History
![Handwritten notes on single vs full-word options and history](./assets/handwritten-notes-9.jpg)

### Image 10: History Navigation & Calendar
![Handwritten notes on history navigation and calendar](./assets/handwritten-notes-10.jpg)

### Image 11: History Command Execution
![Handwritten notes on history command execution](./assets/handwritten-notes-11.jpg)

### Image 12: Advanced History & Variables
![Handwritten notes on advanced history and variables](./assets/handwritten-notes-12.jpg)

### Image 13: Local Variables
![Handwritten notes on local variables](./assets/handwritten-notes-13.jpg)

### Image 14: Echo Command & Environment Variables
![Handwritten notes on echo command and environment variables](./assets/handwritten-notes-14.jpg)

### Image 15: Env, Grep, and Export
![Handwritten notes on env, grep, and export](./assets/handwritten-notes-15.jpg)

### Image 16: Export, Unset, and Variable Modification
![Handwritten notes on export, unset, and variable modification](./assets/handwritten-notes-16.jpg)

### Image 17: PATH Variable & Command Not Found
![Handwritten notes on PATH variable and command not found](./assets/handwritten-notes-17.jpg)

### Image 18: PATH Modification
![Handwritten notes on PATH modification](./assets/handwritten-notes-18.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 05)
| Command | Description | Example |
| :--- | :--- | :--- |
| `history` | Show command history | `history` |
| `alias` | Create command shortcut | `alias ll='ls -la'` |
| `ls` | List directory contents | `ls /etc/ppp` |
| `cal` | Display a calendar | `cal 05 2030` |
| `date` | Display current date/time | `date` |
| `env` | Display environment variables | `env` |
| `export` | Set environment variable | `export variable` |
| `unset` | Remove environment variable | `unset variable` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)
