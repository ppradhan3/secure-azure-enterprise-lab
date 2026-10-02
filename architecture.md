# Architecture Design

## 1. Architecture Overview

The environment uses Microsoft Azure to host a segmented enterprise-style infrastructure environment.

The architecture separates management, application, and data workloads into dedicated network segments while using Microsoft Entra ID and Azure RBAC for centralized identity and authorization.

The design prioritizes:

- Least privilege
- Network segmentation
- Restricted administrative access
- Centralized monitoring
- Reproducible infrastructure
- Cost-conscious resource sizing
- Operational simplicity

---

## 2. High-Level Architecture

```text
                           Internet
                              |
                              |
                    Azure Public Entry
                              |
                     Management Access
                              |
                    +---------+---------+
                    |    Azure VNet     |
                    |   10.20.0.0/16    |
                    |                   |
                    |  +-------------+  |
                    |  | Management  |  |
                    |  | 10.20.1.0/24|  |
                    |  |             |  |
                    |  | Windows     |  |
                    |  | Server      |  |
                    |  +-------------+  |
                    |                   |
                    |  +-------------+  |
                    |  | Application |  |
                    |  | 10.20.2.0/24|  |
                    |  |             |  |
                    |  | Linux VM    |  |
                    |  +-------------+  |
                    |                   |
                    |  +-------------+  |
                    |  | Data        |  |
                    |  | 10.20.3.0/24|  |
                    |  |             |  |
                    |  | Storage     |  |
                    |  +-------------+  |
                    |                   |
                    |  +-------------+  |
                    |  | Monitoring  |  |
                    |  | 10.20.4.0/24|  |
                    |  +-------------+  |
                    +-------------------+

                         |
                         |
                  Microsoft Entra ID
                         |
              +----------+----------+
              |                     |
           Users                  Admins
              |                     |
             MFA                   RBAC
