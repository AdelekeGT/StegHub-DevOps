# SELF-STUDY

This document outlines a series of exercises to refresh your knowledge of core tech concepts.

## 1. The OSI Model

The Open Systems Interconnection (OSI) model is a conceptual framework that divides network communication into seven layers. Each layer has specific functionalities, allowing diverse systems to communicate seamlessly. Here's a breakdown of each layer:

**Layer | Description**
------- | --------
**Application** | This layer interacts directly with user applications like web browsers or email clients. It defines protocols for data exchange between applications.
**Presentation** | This layer formats data for transmission and ensures compatibility between different systems.
**Session** | This layer establishes, manages, and terminates sessions between communicating devices.
**Transport** | This layer provides reliable data transport by breaking data into packets, ensuring delivery, and checking for errors.
**Network** | This layer handles routing and addressing of data packets across networks.
**Data Link** | This layer controls data transmission on the physical layer and detects errors in data frames.
**Physical** | This layer transmits and receives raw data bits over the physical network medium (cables, wires).

**Understanding the OSI model helps you visualize network communication and troubleshoot connection issues.**

## 2. Exploring Load Balancing

Load balancing is a technique for distributing incoming traffic across multiple servers. This ensures better performance and prevents overloading individual servers. Here are some common types of load balancing:

* **DNS-based Load Balancing (DNSBL):** Distributes traffic based on pre-configured settings in the Domain Name System (DNS).
* **Hardware Load Balancing:** Uses dedicated hardware devices to route traffic based on predefined algorithms.
* **Software Load Balancing:** Utilizes software applications running on servers to manage traffic distribution.

**Common Load Balancing Techniques:**

* **Round Robin:** Distributes traffic evenly across available servers.
* **Least Connections:** Directs traffic to the server with the fewest active connections.
* **Weighted Round Robin:** Assigns weights to servers based on capacity, directing more traffic to powerful servers.

**Load balancing is crucial for highly available and scalable web applications.**

## 3. Practicing Web Form Editing (HTML + CSS + JS)

To hone your web development skills, try editing a simple web form. You can use a basic HTML template with placeholders for form elements like text fields, buttons, and dropdowns.

Here's an example structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Form</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Contact Form</h1>
  <form id="contactForm">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    <br>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <br>
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="5" required></textarea>
    <br>
    <button type="submit">Submit</button>
  </form>

  <script src="script.js"></script>
</body>
</html>
```

**Use CSS to style the form elements and define layout.** You can customize fonts, colors, and positioning for a visually appealing form.

In the JavaScript file (`script.js`), you can add basic functionalities like validation to ensure users enter required information before submitting the form.

**Start with simple editing, then experiment with adding functionalities like error messages or basic animation using JavaScript.**

**By completing these self-study exercises, you'll gain a deeper understanding of networking, load balancing, and web form development.**
