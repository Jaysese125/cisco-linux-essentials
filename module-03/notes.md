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

##### 3.2.2.5 File sharing
- For windows-centric file sharing, samba is the clear winner. samba allows a Linux machine to look and behave like a windows machine so that it can share files and participate in a windows domain. samba implements the server components, such as making files available for sharing and certain windows server roles, and also the client end so that a Linux machine may consume a windows file share.
- The netatalk project lets a Linux machine perform as an Apple Macintosh file server. the native file sharing protocol for UNIX/Linux is called the Network File System (NFS).
- NFS is usually part of the kernel which means that a remote file system can be mounted (made accessible) just like a regular disk, making file access transparent to other applications.
- As computer network becomes more substantial, the need for a directory increases. One of the oldest network directory systems is the Domain Name System (DNS). it is used to convert a name like https://www.icann.org/ to an IP address like 192.0.43.7, which is a unique identifier of a computer on the internet. DNS also holds global information like the address of the MTA for a given domain name.
- An organization may want to run their own DNS server to host their public facing names, and also to serve as an internal directory of services. the Internet Software Consortium maintains the most popular DNS server, simply called bind after the name of the process that runs the service.
- the DNS is focused mainly on computer names and IP addresses and is not easily searchable. Other directories have sprung up to store information such as user accounts and security roles.
- The lightweight Directory Access Protocol (LDAP) is one common directory system which also powers Microsoft's Active directory. In LDAP, an object is stored in a tree, and the position of that object on the tree can be used to derive information about the object and what it stores.
- For example, a Linux administrator may be stored in a branch of tree called "IT Department," which is under a branch called "Operations." thus one can find all the technical staff by searching under the "IT Department" branch. OpenLDAP is the dominant program used in Linux infrastructure.
- One final piece of network infrastructure to discuss here is called the Dynamic Host Configuration Protocol (DHCP). when a computer boots up, it needs an IP address for the local network so it can be uniquely identified.
- DHCP's job is to listen for requests and to assign a free address from the DHCP pool. the internet system consortium (known until January 2004 as the Internet software consortium) also maintains the ISC DHCP server, which is the most common open source DHCP server.

#### 3.2.3 Desktop Applications
- the Linux ecosystem has a wide variety of desktop applications. There are games, productivity applications, creative tools, web browser and more.

##### 3.2.3.1 Email
- the mozilla foundation came out with thunderbird, a full-featured desktop email client. thunderbird connects to a POP or IMAP server, displays email locally, and sends email through an external SMTP server.
- Other notable email clients are Evolution and Kmail which are the GNOME and KDE projects email clients.

##### 3.2.3.2 Creative
- standardization through POP and IMAP and local email formats means that it's easy to switch between email clients without losing data.
- For creative types, there is Blender, GIMP (GNU Image Manipulation Program), and Audacity which handle 3D movie creation, 2D image manipulation, and audio editing respectively. They have had various degrees of success in professional markets. Blender is used for everything from independent films to Hollywood movies, for example.
- GIMP supports high quality photo manipulation, original artwork creation, graphic design elements, and is extensible through scripting in multiple languages.
- Audacity is a free and open source audio editing tool that is available on multiple operating systems.

##### 3.2.3.3 Productivity
- Use of common open source applications in presentations and projects is one way to strengthen linux skills. the basic productivity applications, such as a word processor, spreadsheet, and presentation package are valuable assets.
- collectively they're known as an office suite, primarily due to Microsoft Office, the dominant player in the market.
- LibreOffice is a fork of the OpenOffice (sometimes called OpenOffice.org) application suite. Both offer a full office suite, including tools that strive for compatibility with Microsoft Office in both features and file formats.
- The spreadsheet editor of LibreOffice, LibreOffice Calc, is not limited to rows and columns of numbers.
- The numbers can be the source of a graph, and formulas can be written to calculate values based on information, such as pulling together interest rates and loan amounts to help compare different borrowing options.
- Using LibreOffice Writer, the document editor of LibreOffice, a document can contain text, graphics, data tables, and much more. you can link documents and spreadsheets together, for example, so that you can summarize data in a written form and know that any changes to the spreadsheet will be reflected in the document.
- LibreOffice can also work with other file formats, such as Microsoft Office or Adobe Portable Document Format (PDF) files. Additionally, through the use of extensions, LibreOffice can be made to integrate with wiki software to give you a powerful intranet solution.

