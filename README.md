# Operating-System

## Basics of OS (I/O Structure)
Cpu device controller memory 

<img src="https://github.com/user-attachments/assets/f2797839-d49a-4c44-8f9b-b4e84b276ac5" alt="1" width="50%"/>

<img src="https://github.com/user-attachments/assets/440209b4-d046-4f59-9e49-0765740240fa" alt="2" width="50%"/>

---

1. The **device driver** 
    - tells the device controller what to do by loading instructions into its registers.

2. The **device controller** 
    - reads these instructions and decides how to handle the operation.
    - It transfers data between the device and its internal buffer.
    - When the operation finishes, the **device controller** notifies the device driver via an interrupt.
    - Finally, the **device driver** informs the operating system that the task is done.

### Example
- **Initiating the Task**:
    - The operating system (OS) asks the **device driver** to read a file from the hard disk.
    - The device driver sends a "read" command to the **Command Register** of the disk controller.
- **Processing the Command**:
    - The **disk controller** looks at the command in its register and begins reading the requested data from the disk.
    - The data is temporarily stored in the controller’s **buffer**.
- **Completion Notification**:
    - When the read operation is complete, the disk controller sends an **interrupt** to the CPU, saying, "I’m done!"
- **Returning Data to the OS**:
    - The device driver retrieves the data from the disk controller’s buffer and hands it over to the operating system.
    - The OS then processes the file (e.g., displays its content to the user).

---

**Registers in Device Controllers**
These registers control and monitor the device:

- **Data Register**: Temporarily holds the data being transferred.
- **Command Register**: Receives commands from the CPU (e.g., read, write).
- **Status Register**: Provides information about the device’s status (e.g., ready, busy, error).

---

## Functionality
1. **User Interface**: Example: The graphical user interface (GUI) provided by Windows or macOS, where users can interact with files and programs through icons and menus.
2. **Program Execution**: Example: Running a program like Microsoft Word or Google Chrome by clicking its icon.
3. **I/O Operations**: Example: Reading a file from a USB drive or writing data to a printer.
4. **File System Manipulation**: Example: Creating, deleting, or renaming a file or folder on your computer.
5. **Communications**: Example: Sending a message over a chat application like WhatsApp, which involves inter-process communication.
6. **Error Detection**: Example: A notification popping up when a disk becomes full or a file system becomes corrupted.
7. **Resource Allocation**: Example: The OS assigning CPU time and memory to multiple programs running simultaneously, like a browser and a video editor.
8. **Accounting**: Example: A cloud service tracking how much CPU and memory resources your virtual machine is using for billing purposes.
9. **Protection and Security**: Example: A password-protected login screen preventing unauthorized access to a computer.
