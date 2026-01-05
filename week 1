Week 1 — System Planning & Environment Design
← Week 1 | Week 2 →
Overview
Week 1 focuses on the planning and design of a secure and reproducible Linux lab environment prior to implementation. The objective of this phase is to define a clear system architecture, select appropriate Linux distributions, and design a controlled network topology that supports security hardening, performance testing, and future scalability.
All design decisions in this phase are intentionally made before deployment to ensure the environment reflects professional server administration practices and supports accurate security and performance evaluation in later weeks of the coursework.
Objectives
The objectives for Week 1 are to:
Design a virtualised dual-system lab environment
Select and justify appropriate Linux distributions
Plan a secure and controlled network topology
Define clear system roles and responsibilities
Establish a robust foundation for later security hardening and performance testing
Lab Environment Overview
Host System
Hardware: Mac Laptop
Virtualisation Platform: Oracle VirtualBox
Virtual Machines
Ubuntu Server (Target System)
Version: Ubuntu Server 22.04 LTS
Role: Target system for security configuration and performance evaluation
Interface: Headless (no graphical desktop environment)
Network Mode: Host-Only
IP Address: 192.168.56.103
Ubuntu Workstation (Administrative System)
Version: Ubuntu Desktop 24.04 LTS
Role: Administrative workstation for SSH access, monitoring, and testing
Network Mode: NAT + Host-Only
IP Address (Host-Only): 192.168.56.102
System Architecture Design
The system architecture is designed to isolate the server from direct internet access while allowing secure internal communication from a single trusted workstation. This reflects common enterprise and cloud server deployment models.
┌─────────────────────────────────────────────────────────┐
│                     Mac Laptop (Host)                    │
│                                                         │
│  ┌───────────────────────────────────────────────────┐ │
│  │              VirtualBox Environment                │ │
│  │                                                   │ │
│  │  ┌─────────────────┐   ┌──────────────────┐      │ │
│  │  │ Ubuntu Server   │◄──►│ Ubuntu Desktop   │      │ │
│  │  │ 22.04 LTS       │    │ 24.04 LTS        │      │ │
│  │  │ Host-Only       │    │ NAT + Host-Only  │      │ │
│  │  │ 192.168.56.103  │    │ 192.168.56.102   │      │ │
│  │  └─────────────────┘   └──────────────────┘      │ │
│  │                                                   │ │
│  │     Host-Only Network (192.168.56.0/24)           │ │
│  └───────────────────────────────────────────────────┘ │
│                                                         │
└───────────────────────────┼─────────────────────────────┘
                            │
                       Internet (NAT)
Figure W1-1: System architecture showing isolated server and administrative workstation.
Network Design Rationale
The server has no direct internet access, reducing its attack surface
The workstation acts as the single management point, enforcing controlled access
A Host-Only network enables secure internal communication between systems
NAT on the workstation allows controlled access for updates and downloads
Static IP addressing ensures predictable and reliable SSH connectivity
Design Trade-Off Considerations
Isolating the server from the internet significantly improves security by limiting exposure to external threats. However, this design introduces additional administrative complexity when performing system updates or installing packages. This trade-off prioritises security over convenience and reflects real-world operating system design decisions used in professional server environments.
Distribution Selection Justification
Ubuntu Server 22.04 LTS
Reasons for Selection
Long-Term Support (5 years of security updates)
Stable kernel suitable for performance testing
Extensive official documentation and community support
Excellent compatibility with VirtualBox
Widely used in enterprise and cloud environments
Trade-Offs
Slightly heavier than minimal distributions (e.g. Alpine Linux)
Some advanced enterprise features require Ubuntu Pro
Ubuntu Server 22.04 LTS was selected as it provides a realistic, industry-standard environment while remaining suitable for security hardening and performance evaluation tasks.
Workstation Responsibilities
The Ubuntu Desktop workstation is responsible for:
Secure SSH access to the server
Remote system administration and monitoring
Network testing and validation
Evidence collection (screenshots and logs)
Acting as a controlled gateway for internet access
This separation enforces command-line proficiency and mirrors professional remote administration workflows.
Network Configuration Summary
Ubuntu Server
Setting	Value
Network Mode	Host-Only
IP Address	192.168.56.103
Internet Access	Disabled
Ubuntu Workstation
Setting	Value
Adapter 1	NAT
Adapter 2	Host-Only
IP Address	192.168.56.102
Gateway	192.168.56.1
System Information Collection
The following commands were executed on the Ubuntu Server via SSH from the workstation to verify system configuration and resource allocation:
uname -a
free -h
df -h
ip addr
lsb_release -a
These commands confirm operating system version, kernel details, memory allocation, disk usage, and network configuration.
Evidence — System Verification
📸 Screenshot Filename: week1.png
Figure W1-2: Command-line output confirming OS version, memory, disk usage, and network configuration. The terminal prompt (username@server-hostname) is visible, demonstrating remote administration via SSH.
Learning Outcome Alignment
LO4: Demonstrated through command-line system inspection and remote verification of operating system configuration.
LO5: Addressed by evaluating security versus usability trade-offs in system architecture and network design.
Reflection (Week 1)
This planning phase established a secure and controlled lab foundation. By isolating the server, limiting internet exposure, and enforcing clear role separation between systems, the environment is well-suited for security hardening, performance testing, controlled experimentation, and real-world server administration scenarios.
The structured planning undertaken in this week ensures that later configuration, testing, and analysis can be conducted in a secure, repeatable, and professionally relevant manner.
