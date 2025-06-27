#  Firewall Configuration Task – Windows (GUI-Based)

This document outlines the steps to configure Windows Defender Firewall to block and allow specific ports, using the GUI.

---

##  Steps Followed

### 1. Open Firewall Configuration Tool

- Press `Windows + R`, type `wf.msc`, and hit **Enter**.
- This opens **Windows Defender Firewall with Advanced Security**.

---

### 2. List Current Firewall Rules

- In the left panel, click on **Inbound Rules**.
- You will see a list of currently defined rules (enabled/disabled, profiles, etc.).

### 3. Add Rule to **Block Inbound Port 23 (Telnet)**

1. Click **New Rule** on the right panel.
2. Choose **Port**, click **Next**.
3. Select **TCP** and enter:
   ```text
   23
Select:
Block the connection
Choose:
Domain, Private, and Public
Name the rule:
Block Telnet
Click Finish.

## 4. Test the Rule
Open Command Prompt and run:
telnet localhost 23
It should fail to connect, indicating that the port is successfully blocked.
### 5. (Optional) Add Rule to Allow SSH (Port 22)
Follow the same steps as above, but:

Port: 22

Action: Allow the connection

Name: Allow SSH

## 6. Remove Test Rule
To remove the rule:

Go to Inbound Rules.

Right-click Block Telnet.

Click Delete.

## Summary: How Firewall Filters Traffic
A firewall acts as a protective barrier between your computer and the network:

It filters traffic based on:

IP address

Port number

Protocol

It can:

Block unwanted or unsafe connections

Allow necessary traffic like SSH or HTTP

In this task:

Port 23 was blocked to stop insecure Telnet access.

Port 22 was allowed to enable secure SSH connections.

---

Let me know if you want the markdown file exported or converted into PDF