##### 3.2.3.4 Web Browsers
- Linux is a first class citizen for the Mozilla Firefox and Google Chrome browsers. Both are open source web browsers that are fast, feature-rich, and have excellent support for web developers.
- These packages are an excellent example of how competition helps to drive open source development - improvements made to one browser spur the development of the other browser.
- As a result, the internet has two excellent browsers that push the limits of what can be done on the web, and work across a variety of platforms. using a browser, while second nature for many, can lead to privacy concerns. By understanding and modifying the configuration options, one can limit the amount of information they share while searching the web and saving content.

### 3.3 Console Tools
- Historically, the development of UNIX shows considerable overlap between the skills of software development and systems administration. the tools for managing systems have features of computer languages such as loops (which allow commands to be carried out repeatedly), and some computer programming languages are used extensively in automating systems administration tasks. Thus, one should consider these skills complementary, and at least a basic familiarity with programming is required for competent systems administrators.

#### 3.3.1 Shells
- At the basic level, users interact with a linux system through a shell whether connecting to the system remotely or from an attached keyboard. the shell's job is to accept commands, like file manipulations and starting applications, and to pass those to the linux kernel for execution.
- the linux shell provides a rich language for iterating over files and customizing the environment, all without leaving the shell. For example, it is possible to write a single command line that find files with contents matching a specific pattern, extracts useful information from the file, then copies the new information to a new file.
- linux offers a variety of shells to choose from, mostly differing in how and what can be customized, and the syntax of the built-in scripting language. the two main families are the Bourne shell and the C shell. the Bourne shell was named after its creator Stephen Bourne of Bell Labs. the C shell was so named because its syntax borrows heavily from the C language. As both these shells were invented in the 1970s, there are more modern versions, the Bourne Again Shell (Bash) and the tcsh (pronounced tee-cee-shell). Bash is the default shell on most systems, though tcsh is also typically available.
- Programmers have taken favourite features from Bash and tcsh and made other shells, such as the Korn shell (ksh) and the Z shell (zsh). the choice of shells is mostly a personal one; users who are comfortable with Bash can operate effectively on most linux systems. other shells may offer features that increase productivity in specific use cases.

#### 3.3.2 Text Editors
- Most linux systems provide a choice of text editors which are commonly used at the console to edit configuration files. the two main applications are Vi (or the more modern Vim) and Emacs.
- both are remarkably power tools to edit text files; they differ in the format of the commands and how plugins are written for them. Plugins can be anything from syntax highlighting of software projects to integrated calendars.
- both Vi and Emacs are complex and have a steep learning curve, which is not helpful for simple editing of a small text file. therefore, Pico and nano are available on most systems and provide very basic text editing.

> **Consider this**
> the nano editor was developed as a completely open source editor that is loosely based on Pico, as the license for Pico is not an open source license and forbids making changes and altering it.
> while nano is simple and easy to use, it doesn't offer the extensive suite of more advanced editing and key binding features that an editor like vi does. Administrators should strive to gain some basic familiarity with vi, though, because it is available on almost every linux system in existence.

### 3.4 Package Management

#### 3.4.1 Debian Package Management
- The Debian distribution, and its derivatives such as Ubuntu and Mint, use the Debian Package Management System. At the heart of Debian Package management are software packages that are distributed as files ending in the .deb extension.
- the lowest-level tool for managing these files in the dpkg command. This command can be tricky for novice Linux users, so the Advanced Package Tool, apt-get (a front-end program to the dpkg tool), makes management of packages easier.
- Additional command line tools which serve as front-ends to dpkg include aptitude and GUI front-ends like synaptic and software center.

