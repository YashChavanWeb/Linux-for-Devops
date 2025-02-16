# Linux Basics

## Table of Contents
1. [Introduction to the Internet](#introduction-to-the-internet)
2. [What is a Server?](#what-is-a-server)
3. [Difference Between Web Server and Application Server](#difference-between-web-server-and-application-server)
4. [Types of Applications](#types-of-applications)
5. [Application Support and Maintenance](#application-support-and-maintenance)
6. [Introduction to Linux](#introduction-to-linux)
   - [What is Linux?](#what-is-linux)
   - [How to Install Linux?](#how-to-install-linux)
   - [Difference Between Windows and Linux](#difference-between-windows-and-linux)
   - [Software Remote Location Server Tools](#software-remote-location-server-tools)
7. [Understanding Linux Components](#understanding-linux-components)
   - [Kernel, Bootloader, and Shell](#kernel-bootloader-and-shell)
   - [Linux System Architecture](#linux-system-architecture)
   - [Hardware Commands in Linux](#hardware-commands-in-linux)
8. [Linux File System](#linux-file-system)
9. [States of Processes in Linux](#states-of-processes-in-linux)
10. [How to Rent a Linux Machine on AWS](#how-to-rent-a-linux-machine-on-aws)

---

## Introduction to the Internet

The Internet works using fiber optic cables that run under the sea, connecting data centers worldwide. These data centers facilitate data transfer and ensure internet access for users globally.

1. **ISP (Internet Service Provider)**: An ISP provides internet connectivity and issues routers to connect devices like mobile phones and computers to the internet. The router assigns an IP address to each connected device.

2. **DNS (Domain Name System)**: When you type `youtube.com` in your browser, DNS helps map the domain to the correct IP address, allowing access to the YouTube server.

---

## What is a Server?

A **server** is a computer or machine dedicated to serving data to clients. For example:
- **File Server**: Serves files.
- **Web Server**: Serves static files like HTML, images, etc.
- **Application Server**: Runs applications and processes logic.

A **client** is a device or software that requests data, such as a browser, mobile phone, or computer.

---

## Difference Between Web Server and Application Server

- **Web Server**: Handles static data like images, text files, HTML, CSS, etc.
- **Application Server**: Handles dynamic data, processing business logic, calculations, and interacting with databases.

---

## Types of Applications

1. **Stand Alone Application**: 
   - Does not require an internet connection, database, or server.
   - Operates independently.

2. **Web Application**: 
   - Requires a combination of a web server, database, and other backend services.
   - It often involves multiple components working together.

---

## Application Support and Maintenance

Application support involves monitoring the health of applications, ensuring they are running smoothly, and troubleshooting issues like crashes or downtime.

---

## Introduction to Linux

### What is Linux?

Linux is an open-source operating system, developed by Linus Torvalds in 1991. It is a free version of UNIX, with a strong focus on security and development. Over 90% of servers and applications run on Linux.

**Key Features**:
- Open source
- No need for antivirus software
- Frequent updates (twice a year)
- Community contributions

---

### How to Install Linux?

1. **WSL (Windows Subsystem for Linux)**: Run Linux directly in Windows.
2. **VirtualBox**: Download VirtualBox and install Ubuntu.
3. **Cloud Providers (AWS, Azure, GCP)**: Rent a Linux machine via virtual machines in the cloud.
4. **Vagrant**: Set up and manage virtual environments locally.

---

### Difference Between Windows and Linux

| Feature        | Windows                  | Linux                           |
|----------------|--------------------------|---------------------------------|
| License        | Commercial License       | Open Source (GPL)               |
| Purpose        | General Purpose          | Development Focused             |
| Antivirus      | Needed                   | Not Required                    |
| Updates        | Frequent and flexible     | Updates twice a year            |

---

### Software Remote Location Server Tools

To connect to a server remotely:
1. **RDP (Remote Desktop Protocol)**: For graphical interface remote connections.
2. **SSH (Secure Shell)**: For command-line access to remote systems.
3. **Anydesk**: For remote desktop access.

---

## Understanding Linux Components

### Kernel, Bootloader, and Shell

1. **Kernel**: The heart of the operating system that manages hardware and system resources (e.g., storage, memory). Written in C.
2. **Shell**: An interface (command line) that allows interaction with the kernel. It provides command-based input/output.
3. **Bootloader**: A program like **GRUB** that initializes the system and loads the operating system during boot.

---

### Linux System Architecture

The architecture consists of:
- **Application**: Software programs running on top.
- **Shell**: Interface for communication with the kernel.
- **Kernel**: Core system component managing resources.
- **Hardware**: Physical devices running the system.

---

### Hardware Commands in Linux

- `top`: View running processes and their CPU usage.
- `df -h`: Check disk usage.
- `free -h`: View RAM usage.

---

## Linux File System

The Linux file system starts from the root directory `/`. Here's a quick guide:
- **`cd`**: Change directory.
- **`ls`**: List directory contents.
- The hierarchy of directories includes:
  - `/etc`: Configuration files.
  - `/home`: User home directories.
  - `/usr`: User programs and utilities.

---

## States of Processes in Linux

Processes in Linux can be in the following states:
- **Sleeping**: Waiting for an event.
- **Running**: Actively being processed.
- **Terminated/Killed**: Process has stopped.
- **Zombie**: Process that has completed but still has an entry in the process table.
- **Stopped**: A process that is paused.

---

## How to Rent a Linux Machine on AWS

1. **Sign Up for AWS**: Create an account on AWS.
2. **Search for EC2**: Elastic Compute Cloud (EC2) allows you to rent a virtual machine.
3. **Create an Instance**:
   - Choose the instance type (e.g., `t2.micro` for the free tier).
   - Select a Linux distribution (e.g., Ubuntu).
   - Wait for the instance to enter the "Running" state.
4. **Connect**: After the instance is running, click "Connect" to access it via SSH (command-line interface) from your terminal.

---


