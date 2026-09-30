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

#### 3.2.1 Major Applications
- the Linux kernel can run a wide variety of software across many hardware platforms. A computer can act as a server, which means it primarily handles data on others' behalf, or as a desktop, which means a user interface interacts with it directly.
- the machine can run software or be used as a development machine in the process of creating software. A machine can even adopt multiple roles as Linux makes no distinction; it's merely a matter of configuring which applications run.
- One resuliting advantage is that Linux can simulate almost all aspects of a production environment, from development to testing, to verification on scaled-down hardware, which saves costs and time.
- A Linux administrator could run the same server applications on a desktop or inexpensive virtual server that are run by large internet service providers. Of course, a desktop would not be able to handle the same volume as a major provider would, but almost any configuration can be simulated without needing powerful hardware or server licensing.
- Linux software generally falls into one of three categories:
  - **server applications**
    - software that has no direct interaction with the monitor and keyboard of the machine it runs on. Its purpose is to serve information to other computers, called clients. sometimes server applications may not talk to other computers but only sit there and crunch data.
  - **Desktop Applications**
    - Web browsers, text editors, music players, or other applications with which users interact directly.
    - In many cases, such as a web browser, the application is talking to a server on the other end and interpreting the data. This is the "client" side of a client/server application.
  - **tools**
    - A loose category of software that exists to make it easier to manage computer systems. tools can help configure displays, provide a Linux shell that users type commands into, or even more sophisticated tools, called compilers, that convert source code to application programs that the computer can execute.
- the availability of applications varies depending on the distribution. Often application vendors choose a subset of distributions to support. Different distributions have different versions of key libraries, and it is difficult for a company to support all these different versions. some applications, however, like Firefox and LibreOffice are widely supported and available for all major distributions.
- the Linux community has come up with lots of creative solutions for both desktop and server applications. These applications, many of which make up the backbone of the Internet, are critical to understanding, and utilizing the power of Linux.
- Most computing tasks can be accomplished by any number of applications in Linux. There are many web browsers, web servers, database servers, and text editors from which to choose.
- Evaluating application software is an important skill to be learned by the aspiring Linux administrator. Determining requirements for performance, stability, and cost are just some of the considerations needed for a comprehensive analysis.

#### 3.2.2 Server Applications
- Linux excels at running server applications because of its reliability and efficiency. The ability to optimize server operating systems with just needed components allows administrators to do more with less, a feature loved by startups and large enterprise alike.

##### 3.2.2.1 Web servers
- One of the early uses of Linux was for web servers. A web server hosts content for web pages, which are viewed by a web browser using the hypertext transfer protocol (HTTP) or its encrypted flavor, HTTPS.
- the web page itself can either be static or dynamic. when the web browser requests a static page, the web server sends the file as it appears on disk. In the case of a dynamic site, the request is sent by the web server to an application, which generates the content.
- WordPress is one popular example. Users can develop content through their browser in the WordPress application, and the software turns it into a fully functional dynamic website.
- Apache is the dominant web server in use today. Apache was originally a standalone project, but the group has since formed the Apache Software Foundation and maintains over a hundred open source software projects.
- Apache HTTPD is the daemon, or server application program, that "serves" web page requests.
- Another web server is NGINX, which based out of Russia. It focuses on performance by making use of more modern UNIX kernels and only does a subset of what Apache can do.
- "Over 65% of websites are powered by either NGINX or Apache."

##### 3.2.2.2 Private cloud servers
- As individuals, organizations, and companies start to move their data to the cloud, there is a growing demand for private cloud server software that can be deployed and administered internally.
- The ownCloud project was launched in 2010 by Frank Karlitschek to provide software to store, sync and share data from private cloud servers.
- It is available in a standard open source GNU AGPLv3 license and an enterprise version that carries a commercial license.
- The Nextcloud project was forked from ownCloud in 2016 by Karlitschek and has been growing steadily since then.
- It is provided under a GNU AGPLv3 and aims for "an open, transparent development process."
- Both projects focus on providing private cloud software that meets the needs of both large and small organizations that require security, privacy, and regulatory compliance.
- While several other projects aim to serve the same users, these two are by far the largest in terms of both deployment and project members.

##### 3.2.2.3 Database servers
- Database server applications form the backbone of most online services. Dynamic web applications pull data from and write data to these applications, for example, a web program for tracking online students might consist of a front-end server that presents a web form. when data is entered into the form, it is written to a database application such as MariaDB, when instructors need to access student information, the web application queries the database and returns the results through the web application.
- MariaDB is a community-developed fork of the MySQL relational database management system. It is just one of many database servers used for web development as different requirements dictate the best application for the required tasks.
- A database stores information and also allows for easy retrieval and querying. some other popular databases are Firebird and PostgreSQL. You might enter raw sales figures into the database and then use a language called Structured Query Language (SQL) to aggregate sales by product and date to produce a report.

##### 3.2.2.4 Email servers
- Email has always been a widespread use for Linux servers. when discussing email servers, it is always helpful to look at the 3 different tasks required to get email between people:
  - **Mail Transfer Agent (MTA)**
    - The most well known MTA (software that is used to transfer electronic messages to other systems) is Sendmail. Postfix is another popular one and aims to be simpler and more secure than sendmail.
  - **Mail Delivery Agent (MDA)**
    - Also called the local delivery agent, it takes care of storing the email in the user's mailbox. Usually invoked from the final MTA in the chain.
  - **POP/IMAP server**
    - The post office Protocol (POP) and internet message access Protocol (IMAP) are two communication protocols that let an email client running on your computer talk to a remote server to pick up the email.
    - Dovecot is a popular POP/IMAP server owing to its ease of use and low maintenance.
- Cyrus IMAP is another option. some POP/IMAP servers implement their own mail database format for performance and invoke the MDA if the custom database is desired. People using standard file formats (such as all the emails ie in one text file) can choose any MDA.
- There are several significant differences between the closed source and open source software worlds, one being that of inclusion of other projects as components to a projector package.
- in the closed source world, Microsoft Exchange is shipped primarily as a software package/suite that includes all the necessary or approved components, all from microsoft, so there are few if any options to make individual selections.
- in the open source world, many options can be modularly included or swapped out for package components, and indeed some software packages or suites are just a well-packaged set of otherwise individual components all harmoniously working together.

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

### Image 6: Major Applications
![Handwritten notes on major applications](./assets/handwritten-notes-6.jpg)

### Image 7: Application Categories
![Handwritten notes on application categories](./assets/handwritten-notes-7.jpg)

### Image 8: Application Availability & Evaluation
![Handwritten notes on application availability and evaluation](./assets/handwritten-notes-8.jpg)

### Image 9: Server Applications & Web Servers
![Handwritten notes on server applications and web servers](./assets/handwritten-notes-9.jpg)

### Image 10: Apache & NGINX
![Handwritten notes on Apache and NGINX](./assets/handwritten-notes-10.jpg)

### Image 11: Private Cloud Servers
![Handwritten notes on private cloud servers](./assets/handwritten-notes-11.jpg)

### Image 12: Database Servers
![Handwritten notes on database servers](./assets/handwritten-notes-12.jpg)

### Image 13: Email Servers
![Handwritten notes on email servers](./assets/handwritten-notes-13.jpg)

### Image 14: Email Servers & Open Source
![Handwritten notes on email servers and open source](./assets/handwritten-notes-14.jpg)

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