# Lab 001 — Windows 11 Performance Troubleshooting

## 1. Lab Overview

**Lab Type:** Windows Performance Troubleshooting
**Environment:** Windows 11 Virtual Machine
**Virtualization Platform:** Oracle VirtualBox
**Difficulty:** Beginner
**Status:** Completed

### Objective

Simulate a Windows 11 performance issue, investigate system resource utilization, identify a resource-intensive application, implement corrective action, and verify improved system performance.

This lab demonstrates a structured troubleshooting approach applicable to entry-level IT Help Desk and Desktop Support roles.

---

## 2. Help Desk Scenario

**Simulated User Report:**

"My computer becomes noticeably slower when I have multiple browser tabs open. Applications take longer to respond, and overall system performance decreases."

**Troubleshooting Goal:**

Determine which system resources are experiencing increased utilization, identify contributing processes, and restore normal performance without restarting the operating system.

---

## 3. Lab Environment

| Component                       | Configuration        |
| ------------------------------- | -------------------- |
| Operating System                | Windows 11           |
| Virtualization Software         | Oracle VirtualBox    |
| Virtual Processors              | 2                    |
| Allocated Memory                | 6 GB                 |
| Virtual Disk                    | 80 GB                |
| Primary Diagnostic Tool         | Windows Task Manager |
| Application Used for Simulation | Microsoft Edge       |

---

## 4. Establishing a Performance Baseline

Before simulating the performance issue, I used Windows Task Manager to document normal system resource utilization.

### Baseline Observations

* **CPU Utilization:** Approximately 1–4%
* **Memory Utilization:** Approximately 42%
* **Disk Activity:** Low, without evidence of sustained saturation
* **System Responsiveness:** Normal

These measurements provided a reference point for comparing system performance during the simulated workload.

### Evidence Collected

* `01-CPU-Baseline.png`
* `02-Memory-Baseline.png`
* `03-Disk-Baseline.png`
* `04-Processes-Baseline.png`

---

## 5. Reproducing the Performance Issue

To simulate a realistic end-user performance problem, I opened multiple Microsoft Edge browser tabs and navigated between websites.

As additional browser activity occurred, I observed increased system resource utilization and reduced responsiveness.

### Observations During Simulation

* CPU utilization reached approximately **80%** at its highest observed point.
* CPU utilization measured **46%** in the performance screenshot.
* Memory utilization increased to approximately **62%**.
* The virtual machine became noticeably slower during browser activity.

**Evidence:** `05-CPU-Under-Load.png`

---

## 6. Investigating the Cause

I opened Windows Task Manager and navigated to the Processes tab to identify applications consuming system resources.

### Findings

| Metric                                    | Observation    |
| ----------------------------------------- | -------------- |
| Total CPU Utilization                     | 62%            |
| Total Memory Utilization                  | 62%            |
| Highest Visible CPU-Consuming Application | Microsoft Edge |
| Microsoft Edge CPU Utilization            | 28.9%          |
| Microsoft Edge Memory Consumption         | 780.3 MB       |
| Microsoft Edge Processes                  | 18             |

### Analysis

Microsoft Edge was the largest visible contributor to CPU utilization in the captured Task Manager results.

The browser workload also increased memory consumption.

Because the virtual machine was configured with two virtual processors and 6 GB of RAM, the increased resource demand contributed to noticeable performance degradation.

**Evidence:** `06-High-CPU-Processes.png`

---

## 7. Implementing the Resolution

After identifying Microsoft Edge as a significant contributor to resource consumption, I reduced the browser workload.

### Corrective Actions

1. Closed unnecessary browser tabs.
2. Allowed background browser activity to decrease.
3. Monitored resource utilization using Windows Task Manager.
4. Evaluated system responsiveness after the changes.

The troubleshooting process did not require restarting Windows.

---

## 8. Verifying the Resolution

After reducing the browser workload, I reviewed Task Manager to confirm whether resource utilization decreased.

### Before and After Comparison

| Metric                            | During Issue | After Resolution |
| --------------------------------- | ------------ | ---------------- |
| Total CPU Utilization             | 62%          | 4%               |
| Total Memory Utilization          | 62%          | 48%              |
| Microsoft Edge CPU Utilization    | 28.9%        | 0%               |
| Microsoft Edge Memory Consumption | 780.3 MB     | 135.6 MB         |
| Disk Utilization                  | 2%           | 0%               |
| System Responsiveness             | Sluggish     | Improved         |

### Verification Results

CPU utilization decreased significantly after the browser workload was reduced.

Memory utilization also decreased, and the virtual machine became noticeably more responsive.

These observations support the conclusion that excessive browser activity was a significant contributor to the simulated performance issue.

**Evidence:** `07-CPU-After-Fix.png`

---

## 9. Root Cause Analysis

**Identified Contributing Factor:** Increased system resource consumption associated with multiple active Microsoft Edge browser tabs.

**Impact:** Elevated CPU and memory utilization accompanied by reduced system responsiveness.

**Resolution:** Reduced browser activity by closing unnecessary tabs.

**Outcome:** Resource utilization returned to lower levels, and system responsiveness improved.

The evidence supports browser activity as a contributing factor, although it does not establish CPU utilization as the sole cause of the slowdown.

---

## 10. Lessons Learned

This exercise reinforced several important IT support concepts:

* Establishing a performance baseline before troubleshooting.
* Using Task Manager to investigate CPU, memory, and disk utilization.
* Identifying resource-intensive applications.
* Comparing system performance before and after corrective action.
* Verifying that a solution improves the reported problem.
* Documenting troubleshooting procedures and results.

### Skills Demonstrated

* Windows 11 administration fundamentals
* Performance monitoring
* CPU and memory troubleshooting
* Process analysis
* Problem isolation
* Help Desk troubleshooting methodology
* Technical documentation

---

## 11. Conclusion

Successfully reproduced and investigated a Windows 11 performance slowdown in a virtualized environment.

By monitoring resource utilization, identifying Microsoft Edge as a significant contributor, reducing the browser workload, and verifying improved system performance, I completed a structured troubleshooting exercise.

This lab demonstrates foundational diagnostic and problem-solving skills relevant to entry-level IT support positions.

---

**Lab Status:** Completed
**Documented By:** Jarrett Justice
**Project:** Windows 11 Troubleshooting Lab
