# Module 03: Working in Linux

> **Course:** NDG Linux Essentials  
> **Status:** 🔄 In Progress  
> **Objective:** Understand the Linux desktop environment, CLI navigation, and application architecture.

---

## 📖 Lesson 3: Working in Linux

### 3.1 Navigating the Linux Desktop
- To be a Linux system administrator, it is necessary to be comfortable with linux as a desktop operating system and have proficiency with basic information and communication technology (ICT) skills.
- Using linux for productivity tasks, rather than depending on windows or Macintosh systems, accelerates learning by working with linux tools on a daily basis.
- systems administrators do far more than manage servers; they are often called upon to assist users with configuration issues, recommending new software, and update documentation among other tasks.
- Most linux distribution allow users to download a "desktop" installation package that can be loaded onto a USB key. This one of the first things aspiring system administrators should do; download a major distribution and load it onto an old PC. This process is fairly straigtforward, and tutorials are available online.
- The linux desktop should be familiar to anyone who has used a PC or Macintosh with icons to select different programs and a "settings" application to configure things like user accounts, wifi networks, and input devices. After familiarizing oneself with the linux Graphical User Interface (GUI), or desktop, the next step is learning how to perform tasks from the command line.

#### 3.1.1 Getting to know the command line
- The command line interface (CLI) is a simple text input system for entering anything from single word commands to complicated scripts.
- Most Operating systems have a CLI that provides a direct way of accessing and controlling the computer.
- On systems that boot to a GUI, there are two common ways of accessing the command line - a GUI-based terminal, and a virtual terminal.
  - A GUI terminal is a program within the GUI environment that emulates a terminal window. GUI terminals can be accessed through the menu system. For example, on a CentOS machine, you could click on Applications on the menu bar, then System Tools > and, finally Terminal. If you have search tools, you can search for terminal.
  - A virtual terminal can be run at the same time as a GUI but requires the user to log in via the virtual terminal before they can execute commands (as they would before accessing the GUI interfaces).
- Each linux desktop distribution is slightly different, but the application terminal or x-term will open a terminal window from the GUI - while there are subtle differences between the terms console and terminal window sessions, they are all the same from an administrators standpoint and require the same knowledge of commands to use.
- ordinary command line tasks are starting programs, parsing scripts, and editing text files used for system or application configuration. Most servers boot directly to a terminal, as a GUI can be resource intensive and is generally not needed to perform server based operations.

### 3.2 Applications
- the kernel of the operating system is like an air traffic controller at an airport, and the applications are the airplanes under its control. the kernel decides which program gets which blocks of memory, it starts and kills applications, and it handles displaying text or graphics on a monitor.
- Applications make requests to the kernel and in return receive resources, such as memory, CPU, and disk space. If two applications request the same resource, the kernel decides which one gets it, and in some cases, kills off another application to save the rest of the system and prevent a crash.
- the kernel also abstracts some complicated details away from the application. For example, the application doesn't know if a block of disk storage is on a solid-state drive, a spinning metal hard disk, or even a network file share.
- Applications need only follow the kernel's Application Programming Interface (API) and therefore don't have to worry about the implementation details. Each application behave as if it has a large block of memory on the system; the kernel maintains this illusion by remapping smaller blocks of memory, sharing blocks of memory with other applications, or even swapping out untouched blocks to disk.
- the kernel also handles the switching of applications, a process known as multitasking. A computer system has a small number of Central Processing Unit (CPU) and a finite amount of memory.
- the kernel takes care of unloading task and loading a new one if there is more demand than resources available. when one task has run for a specified amount of time, the CPU pauses it so that another may run. If the computer is doing several tasks at once, the kernel is deciding when to switch focus between tasks, with the tasks rapidly switching, it appears that the computer is doing many things at once.
- when we, as users, think of applications, we tend to think of word processors, web browsers, and email clients, however, there are large variety of application types.
- the kernel doesn't differentiate between a user-facing application, a network service that talks to a remote computer, or an internal task. From this, we get an abstraction called a Process.
- A process is just one task that is loaded and tracked by the kernel. An application may even need multiple processes to function, so the kernel takes care of running the processes, starting and stopping them as requested, and handing out system resources.

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Navigating the Linux Desktop
![Handwritten notes on navigating the Linux desktop](./assets/handwritten-notes-1.jpg)

### Image 2: Getting to Know the Command Line
![Handwritten notes on getting to know the command line](./assets/handwritten-notes-2.jpg)

### Image 3: Virtual Terminals & Applications
![Handwritten notes on virtual terminals and applications](./assets/handwritten-notes-3.jpg)

### Image 4: Applications & The Kernel
![Handwritten notes on applications and the kernel](./assets/handwritten-notes-4.jpg)

### Image 5: Multitasking & Processes
![Handwritten notes on multitasking and processes](./assets/handwritten-notes-5.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 03)
| Command | Description | Example |
| :--- | :--- | :--- |
| `ls` | List directory contents | `ls -la` |
| `cd` | Change directory | `cd /home/sysadmin` |
| `pwd` | Print working directory | `pwd` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)