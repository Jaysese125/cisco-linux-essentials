# Module 04: Open Source Software and Licensing

> **Course:** NDG Linux Essentials  
> **Status:** 🔄 In Progress  
> **Objective:** Understand the history, philosophy, and mechanics of open source software and licensing.

---

## 📖 Lesson 4: Open Source Software and licensing

### 4.1 Introduction
- software projects take the form of source code, which is a human-readable set of computer instructions. since source code is not understood directly by the computer, it must be compiled into machine instructions by a compiler. the compiler is a special program that gathers all of the source code files and generates instructions that can be run on the computer, such as by the linux kernel.
- Historically, commercial software has been sold under a closed source license, meaning that users have the right to use the machine code, but cannot see the source code. Often the license explicitly states that users may not attempt to reverse engineer the machine code back to source code to figure out what it does.

> **consider this:**
> source code compiled into binary programs is one method of creating programs and running computing instructions. another is the many types of interpreted languages, such as PERL, Python and even BASH scripting, where the code is not compiled, but fed to an interpreting program, typically a binary executable that understands and implements the instructions contained in the source code or scripts.

- the development of Unix closely parallels the rise of open source software. early on there was shareware, freely available programs where users did not necessarily have access to the source code. there were a lot of good things about this, but it was also problematic because malicious programs could be disguised as innocent-looking games, screensavers, and utilities.
- Open source takes a source-centric view of software. the open source philosophy is that users have the right to obtain the software source code, and to expand and modify programs for their own use. this also meant the code could be inspected for backdoors, viruses, and malware.
- By creating a community of developers and users, accountability for bugs, security vulnerabilities, and compatibility issues became a shared responsibility. this new, global community of computer enthusiasts was empowered by the growing availability of faster internet services and the world wide web.
- there are many different variants of open source code, but all agree that users should have access to the source code. where they differ is in how one can, or must, redistribute changes.
- linux has adopted this philosophy to great success. since linux was written in the C programming language, and it mirrored the design and functionality of already established UNIX systems, it naturally became a forum where people could develop and share new ideas. Freed from the constraints of proprietary hardware and software platforms, large numbers of very skilled programmers have been able to contribute to the various distributions, making for software that is often more robust, stable, adaptable, and, frankly, better than the proprietary, closed source offerings which dominated the previous decades.
- large organizations were understandably suspicious of this new way of doing software. but over time they realized their best programmers were working on linux-based open source projects in their spare time. soon, linux servers and open source programs began to outperform the expensive, proprietary systems already in place. when it came time to upgrade outdated hardware the same programmers, engineers, and system administrators who had started working on linux as a hobby were able to convince their bosses to give linux a try. the rest is, as they say, history.
- Before the development of linux, many corporate and scientific applications ran on proprietary UNIX systems. companies, universities and governments that ran large server farms liked the stability and relative ease of application development offered.
- UNIX was initially created in 1969. By its fourth edition, in 1973, it had been rewritten in the C programming language that is still prominent today. In 1984 the University of California Berkeley released 4.2 BSD which introduced TCP/IP, the networking specification that underpins the internet. By the early 1990's, when linux development started, different companies developing UNIX operating systems realized their systems needed to be compatible, and they started working on the X/Open specification that is still used today.
- Over the years, computer scientists and the organizations that employ them have realized the benefit of using a consistent way of doing things, provide familiar tools and consistent ways of accomplishing specific tasks.
- The standardization of application programming interfaces (APIs) allows programs written for one specific UNIX or linux operating system to be ported (converted) relatively easy to run on another. So, while proprietary UNIX systems are still in use throughout the world in environments where "certified" solutions are preferred, the interoperability of these systems alongside linux computers is valued by industry, academia, and governments that use them.
- The importance of standards organizations cannot be overstated.
- Groups like the IEEE (Institute of Electrical and Electronics Engineers) and POSIX (Portable Operating System Interface), allow professionals from different companies and institutions to collaborate on specifications that make it possible for different operating systems and programs to work together. It doesn't matter if a program is closed or open source, simple or complex, if it is written to these standards others will be able to use and modify it in the future.
- Every innovation in computing is built on the work of others who came before.
- Open source software is a collaboration of different people with different needs and backgrounds all working together to make something better than any one of them could have made individually. Standards are what makes this possible and the many organizations that create, maintain and promote them are integral to the industry.

### 4.2 Open Source Licensing
- When talking about buying software, there are three distinct components:
  - **ownership** - who owns the intellectual property behind the software?
  - **money transfer** - how does money change hands, if at all?
  - **licensing** - what do you get? what can you do with the software? can you use it on only one computer? can you give it to someone else?
