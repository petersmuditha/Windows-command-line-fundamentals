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
