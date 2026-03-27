# Windows-command-line-fundamentals

# 🖥️ Windows Command Line Mastery: Security & Administration
This repository is a comprehensive documentation and reference guide based on the Windows Command Line curriculum from TryHackMe. It focuses on leveraging the Command Prompt (CMD) for system navigation, configuration, and security auditing.

# 📝 Project Description
This project serves as a technical knowledge base for interacting with the Windows Operating System through its native Command Line Interface (CLI). 
It bridges the gap between basic file manipulation and advanced system interrogation, providing a structured approach to managing Windows environments without relying on a Graphical User Interface (GUI). 
It is designed for system administrators, security analysts, and penetration testers who need to operate efficiently within a Windows ecosystem.

# 🔍 What is it?
At its core, the Windows Command Line is a Command-Line Interpreter (CLI). Unlike the Graphical User Interface (GUI) we use every day—which relies on icons, windows, and mouse clicks—the CLI is a text-based medium for interacting with the operating system's kernel.
Think of the GUI as a "pre-set menu" in a restaurant where you can only pick what is visible.
The Command Line is like talking directly to the chef in the kitchen: it allows you to bypass the visual limitations and execute specific, complex instructions that the interface might hide or simplify.
In Windows, this is primarily represented by CMD.exe (the Command Prompt), a legacy-compatible environment that executes Win32 functions through text input.

# 💼 Why is it vital to our business?
In a professional or enterprise environment, the Command Line isn't just a "cool tool" for hackers; it is a foundational pillar of reliability.
Automation at Scale: You cannot "click" a button on 1,000 computers at once. The CLI allows us to write scripts that perform updates, configurations, and deployments across an entire global network simultaneously.
Precision and Speed: Many administrative tasks (like checking network routing tables or deep-level file permissions) require ten clicks in the GUI but only one string of text in the CLI.
Low Overhead: When managing remote servers (Windows Server), running a GUI consumes RAM and CPU. The CLI is "lightweight," allowing the hardware to focus 100% of its power on the actual business data rather than rendering pretty windows.

# 🛡️ How do we keep the system secure?

Command-line access is powerful, and with power comes the need for rigorous security protocols. We maintain system integrity through:
The Principle of Least Privilege (PoLP): We advocate for performing most tasks as a standard user. Administrative privileges (Run as Administrator) are only invoked when absolutely necessary for system-wide changes.
Command Auditing: We implement logging (such as Process Creation events via Group Policy) to track which commands are executed, helping to detect "Living off the Land" (LotL) attacks where hackers use built-in tools for malicious ends.
Input Validation: When writing scripts, we ensure all variables are sanitized to prevent command injection vulnerabilities.
Access Control: Restricting access to sensitive commands (like net user or reg) to only authorized personnel to prevent unauthorized configuration changes or privilege escalation.

## ⌨️ Essential Interaction: Basic Commands

Once we understand the importance of Linux, the next step is learning how to communicate with the system via the Command Line Interface (CLI). Below are two fundamental commands for any security professional.

### 1. `set` 
The set command is used to view, set, or remove environment variables in the current Command Prompt session.
* **Why it matters:** Automation and Scripting: IT administrators use scripts within batch files (.bat) to automate repetitive tasks, such as mapping network drives or installing software, dynamically adapting to the specific user or computer.

Software Configuration: Many business applications read environment variables to determine where to find data or licenses..

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 2. `path` 
Displays or sets the list of directories contained in the system variable.
* **Why it matters:** Operational Efficiency: Without proper path configuration, employees would have to type the entire path (e.g., C:\Program Files\CompanySoftware\bin\app.exe) every time. With path, they simply type app.
Development Tool Management: For IT teams and programmers, path configuration is essential for ensuring compilers, databases, and management tools run without "unrecognized command" errors..

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 3. `Ver` 
The ver command is the quickest way to see the exact version of your Windows operating system.
* **Why it matters:** Security and Compliance: Knowing whether PCs are up to date is critical for businesses. ver allows you to instantly identify if a machine is running an outdated version vulnerable to cyber attacks.
Technical Support (Help Desk): When an employee has a problem, the technician uses ver to determine whether the company software is compatible with that specific build of Windows, speeding up ticket resolution..

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 4. `systeminfo` 
Displays detailed configuration information about the computer and its operating system, including BIOS version, memory, and network card details.
* **Why it matters:** Vital for Asset Management. It helps IT departments quickly audit hardware specs and see when the OS was last installed or patched.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 5. `ipconfig` 
Displays the basic IP address, subnet mask, and default gateway for all network adapters.
* **Why it matters:** The starting point for any "I can't get on the internet" ticket. It confirms if a machine is actually connected to the office network.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

  ### 6. `ipconfig /all` 
A more verbose version of the previous command that includes DNS servers, MAC addresses (physical IDs), and DHCP lease info.
* **Why it matters:** Essential for Network Troubleshooting. It tells the IT team exactly which server is providing the IP address and whether the DNS settings are correct for the company domain.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 7. `ping` 
Sends a small packet of data to an IP address or domain to see if it responds and how long it takes.
* **Why it matters:** Verifies Reachability. It’s the quickest way to check if a server is "up" or "down" without needing to open a browser or app.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 8. `tracert` 
Shows the path a packet takes to reach a destination, listing every "hop" (router) along the way.
* **Why it matters:** Used for Bottleneck Identification. If a branch office can’t reach the main headquarters, tracert shows exactly where the connection is failing in the provider's network.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 9. `nslookup` 
Queries DNS (Domain Name System) to find the IP address associated with a domain name, or vice versa.
* **Why it matters:** Critical for Web and Email Services. If employees can't reach "https://www.google.com/search?q=portal.company.com," nslookup tells the admin if the name is being translated correctly to the right server.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 10. `netstat` 
Displays all active network connections (incoming and outgoing) and listening ports.
* **Why it matters:** Provides Visibility. It helps admins see if a computer is communicating with an unauthorized external server.

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)

### 11. `netstat -abon` 
A powerful variation that shows the executable (program) involved in every connection, along with the Process ID (PID).
* **Why it matters:** A key Cybersecurity tool. If a computer is infected with malware, netstat -abon can reveal exactly which "hidden" program is sending data to a hacker's server..

  ![image alt](https://github.com/petersmuditha/Linux-for-cybersecutry/blob/0d8ed979dd37fe43dcf48b0d73b9e676b0888044/Cattura5.PNG)