- In most cases, the ownership of the software remains with the person or company that created it. Users are only granted a license to use the software, this is a matter of copyright law. The money transfer depends on the business model of the creator. It's the licensing that differentiates open source software from closed source software.
- Two contrasting examples will get things started.
- With Microsoft Windows, the Microsoft corporation owns the intellectual property. The license itself, the End User License Agreement (EULA), is a custom legal document that you must click through, indicating your acceptance, in order to install the software. Microsoft keeps the source code and distributes only binary copies through authorized channels. For most consumer products you are allowed to install the software on one computer and are not allowed to make copies of the disk other than for a backup. You are not allowed to reverse engineer the software. You pay for one copy of the software, which gets you minor updates but not major upgrades.
- Linux is owned by Linus Torvalds. He has placed the code under a license called GNU General Public License Version 2 (GPLv2). This license, among other things, says that the source code must be made available to anyone who asks and that anyone is allowed to make changes. One caveat to this is that if someone makes changes and distributes them, they must put the changes under the same license so that others can benefit. GPLv2 also says that no one is allowed to charge for distributing the source code other than the actual costs of doing so (such as copying it to removable media).
- In general, when someone creates something, they also get the right to decide how it is used and distributed. Free and Open Source Software (FOSS) refers to software where this right has been given up; and one is allowed to view the source code and redistribute it.
- Linus Torvalds has done that with Linux - even though he created Linux he can't forbid someone from using it on their computer because he has given up that right through the GPLv2 license.
- Software licensing is a political issue, therefore it should come as no surprise that there are many different opinions. Organizations have come up with their own license that embodies their particular views, so it is easier to choose an existing license than come up with your own.
- For example, universities like the Massachusetts Institute of Technology (MIT) and University of California have come up with licenses, as have projects like the Apache foundation. Also, groups like the Free Software Foundation have created their own licenses to further their agenda.

#### 4.2.1 The Free Software Foundation
- Two groups can be considered the most influential forces in the world of open source: the Free Software Foundation and the Open Source Initiative.
- Only a few years after the development of the GNU project, Richard Stallman founded the Free Software Foundation (FSF) in 1985 with the goal of promoting free software. In this context, the word "free" does not refer to the price, but to the freedom to share, study, and modify the underlying source code.
- According to their website, the FSF believes that users should have "control over the technology we use in our homes, schools, and businesses."
- FSF also advocates that software licenses should enforce the openness of modifications. It is their view that if someone modifies free software that they should be required to share any changes they have made when they share it again. This specific philosophy is called copyleft.
- According to FSF, "copyleft is a general method for making a program (or other work) free (in the sense of freedom, not "zero price"), and requiring any modified and extended versions of the program to be free as well."
- The FSF also advocates against software patents and acts as a watchdog for standards organizations, speaking out when a proposed standard might violate the free software principles by including items like Digital Rights Management (DRM) which restrict what can be done with compliant programs.

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Introduction & Compiler
![Handwritten notes on introduction and compiler](./assets/handwritten-notes-1.jpg)

### Image 2: Open Source Philosophy & Interpreted Languages
![Handwritten notes on open source philosophy and interpreted languages](./assets/handwritten-notes-2.jpg)

### Image 3: Community & Linux Adoption
![Handwritten notes on community and Linux adoption](./assets/handwritten-notes-3.jpg)

### Image 4: UNIX History & Standards
![Handwritten notes on UNIX history and standards](./assets/handwritten-notes-4.jpg)

### Image 5: Standards Organizations & APIs
![Handwritten notes on standards organizations and APIs](./assets/handwritten-notes-5.jpg)

### Image 6: Open Source Licensing & Microsoft EULA
![Handwritten notes on open source licensing and Microsoft EULA](./assets/handwritten-notes-6.jpg)

### Image 7: GPLv2, FOSS, and Linus Torvalds
![Handwritten notes on GPLv2, FOSS, and Linus Torvalds](./assets/handwritten-notes-7.jpg)

### Image 8: Software Licensing & Free Software Foundation
![Handwritten notes on software licensing and Free Software Foundation](./assets/handwritten-notes-8.jpg)

### Image 9: FSF, Copyleft, and DRM
![Handwritten notes on FSF, copyleft, and DRM](./assets/handwritten-notes-9.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 04)
| Command | Description | Example |
| :--- | :--- | :--- |
| `gcc` | GNU Compiler Collection | `gcc -o program program.c` |
| `python` | Run Python interpreter | `python script.py` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)