#### 3.4.2 RPM Package Management
- the linux standards base, which is a linux foundation project, is designed to specify (through a consensus) a set of standards that increase the compatibility between conforming Linux systems.
- According to the Linux Standards Base, the standard package management system is RPM.
- RPM makes use of an .rpm file for each software package. This system is what distributions derived from Red Hat, including CentOS and Fedora, use to manage software. several other distributions that are not Red Hat derived, such as SUSE, openSUSE, and Arch, also use RPM.
- Like the Debian system, RPM Package Management systems track dependencies between packages. Tracking dependencies ensures that when a package is installed, the system also installs any packages needed by that package to function correctly. Dependencies also ensure that software updates and removals are performed properly.
- the back end tool most commonly used for RPM package Management is the rpm command. While the rpm command can install, update, query and remove packages, the command line front-end tools such as yum and updater outsource the process of resolving dependency issues.
- Note: A back end program or application either interacts directly with a front-end program or is 'called' by an intermediate program. Back end programs would not interact directly with the user. Basically, there are programs that interact with people (front end) and programs that interact with other programs (back-end).
- There are also GUI-based front-end tools such as yumex and GNOME PackageKit that also make RPM package management easier.
- Some RPM-based distributions have implemented the Zypp (or libzypp) package management style, mostly openSUSE and SUSE Linux Enterprise, but mobile distributions Meego, Tizen and Sailfish as well.
- The zypper command is the basis of the Zypp method, and it features short and long English commands to perform functions, such as zypper in packagename which installs a package including any needed dependencies.
- Most of the commands associated with package management require root privileges. The rule of thumb is that if a command affects the state of a package, administrative access is required.
- In other words, a regular user can perform a query or a search, but to add, update, or remove a package requires the command to be executed as the root user.

### 3.5 Development Languages
- It should come as no surprise that as software built on contributions from programmers, Linux has excellent support for software development. The shells are built to be programmable, and there are powerful editors included on every system, There are also many development tools available, and many modern programming languages treat Linux as a first-class citizen.
- Computer programming languages provide a way for a programmer to enter instructions in a more human readable format, and for those instructions to eventually becomes translated into something the computer understands.
- languages fall into one of two camps: interpreted or compiled. An interpreted language translates the written code into computer code as the program runs, and a compiled language is translated all at once.
- Unix itself was written in a compiled language called C. the main benefit of C is that the language itself maps closely to the generated machine code so that a skilled programmer can write code that is small and efficient. when computer memory was measured in kilobytes, this was very important. Even with large memory sizes today, C is still helpful for writing code that must run fast, such as an operating system.
- C has been extended over the years. there is C++, which adds object support to C (a different style of programing), and Objective C that took another direction and is in heavy use in Apple products.
- The Java language puts a different spin on the compiled approach. Instead of compiling to machine code, Java first imagines a hypothetical CPU called the Java Virtual Machine (JVM) and then compiles all the code to that. Each host computer runs JVM software to translate the JVM instructions (called bytecode) into native instructions.
- The additional translation with Java might make you think it would be slow. However, the JVM is relatively simple so it can be implemented quickly and reliably on anything from a powerful computer to a low power device that connects to a television. A compiled Java file can also be run on any computer implementing the JVM.
- Another benefit of compiling to an intermediate target is that the JVM can provide services to the application that usually wouldn't be available on a CPU.
- Allocating memory to a program is a complex problem, but it's built into the JVM. As a result, JVM makers can focus their improvements on the JVM as a whole, so any progress they make is instantly available to applications.
- Interpreted languages, on the other hand, are translated to machine code as they execute. The extra computer power spent doing this can often be recouped by the increased productivity the programmer gains by not having to stop working to compile.
- Interpreted languages also tend to offer more features than compiled languages, meaning that often less code is needed. The language interpreter itself is usually written in another language such as C, and sometimes even Java! This means that an interpreted language is being run on the JVM, which is translated at run time into actual machine code.
- Javascript is a high level interpreted programming language that is one of the core technologies on the world wide web.
- It is similar to but fundamentally different from Java, which is a completely object-oriented programming language owned by Oracle. Javascript is a cross-platform scripting language for adding interactive elements to web pages, that is in wide use across the internet. By using Javascript libraries, web programmers can add everything from simple animations to complex server-side applications for internet users. Javascript is continuously evolving to meet the functionality and security needs of internet users and is capable of being released under a GNU GPL license.

> **Consider this:**
> the term object-oriented refer to programming that abstract complex actions and processes so that the end user only deals with basic tasks. to visualize this concept, think of a machine that performs a complex set of tasks by simply pushing a button.

