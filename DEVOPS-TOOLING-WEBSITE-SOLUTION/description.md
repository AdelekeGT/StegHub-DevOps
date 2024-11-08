# DevOps Tooling Website Solution: Multi-Tier Web Application

## Overview

This DevOps project implements a multi-tier web application with the following components:

1. **Infrastructure**: AWS
2. **Web Server**: Red Hat Enterprise Linux 8
3. **Database Server**: Ubuntu 24.04 + MySQL
4. **Storage Server**: Red Hat Enterprise Linux 8 + NFS Server
5. **Programming Language**: PHP
6. **Code Repository**: GitHub

## Architecture

The project uses a multi-tier architecture, with each component on a separate server or service:

+-------------+     +------------------+     +------------------+
| Web Server  |     | Database Server  |     |  Storage Server  |
| (RHEL 8)    |     | (Ubuntu 24.04)   |     |  (RHEL 8 + NFS)  |
|  +-------+  |     |  +-----------+   |     |   +---------+    |
|  |PHP App|  |     |  |  MySQL    |   |     |   |   NFS   |    |
|  +-------+  |     |  +-----------+   |     |   +---------+    |
+-------------+     +------------------+     +------------------+
|                     |                         |
|                     |                         |
+------------------+  +------------------+  +------------------+
|       AWS        |  |       AWS        |  |       AWS        |
|  Infrastructure  |  |  Infrastructure  |  |  Infrastructure  |
+------------------+  +------------------+  +------------------+
