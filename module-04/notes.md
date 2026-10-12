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

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Introduction to Open Source
![Handwritten notes on introduction to open source](./assets/handwritten-notes-1.jpg)

### Image 2: Open Source Philosophy & Community
![Handwritten notes on open source philosophy and community](./assets/handwritten-notes-2.jpg)

### Image 3: Linux Adoption & Industry Shift
![Handwritten notes on Linux adoption and industry shift](./assets/handwritten-notes-3.jpg)

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