- Perl is an interpreted language. Perl was originally developed to perform text manipulation. Over the years, it gained favor with systems administrators and continues to be improved and used in everything from automation to building web applications.
- PHP is a language that was initially built to create dynamic web pages. A PHP file is read by a web server such as Apache. Special tags in the file indicate that parts of the code should be interpreted as instructions. the web server pulls all the different parts of the file together and sends it to the web browser. PHP's main advantages are that it is easy to learn and available on almost any system. Because of this, many popular projects are built on PHP. notable examples include wordpress (for blogging), cacti (for monitoring), and even parts of facebook.
- Ruby is another language that was influenced by Perl and shell, along with many other languages. It makes complex programming tasks relatively easy, and with the inclusion of the Ruby on rails framework, is a popular choice for building complex web applications.
- Ruby is also the language that powers many of the leading automation tools like chef and puppet, which makes processing abilities and is a favorite in automating managing a large number of linux systems much simpler.
- Python is another scripting language that is is general use. much like Ruby It makes complex tasks easier and has a framework called Django that makes building web applications very easy. Python has excellent statistical processing abilities and is a favorite in academia.
- A computer programming language is just a tool that makes it easier to tell the computer what you want it to do. A library bundles common tasks into a distinct packages that can be used by the developer.
- ImageMagick is one such library that lets programmers manipulate images in code. Image Magick also ships with some command line tools that enable programmers to process images from a shell and take advantage of the scripting capabilities there.
- OpenSSL is a cryptographic library that is used in everything from web servers to the command line. It provides a standard interface for adding cryptography into a perl script for example. At much lower level is the c library. the c library provides a basic set of functions for reading and writing to files and displays, and used by applications and other languages alike.

### 3.6 Security
- Administrators and computer users are increasingly aware of privacy concerns in both their personal and professional lives. High-profile data breaches have been in the news all too often recently, and the cost of these break-ins can reach into the millions of dollars for the institutions that fall victim to hackers and ransomware attacks. Many times the cause of these breaches is simply human error such as opening a suspicious email or entering a password into a phony login page.
- cookies are the primary mechanism that websites use to track you. sometimes this tracking is good, even as to keep track of what is in your shopping cart or to keep you logged in when you return to the site.
- As you browse the web, a web server can send back the cookie, which is a small piece of text, along with the web page. Your browser stores this information and sends it back with every request to the same site. cookies are normally only sent back to the site they originated from, so a cookie from example.com wouldn't be sent to example.org.
- However, many sites have embedded scripts that come from third parties, such as a banner advertisement or google analytics pixel. If both example.com and example.org have a tracking pixel, such as one from an advertiser, then the same cookie will be sent when browsing both sites, the advertiser then knows that you have visited both example.com and example.org.
- With a broad enough reach, such as placement on social network sites with "Like" buttons and such, a website can gain an understanding of which websites you frequent and figure out your interests and browsing habits.
- there are various strategies for dealing with this. One is to ignore it. the other is to limit the tracking pixels you accept, either by blocking them entirely or clearing them out periodically.
- Browsers typically offer cookie-related settings; users can opt to have the browser tell the site not to track. This voluntary tag is sent in the request, and some site will honor it. The browser can also be set never to remember third-party cookies and remove regular cookies (such as from the site you are browsing) after being closed.
- tweaking privacy settings can make you more anonymous on the internet, but it can also cause problems with some sites that depend on third-party cookies. If this happens, you might have to explicitly permit some cookies to be saved.
- Browsers also offer a private or incognito mode where cookies and tracking pixels are deleted upon exiting the window. This mode can be helpful if you would like to search for something without letting other websites know what you are looking for.

#### 3.6.1 Password issues
- Good password management is essential to security in any computing environment. the linux systems administrator is often the person responsible for setting and enforcing password policies for users at all levels. The most privileged user on any linux system is root, this account is the primary administrator and is created when the operating system is installed. often administrators will disable root access as the first line of defense against intrusion since computer hackers will try to gain root access in order to take control of the system.
- there are many levels of access and various means of password management on a linux system. when users are created, they are given different login permissions depending on what groups they are assigned to. For example, administrators can create and manage users while regular users cannot. services that run on systems such as databases can also have login permissions with their own password and privileges. Additionally, there are specific passwords for accessing systems remotely through SSH, FTP, or other management programs.
- Managing all these accounts, and their accompanying passwords is a complicated and necessary part of the systems administrator role. Passwords need to be complex enough not to be easily guessed by hackers, yet easy to remember for users. Increasingly users and administrators are turning to password manager programs to store login credentials in encrypted form. Another trend is two-factor authentication (2FA), a technique where a password is supplemented by a second "factor", often a passcode sent to the user's phone or other devices. keeping up with current security trends, while ensuring authorized users' ease of access, is an ongoing challenge that must be met.

