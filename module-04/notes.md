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
- The FSF have developed their own set of licenses which are free for anyone to use based on the original GNU General Public License (GPL). FSF currently maintains GNU General Public License version 2 (GPLv2) and version 3 (GPLv3), as well as the GNU Lesser General Public licenses version 2 (LGPLv2) and version 3 (LGPLv3).
- These licenses are meant to be included in the actual source code to ensure that all future variants and modifications of the original program continue to have the same freedom of use as the original.
- The GPL license and its variants are powerful legal tools to advance the cause of free software worldwide. what started off in 1983 as one man's desire to share and improve software by letting others change it has ended up changing the world.

> **consider this :**
> the changes between GPLv2 and GPLv3 largely focused on using free software on a closed hardware device which has been coined tivoization. TiVo is a company that builds a television digital video recorder on their own hardware and used linux as the base for their software.
> While tivo released the source code to their version of linux as required under GPLv2, the hardware would not run any modified binaries. In the eyes of the FSF, this went against the spirit of the GPLv2, so they added a specific clause to version 3 of the license. Linus Torvalds agrees with Tivo on this matter and has chosen to stay with GPLv2.

#### 4.2.2 The Open Source Initiative
- The Open Source Initiative (OSI) was founded in 1998 by Bruce Perens and Eric Raymond. They believed that the Free Software Foundation was too politically charged and that less extreme licenses were necessary, eventually around the copyright aspects of FSF licenses. OSI believes that not only should the source be freely available, but also that no restrictions should be placed on the use of the software, no matter what the intended use.
- Unlike the FSF, the OSI does not have its own licenses. Instead, the OSI has a set of principles and adds licenses to that list if they meet those principles, called open source licenses. software that conforms to an open source license is, therefore, open source software.
- One type of open source license is the BSD (Berkeley Software Distribution) and its derivatives, which are much simpler than GPL. There are currently two current "BSD" licenses approved by OSI, a 2-clause and a 3-clause.
- These licenses state that you may redistribute the source and binaries as long as you maintain copyright notices and don't imply that the original creator endorses your version. In other words "do what you want with this software, just don't say you wrote it." According to FSF, the original BSD license had a serious flaw in that it required developers to add a clause acknowledging the University of California, Berkeley in every advertisement for software licensed this way. As others copied this simple license, they included acknowledgement for their own institutions which led to over 75 such acknowledgements in some cases.
- FSF licenses, such as GPLv2, are also open source licenses. However, many open source licenses such as BSD and MIT do not contain the copyleft provisions and thus not acceptable to the FSF.
- These licenses are called permissive free software licenses because they are permissive in how you can redistribute the software. you can take BSD licensed software and include it in a closed software product as long as you give proper attribution.
- Rather than dwell over the finer points of open source and free software, the community has started referring to them collectively as Free and Open Source Software (FOSS). The English word "free" can mean "free as in lunch" (as in no cost) or "free as in speech" (as in no restrictions). This ambiguity led to the inclusion of the word "libre" to refer to the latter definition, thus, we end up with Free / Libre / open source software (F/LOSS).

#### 4.2.3 Creative Commons
- FOSS licenses are mostly related to software. people have placed works such as drawings and plans under FOSS licenses, but this was not the intent.
- When software has been placed in the public domain, the author has relinquished all rights, including the copyright on the work. In some countries, this is the default when the work is done by a government agency. in some countries, copywrited work becomes public domain after the author has died and a lengthy waiting period has elapsed.
- The creative commons (cc) organization has created the creative commons licenses which try to address the intentions behind FOSS licenses for non-software entities. CC licenses can also be used to restrict commercial use if that is the desire of the copyright holder. the CC licenses are made of the following set of conditions the creator can apply to their work:
  - **Attribution (BY)** - All CC licenses require that the creator must be given credit, without implying that the creator endorse the use.
  - **ShareAlike (SA)** - this allows others to copy, distribute, perform, and modify the work, provided they do so under the same terms.
  - **NonCommercial (NC)** - this allows others to distribute, display, perform, and modify the work for any purpose other than commercially.
  - **NoDerivatives (ND)** - this allows others to distribute, display, and perform only original copies of the work. they must obtain the creator's permission to modify it.
- These conditions are then combined to create the six main licenses offered by creative commons.
  - **Attribution (CC BY)** - much like the BSD license, you can use CC BY content for any use but must credit the copyright holder.
  - **Attribution ShareAlike (CC BY-SA)** - A copyleft version of the Attribute license: Derived works must be shared under the same license, much like in the free software ideals.
  - **Attribution NoDerivs (CC BY-ND)** - you may redistribute the content under the same conditions as CC BY, but must not change it.
  - **Attribution-NonCommercial (CC BY-NC-SA)** - builds on the CC BY-NC license but requires that your changes be shared under the same license.
  - **Attribution-NonCommercial (CC BY-NC)** - just like CC BY, but you may not use it for commercial purposes.
  - **Attribution-NonCommercial-NoDerivs (CC BY-NC-ND)** - you are sharing the content to be use for non-commercial purposes, but people may not change the content.
  - **No Rights Reserved (CC0)** - this is the creative commons version of public domain.

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

### Image 10: GPL Variants and Tivoization
![Handwritten notes on GPL variants and Tivoization](./assets/handwritten-notes-10.jpg)

### Image 11: Open Source Initiative & Tivoization Dispute
![Handwritten notes on Open Source Initiative and Tivoization dispute](./assets/handwritten-notes-11.jpg)

### Image 12: BSD Licenses & OSI Principles
![Handwritten notes on BSD licenses and OSI principles](./assets/handwritten-notes-12.jpg)

### Image 13: Permissive Licenses, FOSS, and Public Domain
![Handwritten notes on permissive licenses, FOSS, and public domain](./assets/handwritten-notes-13.jpg)

### Image 14: Creative Commons Organization & Conditions
![Handwritten notes on Creative Commons organization and conditions](./assets/handwritten-notes-14.jpg)

### Image 15: Creative Commons License Combinations
![Handwritten notes on Creative Commons license combinations](./assets/handwritten-notes-15.jpg)

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