# 🛡️ Task 1 – Port Scanning (Cybersecurity Internship)

## 👋 Introduction

This task helped me learn how to discover open ports on devices connected to my local network using `nmap`. It taught me basic network reconnaissance and how to identify what services are exposed to the network.

---

## 🎯 Objective

To scan the local IP range and identify devices with open ports, helping to understand network exposure and potential attack surfaces.

---

## 🛠 Tools Used

- **Nmap 7.95** – Port scanning tool
- **Linux Terminal (Kali Linux)** – Scan execution

---

## 🧪 Command Used

```bash
nmap -sS 192.168.XX.0/24

This command performs a TCP SYN scan over the subnet to find live hosts and their open ports.


---

🖥️ Scan Result Summary

IP Address	Device Name	Open Ports & Services	MAC Vendor

192.168.XX.XXX	jiofiber.local.html	53 (DNS), 80 (HTTP), 443 (HTTPS), 7443, 8080 (HTTP-proxy)	Cloud Network Technology Singapore PTE
192.168.XX.XXX	POCO-M4-5G.lan	None (All ports closed)	Unknown
192.168.XX.XXX	Redmi-13C-5G.lan	None (All ports closed)	Unknown
192.168.XX.XXX	Redmi-TV.lan	1900 (SSDP), 8016, 8080, 8093	Unknown
192.168.XX.XXX	kali.lan	None (All ports closed)	My own device

```



---

🔍 What I Observed

The router (JioFiber) has several open ports, including HTTP(S), DNS, and possibly admin APIs.

The Redmi TV is running multiple media-related services like SSDP and custom HTTP ports.

Other personal mobile devices had all ports closed, which is a good security practice.

My own Kali Linux machine is configured to block all incoming ports, as expected.



---

🔐 Security Risks Identified

Exposed ports on routers and smart devices could allow unauthorized access or remote exploitation.

Port 8080 and 7443 are often used for admin panels – this could be risky if misconfigured or not password-protected.

Smart TVs are often overlooked but may introduce vulnerabilities if not patched or secured.



---

🛡️ Security Recommendations

Change default router passwords and disable unused admin panels.

Place smart/IoT devices like TVs on a separate guest network.

Use a firewall on all personal devices and keep ports closed unless required.

Regularly scan your network to check for new or unexpected devices/services.



---

📝 Outcome

By doing this task, I gained:

Hands-on experience with nmap

Better understanding of local IP ranges and TCP ports

Awareness of real-world risks from exposed network services



---

Made with 💻 by VIMAL KUMAR R