#### 3.6.2 Protecting yourself
- As you browse the web, you leave a digital footprint, much of this info goes ignored; some of it is gathered to collect statistics for advertising, and some can be used for malicious purposes.
- the easiest thing you can do is to use a good, unique password everywhere you go, especially on your local machine. A good password is at least 10 characters long and contains a mixture of numbers, letters (both upper and lower case) and special symbols.
- Use a password manager like KeePassX to generate passwords, and then you only need to have a login password to your machine and a password to open up your Keepass file.
- Also limit the information you give to sites to only what is needed. While giving your mother's maiden name and birthdate might help unlock your social network login if you lose your password, the same information can be used to impersonate you to your banks.
- After that, make a point of checking for updates periodically. the system can be configured to check for updates on a regular basis. If there are security-related upgrades, you may be prompted immediately to install them.
- Finally, you should protect your computer from accepting incoming connections. A firewall is a device that filters network traffic, and linux has one built-in. If you are using Ubuntu, then the gufw is a graphical interface to Ubuntu's uncomplicated firewall (ufw).
- Under the hood, you are using iptables which is the built-in firewall system. instead of entering complicated iptables commands, you see a GUI. while this GUI lets you build an effective policy for a desktop, it barely scratches the surface of what iptables can do.

#### 3.6.3 Privacy tools
- the use of modern privacy tools, both at the server and user level, can help prevent system intrusions and unauthorized access to data.
- the good news is that linux is by default one of the most secure operating systems ever created. Many of the exploits that plague other operating systems simply won't work on linux due to the underlying architecture. however, there are still many known weaknesses that hackers can take advantage of so the proactive systems administrator is wise to deploy privacy tools that protect their users as well as the systems they use.
- Encryption is probably the best-known and most widely-deployed privacy tool in use today. Administrators deploy encryption with authentication keys on almost every system that communicates with the outside world.
- one well-known example is the HyperText Transfer Protocol Secure (HTTPS) standard used on web servers to ensure that data transmitted between users and online resources cannot be intercepted as it travels on the open internet.
- Virtual Private Networks (VPN) have been in use by companies to connect their remote servers and employees for many years. Now they are gaining popularity amongst ordinary users looking to protect their privacy online. They work by creating an encrypted channel of communication between two systems, so the data transmitted between them is scrambled by an algorithm only the systems know.
- the tor project has long been involved in creating privacy tools like its Tor Browser that works by relaying internet requests through a network of servers that prevents websites and others from learning the identity of person making the request.
- These tools are constantly evolving and choosing which ones are appropriate for the users and systems involved is an essential part of the systems administrator's role.

### 3.7 The Cloud
- No doubt you've heard of the cloud, whether you're using Google Docs for your homework or storing music and photos on iCloud, you probably have at least some of your digital content hosted on a cloud server somewhere.
- Cloud computing has revolutionized the way we access technology. As internet connectivity and speeds have increased, it's become easier to move computing resources to remote locations where content can be accessed, manipulated and shared around the globe. Organizations are increasingly looking at the cloud as essential to their businesses and operations.
- The migration of an organization's IT applications and processes to cloud services, known as cloud adoption, is rapidly becoming a strategic business decision for many. With cloud adoption rising significantly all over the globe, cloud computing is not the catchphrase that it once was. Cloud computing is seen as one of the major disruptive technologies for the coming decade which will significantly transform businesses, economies, and lives globally.
- Physically, a cloud can be described as computing resources from one or many off-site data centers which can be accessed over the internet.
- The cloud builds on the benefits of a data center and provides computing solutions to organizations who need to store and process data, and it allows them to delegate management of IT infrastructure to a third-party.
- The data and resources that organizations store in the cloud can include data, servers, storage, application hosting, analytics and a myriad of other services.
- A cloud deployment model provides a basis for how cloud infrastructure is built, managed, and accessed.

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

### Image 15: File Sharing, DNS, LDAP & DHCP
![Handwritten notes on file sharing, DNS, LDAP and DHCP](./assets/handwritten-notes-15.jpg)

