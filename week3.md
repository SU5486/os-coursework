# Week 3 – Application Selection for Performance Testing

## 1. Introduction

The aim of Week 3 was to select suitable applications to evaluate the performance of the Ubuntu Server under different workload types. These applications were chosen to represent common server workloads such as CPU-intensive tasks, memory usage, disk I/O operations, and network activity.

This planning stage ensures that performance testing carried out in later weeks is structured, meaningful, and representative of real-world server usage.

---

## 2. Application Selection Strategy

To evaluate operating system behaviour effectively, applications were selected based on the type of system resource they primarily stress. Each application focuses on a different aspect of system performance, allowing detailed analysis and comparison.

The selected applications are lightweight, widely used, and suitable for command-line execution on a headless server.

---

## 3. Application Selection Matrix

| Application | Workload Type | Reason for Selection |
|------------|--------------|---------------------|
| stress-ng | CPU / Memory | Used to generate controlled CPU and memory load |
| fio | Disk I/O | Used to measure disk read/write performance |
| iperf3 | Network | Used to test network throughput and latency |
| nginx | Server Application | Represents a real-world server workload |

---

## 4. Installation Commands

All applications will be installed remotely via SSH using the Ubuntu package manager.

*sudo apt update*

*sudo apt install stress-ng fio iperf3 nginx -y* 

These commands ensure consistent and repeatable installation of testing tools.

## 5. Expected Resource Profiles

Each application is expected to impact system resources in different ways:

* *stress-ng:*
 High CPU usage and increased memory consumption depending on test parameters.

* *fio:*
 Increased disk read/write activity and I/O wait times.

* *iperf3:*
 High network throughput and increased network interface usage.

*  *nginx:*
 Moderate CPU and memory usage while responding to HTTP requests.

Understanding these expected profiles allows comparison between anticipated and actual system behaviour during testing.

## 6. Monitoring Strategy

System monitoring will be performed remotely using SSH from the workstation. The following tools will be used to observe system performance:

* **top** and **htop** for CPU and memory usage

* **vmstat** for system activity and memory statistics

* **iostat** for disk I/O performance

* **ss** and **ip** for network statistics

Monitoring will take place during baseline conditions, under application load, and after any optimisation changes.

## 7. Testing Approach Summary

Each application will be tested individually to isolate its impact on system performance. Metrics collected during testing will be recorded and compared to baseline values. This approach ensures accurate identification of bottlenecks and allows meaningful performance analysis.

## 8. Reflection

This week helped clarify how different applications place varying demands on system resources. Selecting appropriate tools in advance ensures that performance testing in later weeks is structured and relevant. This planning stage also reinforced the importance of understanding expected system behaviour before analysing real performance data. 

