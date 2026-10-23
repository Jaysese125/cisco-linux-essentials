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

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 05)
| Command | Description | Example |
| :--- | :--- | :--- |
| `history` | Show command history | `history` |
| `alias` | Create command shortcut | `alias ll='ls -la'` |
| `ls` | List directory contents | `ls /etc/ppp` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)