### Image 16: DNS, LDAP & OpenLDAP
![Handwritten notes on DNS, LDAP and OpenLDAP](./assets/handwritten-notes-16.jpg)

### Image 17: DHCP & Desktop Applications
![Handwritten notes on DHCP and desktop applications](./assets/handwritten-notes-17.jpg)

### Image 18: Creative Applications
![Handwritten notes on creative applications](./assets/handwritten-notes-18.jpg)

### Image 19: Productivity Applications
![Handwritten notes on productivity applications](./assets/handwritten-notes-19.jpg)

### Image 20: Web Browsers
![Handwritten notes on web browsers](./assets/handwritten-notes-20.jpg)

### Image 21: Console Tools & Shells
![Handwritten notes on console tools and shells](./assets/handwritten-notes-21.jpg)

### Image 22: Shells & Text Editors
![Handwritten notes on shells and text editors](./assets/handwritten-notes-22.jpg)

### Image 23: Text Editors & Nano
![Handwritten notes on text editors and nano](./assets/handwritten-notes-23.jpg)

### Image 24: Debian Package Management & RPM
![Handwritten notes on Debian package management and RPM](./assets/handwritten-notes-24.jpg)

### Image 25: RPM Package Management & Front-End Tools
![Handwritten notes on RPM package management and front-end tools](./assets/handwritten-notes-25.jpg)

### Image 26: Zypp Package Management & Root Privileges
![Handwritten notes on Zypp package management and root privileges](./assets/handwritten-notes-26.jpg)

### Image 27: Development Languages & C
![Handwritten notes on development languages and C](./assets/handwritten-notes-27.jpg)

### Image 28: C++, Java, and the JVM
![Handwritten notes on C++, Java, and the JVM](./assets/handwritten-notes-28.jpg)

### Image 29: Interpreted Languages & JavaScript
![Handwritten notes on interpreted languages and JavaScript](./assets/handwritten-notes-29.jpg)

### Image 30: JavaScript, Perl, and PHP
![Handwritten notes on JavaScript, Perl, and PHP](./assets/handwritten-notes-30.jpg)

### Image 31: PHP, Ruby, and Automation
![Handwritten notes on PHP, Ruby, and automation](./assets/handwritten-notes-31.jpg)

### Image 32: Python, ImageMagick, and OpenSSL
![Handwritten notes on Python, ImageMagick, and OpenSSL](./assets/handwritten-notes-32.jpg)

### Image 33: Security & Cookies
![Handwritten notes on security and cookies](./assets/handwritten-notes-33.jpg)

### Image 34: Third-Party Cookies & Tracking
![Handwritten notes on third-party cookies and tracking](./assets/handwritten-notes-34.jpg)

### Image 35: Privacy Settings & Password Issues
![Handwritten notes on privacy settings and password issues](./assets/handwritten-notes-35.jpg)

### Image 36: Password Management & 2FA
![Handwritten notes on password management and 2FA](./assets/handwritten-notes-36.jpg)

### Image 37: Protecting Yourself & Passwords
![Handwritten notes on protecting yourself and passwords](./assets/handwritten-notes-37.jpg)

### Image 38: Updates, Firewalls & Privacy Tools
![Handwritten notes on updates, firewalls and privacy tools](./assets/handwritten-notes-38.jpg)

### Image 39: Encryption, HTTPS, and VPNs
![Handwritten notes on encryption, HTTPS, and VPNs](./assets/handwritten-notes-39.jpg)

### Image 40: Tor Browser & The Cloud
![Handwritten notes on Tor Browser and the Cloud](./assets/handwritten-notes-40.jpg)

### Image 41: Cloud Adoption & Deployment Models
![Handwritten notes on cloud adoption and deployment models](./assets/handwritten-notes-41.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 03)
| Command | Description | Example |
| :--- | :--- | :--- |
| `ls` | List directory contents | `ls -la` |
| `cd` | Change directory | `cd /home/sysadmin` |
| `pwd` | Print working directory | `pwd` |
| `dpkg` | Debian package manager | `dpkg -i package.deb` |
| `apt-get` | Advanced Package Tool | `sudo apt-get install package` |
| `rpm` | RPM package manager | `rpm -ivh package.rpm` |
| `yum` | Yellowdog Updater Modified | `sudo yum install package` |
| `zypper` | Zypp package manager | `sudo zypper in package` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)