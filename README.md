# Task 7 – Monitor System Resources using Netdata

## Overview
For this task, I used **Netdata** to monitor real-time system metrics such as CPU, RAM, disk I/O, and Docker container activity.

## Setup Summary
- Launched an AWS EC2 instance (Amazon Linux 2023)
- Installed Docker
- Ran Netdata using the official Docker container
- Opened port `19999` in EC2 security group to access the dashboard

## Docker Command Used
```bash
docker run -d --name=netdata -p 19999:19999 --cap-add=SYS_PTRACE --security-opt apparmor=unconfined netdata/netdata
