# Windows 11 Troubleshooting Lab

## Project Overview

This repository documents hands-on Windows 11 troubleshooting exercises performed in a virtualized environment using Oracle VirtualBox.

The purpose of this project is to develop practical IT support skills by simulating common end-user problems, investigating their causes, implementing solutions, and verifying system functionality.

Each lab follows a structured troubleshooting methodology similar to procedures used by IT Help Desk technicians.

## Lab Environment

* **Operating System:** Windows 11
* **Virtualization Platform:** Oracle VirtualBox
* **Virtual Machine RAM:** 6 GB
* **Virtual Processors:** 2
* **Tools:** Windows Task Manager, PowerShell, Windows troubleshooting utilities

## Troubleshooting Methodology

Each exercise follows five stages:

1. **Identify the Problem** — Gather information about the reported issue.
2. **Investigate** — Examine system performance, processes, and relevant settings.
3. **Determine the Cause** — Identify potential sources of the problem.
4. **Implement a Solution** — Apply appropriate corrective actions.
5. **Verify and Document** — Confirm the issue is resolved and record findings.

## Completed Labs

### Lab 001 — Windows Performance Troubleshooting

**Scenario:** A Windows 11 user experiences slow system performance while using multiple browser tabs.

**Objective:** Investigate elevated CPU and memory usage, identify resource-intensive processes, and restore normal system performance.

**Tools Used:** Windows Task Manager, Microsoft Edge

**Results:**

* Observed CPU utilization reaching approximately 80% during the simulated workload.
* Identified Microsoft Edge consuming 28.9% CPU and approximately 780 MB RAM.
* Reduced CPU utilization to approximately 4% by closing unnecessary browser tabs.
* Verified improved system responsiveness.

Detailed troubleshooting steps and screenshots are documented in the Lab 001 folder.

## Skills Demonstrated

* Windows 11 troubleshooting
* CPU and memory performance monitoring
* Process identification and analysis
* Resource utilization troubleshooting
* Virtual machine management
* Technical documentation
* Help Desk troubleshooting methodology

## Project Goals

This repository will continue to expand with additional Windows troubleshooting scenarios to strengthen practical IT support skills and demonstrate hands-on technical experience.

---

**Author:** Jarrett Justice
**Focus:** IT Support | Help Desk | Cybersecurity


---

## Screenshots & Supporting Evidence

### Initial System Baseline

**CPU Baseline**

![CPU Baseline](screenshots/01-CPU-Baseline.png)

**Memory Baseline**

![Memory Baseline](screenshots/02-Memory-Baseline.png)

**Disk Baseline**

![Disk Baseline](screenshots/03-Disk-Baseline.png)

**Processes Baseline**

![Processes Baseline](screenshots/04-Processes-Baseline.png)

### Simulated Performance Issue

**CPU Utilization Under Load**

![CPU Under Load](screenshots/05-CPU-Under-Load.png)

**Identifying the Resource-Intensive Process**

![High CPU Processes](screenshots/06-High-CPU-Processes.png)

### Resolution Verification

**CPU Utilization After Corrective Action**

![CPU After Fix](screenshots/07-CPU-After-Fix.png)
