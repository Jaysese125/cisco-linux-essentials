# Module 02: Operating Systems

> **Course:** NDG Linux Essentials  
> **Status:** 🔄 In Progress  
> **Objective:** Understand the role of operating systems, different interface types, and major OS families.

---

## 📖 Chapter 2: Operating Systems

### 2.1 Operating Systems
- an operating system is software that runs on a computing device and manages the hardware and software components that make up a functional computing system.
- Modern operating systems don't just manage hardware and software resources, they schedule programs to run in a multi-tasking manner (sharing the processor so that multiple tasks can occur apparently simultaneously)
- provide standard services that allow users and programs to request something happen (for example a print job) from the operating system, and provided it's properly requested, the operating system will accept the request and perform the function needed.
- Desktop and server operating systems are by nature more complex than an operating system that runs on a single-purpose device such as a firewall, or a mobile phone. From a simple set-top box that provides a menu interface for a cable provider, to supercomputers and massive, parallel computing clusters, the generic term operating system is used to describe whatever software is booted and run on that device.

> **Diagram:**
> users
> software (system software, application, operating system)
> hardware

- Computer users today have a choice mainly between three major operating systems: Microsoft Windows, Apple MacOS, and Linux.
- Of the three major operating systems listed, only Microsoft windows is unique in its underlying code. Apple's MacOS is a fully-qualified UNIX distribution based on BSD Unix (an operating system distributed until 1995), complemented by a large amount of proprietary code. It runs on hardware specifically optimized to work with Apple software.
- Linux can be any one of hundreds of distribution packages designed or optimized for whatever task is required. Only Microsoft windows is based on a proprietary code base that isn't either UNIX or Linux based.
- A user can easily interact with any of these systems by pointing and clicking their way through everyday productivity tasks that all behave similarly regardless of the underlying operating system.
- Except for windows, which is mostly administered via the GUI, most system administration tasks are performed using typed commands in a terminal.
- An administrator that is familiar with UNIX can typically perform tasks on Linux system and vise versa. Many UNIX command line functions also have Microsoft equivalents that administrator use to do their work efficiently.

### 2.1.1 Decision Points

#### Role
- The first decision when specifying any computer system is the machine's role.
  - Will you be sitting at the console running productivity applications or web browsing? If so, a familiar desktop is best.
  - Will the machine be accessed remotely by many users or provide services to remote users? Then it's a server.
- Servers typically sit in a rack and share a keyboard and monitor with many other computers, since console access is generally only used for configuration and troubleshooting.
- servers generally run as a CLI, which frees up resources for the real purpose of the computer: serving information to clients (any user or system that accesses resources remotely).
- Desktop systems primarily run a GUI for the ease of use of their users.

#### Function
- Next point is to determine the functions of the machine. Is there a specific software it needs to run, or specific functions it needs to perform? Will there be hundreds, even thousands, of these machines running at the same time? What is the skill-set of the team managing the computer and software?

#### life cycle
- the service lifetime and risk tolerance of the server also needs to be determined. Operating systems and software upgrades come on a periodic basis, called a release cycle.
- vendors only support older version of software for a certain period of time before not offering any updates; this is called a maintenance cycle or life cycle.
- In an enterprise server environment, maintenance and release cycles are critical considerations because it is time-consuming and expensive to do major upgrades. Instead, the server hardware itself is often replaced because increased performance is worth extra expense and the resources involved are often many times more costly than the hardware.

> **consider this**
> there is a fair amount of work involved in upgrading a server due to specialized configurations, application software patching, and user testing, so a proactive organization will seek to maximize their return on investment in both human and monetary capital.

- Modern data centers are addressing this challenge through virtualization. In a virtual environment, one physical machine can host dozens, or even hundreds of virtual machines, decreasing space and power requirements, as well as providing for automation of many tasks previously done manually by systems administrators.
- scripting programs allow virtual machines to be created, configured, deployed and removed from a network without the need for human intervention. Of course, a human still needs to write the script and monitor these systems, at least for now.
- the need for physical hardware upgrades has also been decreased immensely with the advent of cloud services providers like AMAZON WEB SERVICES, RACKSPACE, and MICROSOFT AZURE.
- Similar advances have helped desktop administrators manage upgrades in an automatic fashion and with little to no user interruption.

---

## 📸 Proof of Learning (Handwritten Notes)

### Image 1: Operating Systems (Part 1)
![Handwritten notes on operating systems part 1](./assets/handwritten-notes-1.jpg)

### Image 2: Operating Systems (Part 2)
![Handwritten notes on operating systems part 2](./assets/handwritten-notes-2.jpg)

### Image 3: Operating Systems (Part 3)
![Handwritten notes on operating systems part 3](./assets/handwritten-notes-3.jpg)

### Image 4: Decision Points - Role & Function
![Handwritten notes on decision points role and function](./assets/handwritten-notes-4.jpg)

### Image 5: Decision Points - Life Cycle & Upgrades
![Handwritten notes on decision points life cycle and upgrades](./assets/handwritten-notes-5.jpg)

### Image 6: Decision Points - Virtualization & Cloud
![Handwritten notes on decision points virtualization and cloud](./assets/handwritten-notes-6.jpg)

---

## 🆕 Ongoing Learning & Additions

### New Discoveries / Lab Reflections

### Command Cheat Sheet (Module 02)
| Command | Description | Example |
| :--- | :--- | :--- |
| `uname -r` | Show Linux kernel version | `uname -r` |
| `su` | Switch user (to root) | `su` |
| `ls` | List directory contents | `ls -la` |

---

## 📚 Resources
- [LPI Linux Essentials Official Page](https://www.lpi.org/our-certifications/linux-essentials-overview/)
- [GNU Project Official Website](https://www.gnu.org/)
- [The Linux Kernel Archives](https://www.kernel.org/)