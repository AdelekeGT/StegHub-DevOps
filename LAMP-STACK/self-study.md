# Self Study

## Software Development Life Cycle (SDLC)

Software engineering is the systematic approach to the design and development of software. It identifies the steps needed to develop high-quality software in a predictable timeframe and budget. The goal of the SDLC is to produce software that meet the client's business requirements. It defines phases of the software development process that encompass their own process and deliverables. It is cycle of planning, design and development that can be implemented as an iterative approach to software development. Adherence the SDLC minimizes development risks and costs.

The SDL began to take shape in the mid-1960s. In its initial conception, it used what is called the 'waterfall method' to manage projects where the development of software follows a linear pattern through discrete stages, but have since been adapted to introduce iteration so that shifting requirements can be accommodated.

### Stages of the SDLC

- **Planning:**
  Depending on organizations, this stage might be called requirements, strategy, or analysis. Here, requirements are gathered, analyzed, documented and prioritized. Labor and material costs are estimated and weighed against time constraints. Project teams are identified, and roles of each team member are proposed. If stakeholders are struggling to define requirements, often the development team produces prototypes to tease out those requirements. After requirements have been gathered, they are combined into a Software Requirements Specification (SRS) document. The requirements from SRS are used by the team to propose and develop the software architecture. A Design Document is created here, which is given to the developers for use in the coming development stage.

- **Development:**
  Can be called the building or implementation phase. Here, developers start the coding process once the design document, which will be a guide for them, is completed. Document is used to determine and assign coding tasks, depending on the specialty of each team member. This stage requires use of programming tools, languages, and software stacks. Organizations might have standard guidelines to be followed when coding.

- **Testing:**
  Once coding is complete, testing commences. Some large organizations have dedicated testing teams. Testing can be manual. automated, or both. Code needs to be tested to ensure it is stable, secure, and meets requirements outlined in SRS. Product bugs are reported, tracked, and fixed, and code is retested until software is stable. Common levels of testing include unit testing, integration testing, system testing, and acceptance testing.

- **Deployment:**
  Here, the application is released into the production environment and made available to users. This can also happen in stages - first, it is release onto a user acceptance testing platform, also called UAT, and one the customer signs off on the functionality, it is released to production.

- **Maintenance:**
  This stage helps to find anu other bugs, identify UI issues, and identify other requirements that may not have been listed in the SRS. If bugs are discovered in this stage that somehow got past testing, these errors may need to be fixed for high-priority issues, or incorporated into the requirements as part of a future software release and the process can start over again for an improved version of the software.

## LAMP Stack

The LAMP stack is a popular set of open-source software used to build and run web applications and websites. The acronym LAMP stands for:

- L - Linux: The operating system that provides the foundation for the stack.
- A - Apache: The web server software that serves web pages to users.
- M - MySQL: The database management system used to store and manage data.
- P - PHP (or Perl/Python): The programming language used to develop dynamic content for the web application.

### Components in Detail

- **Linux:** The operating system that manages hardware and software resources. It’s widely used for servers due to its security, stability, and flexibility.

- **Apache:** A widely used web server software that handles HTTP requests from users and delivers web pages to their browsers.

- **MySQL:** A relational database management system (RDBMS) used to store and retrieve data for web applications. It supports SQL (Structured Query Language) for querying the database.

- **PHP (or Perl/Python):** A server-side scripting language that processes user requests and dynamically generates content. PHP is often used to connect the application to the database and process data from forms or other user interactions.

### How the LAMP Stack Works

Linux serves as the foundation where all other components run.
Apache listens for HTTP requests from clients (browsers) and responds by serving web pages.
PHP runs on the server, interpreting the server-side scripts and generating dynamic web pages based on user input or other factors.
MySQL stores all the application’s data, which PHP can interact with to retrieve or save information (e.g., user profiles, blog posts, product listings).
Below is an example of a LAMP Stack workflow:
A user sends a request via a browser to view a webpage (Apache handles the request).
PHP interacts with the MySQL database to fetch necessary data (e.g., content, user data).
PHP dynamically generates the HTML and sends the response back to the user's browser, which displays the content.

## 'chmod' and 'chown'

In Linux and Unix-based operating systems, **`chmod`** and **`chown`** are two important commands used to manage file and directory permissions and ownership:

### 1. **`chmod`** (Change Mode)

The `chmod` command is used to **change file or directory permissions**. Permissions determine who can read, write, or execute a file.

- _Syntax_

```bash
chmod [options] mode file
```

#### File Permissions

Each file and directory in Linux has three sets of permissions:

1. **Owner (User)**: The person who owns the file.
2. **Group**: A group of users that can also have permissions on the file.
3. **Others (World)**: Everyone else who has access to the system.

The permissions are represented by three types:

- **r** (read): Permission to view the file or list a directory.
- **w** (write): Permission to modify the file or directory contents.
- **x** (execute): Permission to run a file or access a directory.

These are often represented as a string like `rwxr-xr--`, where:

- The first set (`rwx`) refers to the owner.
- The second set (`r-x`) refers to the group.
- The third set (`r--`) refers to others.

### 2. **`chown`** (Change Ownership)

