# Findings

## Summary

The cybersecurity laboratory was successfully implemented and validated.

---

## Key Findings

### Virtualization

Oracle VirtualBox provided an isolated environment for security testing.

### Networking

NAT and Host-Only networking enabled Internet access while maintaining laboratory isolation.

### Docker

Docker simplified the deployment of OWASP Juice Shop.

### Nmap

The application was successfully detected on TCP port **3000**, confirming that the service was active.

### Burp Suite

HTTP requests and responses were successfully captured, demonstrating proper communication between the browser and the web application.

### Wireshark

Packet analysis confirmed communication over the loopback interface (`127.0.0.1`) using TCP port **3000**.

---

## Conclusion

The laboratory environment functioned as expected and provides a reliable platform for learning network security, web application security, and traffic analysis using industry-standard tools.