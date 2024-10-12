# README.md

## Network Diagnostic Utilities: Ping and Traceroute

### Ping

**Description:**
Ping is a network diagnostic tool that tests the reachability of a host (such as a server) on an IP network. It measures the round-trip time for messages sent from the originating host to a destination computer and back.

**How It Works:**
When you use the ping command, it sends Internet Control Message Protocol (ICMP) Echo Request packets to the target address. If the target is reachable, it responds with ICMP Echo Reply packets. This tool is useful for:

- Checking if a host is online.
- Measuring network latency.
- Diagnosing packet loss.

**Sample Ping Command:**

```bash
ping example.com
```

**Interpreting Results:**

- **Reply from ```<IP Address>```:** Indicates that the host is reachable.
- **Time=xx ms:** Displays the round-trip time, indicating how long it took for the packets to travel to the host and back. Lower times indicate better network performance.
- **Request timed out:** Suggests that the host is not reachable, potentially due to network issues or that the host is offline.

### Traceroute

**Description:**
Traceroute is a network diagnostic tool used to determine the path taken by packets across an IP network. It reveals the route that data packets take to reach a target destination, showing all intermediate devices or nodes.

**How It Works:**
Traceroute sends out a series of packets with incrementally increasing Time to Live (TTL) values. When a packet reaches a router, the TTL is decremented by one. If the TTL reaches zero, the router drops the packet and sends back an ICMP Time Exceeded message. This process repeats until the final destination is reached.

**Sample Traceroute Command:**

```bash
traceroute example.com
```

(Use `tracert example.com` on Windows.)

**Interpreting Results:**

- **Each line in the output represents a hop.** Each hop indicates a router or a device the packets passed through to reach the destination.
- **IP Addresses:** Show the address of each intermediate router.
- **Time Values:** Show how long it took to reach each hop. If a hop times out, you will see `* * *` indicating that it did not receive a response within the expected timeframe.

---

## Basic SQL Commands Refresher

### 1. SHOW

The `SHOW` command is used to display information about databases, tables, or other objects in the database management system.

- **Example: Show all databases**

    ```sql
    SHOW DATABASES;
    ```

- **Example: Show tables in the current database**

    ```sql
    SHOW TABLES;
    ```

### 2. CREATE

The `CREATE` command is used to create a new database or table.

- **Example: Create a new database**

    ```sql
    CREATE DATABASE my_database;
    ```

- **Example: Create a new table**

    ```sql
    CREATE TABLE users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(100),
        email VARCHAR(100) UNIQUE,
        created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```

### 3. DROP

The `DROP` command is used to delete databases or tables.

- **Example: Drop a database**

    ```sql
    DROP DATABASE my_database;
    ```

- **Example: Drop a table**

    ```sql
    DROP TABLE users;
    ```

### 4. SELECT

The `SELECT` statement is used to retrieve data from one or more tables.

- **Example: Select all columns from a table**

    ```sql
    SELECT * FROM users;
    ```

- **Example: Select specific columns**

    ```sql
    SELECT name, email FROM users;
    ```

### 5. INSERT

The `INSERT` command is used to add new records to a table.

- **Example: Insert a new row into a table**

    ```sql
    INSERT INTO users (name, email) VALUES ('John Doe', 'john.doe@example.com');
    ```

- **Example: Insert multiple rows**

    ```sql
    INSERT INTO users (name, email) VALUES ('Jane Doe', 'jane.doe@example.com'), ('Alice Smith', 'alice.smith@example.com');
    ```
