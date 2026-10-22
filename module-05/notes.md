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

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Command Line Skills & Introduction
![Handwritten notes on command line skills and introduction](./assets/handwritten-notes-1.jpg)

### Image 2: Shell & Bash Features
![Handwritten notes on shell and bash features](./assets/handwritten-notes-2.jpg)

### Image 3: Variables & Prompt Structure
![Handwritten notes on variables and prompt structure](./assets/handwritten-notes-3.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 05)
| Command | Description | Example |
| :--- | :--- | :--- |
| `history` | Show command history | `history` |
| `alias` | Create command shortcut | `alias ll='ls -la'` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)