The `chown` command is used to change the owner or group of a file or directory. It can be used to transfer ownership or set the group that can access the file.

- _Syntax_

```bash
chown [options] owner[:group] file
```

- **owner**: The user who will own the file.
- **group**: The group that will own the file.

## TCP and UDP

TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) are two fundamental communication protocols used to transmit data over the Internet. They both operate in the transport layer of the OSI model, but they differ in how they manage the transmission of data.

### TCP (Transmission Control Protocol)

TCP is a connection-oriented protocol, meaning that a connection is established and maintained until all data is transmitted between the two communicating devices. It ensures reliable, ordered, and error-checked delivery of data.

#### Key Features of TCP

1. **Connection-Oriented**: A connection is established using a process called the three-way handshake before data is transmitted.
2. **Reliable**: TCP guarantees the delivery of data packets. If any packets are lost, they are re-sent.
3. **Ordered**: Packets are guaranteed to arrive in the correct order.
4. **Error-Checking**: TCP performs error-checking and will retransmit packets if errors are detected.
5. **Flow Control**: TCP regulates the data flow to ensure that a sender is not overwhelming the receiver.

#### Example Uses of TCP

- Web browsing (HTTP/HTTPS)
- Email (SMTP, IMAP, POP3)
- File Transfer Protocol (FTP)
- Secure Shell (SSH)

### UDP (User Datagram Protocol)

UDP is a connectionless protocol, meaning that data is sent without establishing a connection and without ensuring the reliability of transmission. It is faster but less reliable compared to TCP.

#### Key Features of UDP

1. **Connectionless**: No handshake is required; data is just sent without establishing a connection.
2. **Unreliable**: UDP does not guarantee the delivery of packets. Packets can be lost, duplicated, or arrive out of order.
3. **No Ordering**: UDP does not guarantee that packets will arrive in the correct order.
4. **No Flow Control**: There is no mechanism to regulate data flow between sender and receiver.
5. **Lightweight and Fast**: UDP is simpler and has lower overhead, making it faster than TCP, but at the cost of reliability.

#### Example Uses of UDP

- Video and audio streaming (e.g., Netflix, YouTube)
- Online gaming (real-time multiplayer)
- Voice over IP (VoIP)
- DNS queries
- TFTP (Trivial File Transfer Protocol)

### Differences Between TCP and UDP

| Feature            | TCP                                         | UDP                                       |
| ------------------ | ------------------------------------------- | ----------------------------------------- |
| **Connection**     | Connection-oriented (establishes a session) | Connectionless (no session required)      |
| **Reliability**    | Reliable, ensures data is received          | Unreliable, no guarantee of delivery      |
| **Ordering**       | Ensures data is received in order           | No order guarantee                        |
| **Error-checking** | Yes, with retransmission of lost packets    | Minimal error-checking, no retransmission |
| **Speed**          | Slower due to overhead of reliability       | Faster, lower overhead                    |
| **Use Cases**      | File transfer, web browsing, email          | Streaming, gaming, VoIP, DNS queries      |

### Popular Ports on the Web

Both TCP and UDP operate over ports. Below is a list of commonly used ports and the services that typically use them:

| Port | Protocol | Service/Use                                         |
| ---- | -------- | --------------------------------------------------- |
| 20   | TCP      | FTP (File Transfer Protocol) - Data                 |
| 21   | TCP      | FTP (File Transfer Protocol) - Command              |
| 22   | TCP      | SSH (Secure Shell)                                  |
| 23   | TCP      | Telnet                                              |
| 25   | TCP      | SMTP (Simple Mail Transfer Protocol)                |
| 53   | UDP/TCP  | DNS (Domain Name System)                            |
| 67   | UDP      | DHCP (Dynamic Host Configuration Protocol) - Server |
| 68   | UDP      | DHCP (Dynamic Host Configuration Protocol) - Client |
| 80   | TCP      | HTTP (Hypertext Transfer Protocol)                  |
| 110  | TCP      | POP3 (Post Office Protocol v3)                      |
| 119  | TCP      | NNTP (Network News Transfer Protocol)               |
| 123  | UDP      | NTP (Network Time Protocol)                         |
| 143  | TCP      | IMAP (Internet Message Access Protocol)             |
| 161  | UDP      | SNMP (Simple Network Management Protocol)           |
| 194  | TCP      | IRC (Internet Relay Chat)                           |
| 443  | TCP      | HTTPS (HTTP Secure)                                 |
| 465  | TCP      | SMTPS (SMTP Secure)                                 |
| 514  | UDP      | Syslog (System Logging Protocol)                    |
| 636  | TCP      | LDAPS (LDAP over SSL)                               |
| 993  | TCP      | IMAPS (IMAP Secure)                                 |
| 995  | TCP      | POP3S (POP3 Secure)                                 |
| 3306 | TCP      | MySQL Database                                      |
| 3389 | TCP      | RDP (Remote Desktop Protocol)                       |
| 5432 | TCP      | PostgreSQL Database                                 |
| 5900 | TCP      | VNC (Virtual Network Computing)                     |
| 8080 | TCP      | HTTP Alternative                                    |
| 8443 | TCP      | HTTPS Alternative                                   |
