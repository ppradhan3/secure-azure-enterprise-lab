# Secure Azure Enterprise Infrastructure Lab

## 1. Project Overview

This project simulates the design and operation of a secure cloud environment for a small organization transitioning workloads to Microsoft Azure.

The environment is designed for approximately 50 employees and includes centralized identity, segmented networking, Windows and Linux workloads, security controls, monitoring, automation, backup/recovery, and operational procedures.

The project is intentionally designed to demonstrate practical cloud infrastructure and systems administration skills rather than application software development.

---

## 2. Business Scenario

A 50-person organization is migrating selected internal infrastructure to Microsoft Azure.

The organization requires:

- Centralized identity and access management
- Secure administrative access
- Internal Windows and Linux workloads
- Segmented network architecture
- Controlled communication between workloads
- Centralized monitoring and logging
- Automated infrastructure deployment
- Backup and recovery capabilities
- Documented incident response procedures
- Cost-conscious cloud resource management

The environment should be secure, reproducible, observable, and maintainable by a small IT infrastructure team.

---

## 3. Project Objectives

The project will demonstrate the ability to:

1. Design a cloud network architecture in Azure.
2. Deploy and configure Windows and Linux workloads.
3. Implement Microsoft Entra ID and role-based access control.
4. Apply network segmentation and security controls.
5. Implement centralized monitoring and logging.
6. Automate infrastructure deployment and administrative tasks.
7. Establish backup and recovery procedures.
8. Troubleshoot simulated infrastructure failures.
9. Document operational procedures and technical decisions.
10. Apply security, reliability, operational, performance, and cost considerations throughout the environment.

---

## 4. Functional Requirements

### 4.1 Identity and Access

The environment must provide:

- Microsoft Entra ID identity management
- User and group organization
- Role-based access control (RBAC)
- Multi-factor authentication where supported
- Separation of administrative and standard-user access
- Least-privilege administrative permissions
- Documented access assignments

### 4.2 Networking

The environment must include:

- An Azure Virtual Network
- Multiple subnets
- Defined IP address ranges
- Network Security Groups (NSGs)
- Controlled inbound and outbound traffic
- Internal communication between approved workloads
- Restricted administrative access
- Documented network flows

### 4.3 Compute

The environment must include:

- At least one Windows Server workload
- At least one Linux workload
- Appropriate network interfaces
- Secure administrative access
- Basic system hardening
- Automated or documented configuration procedures

### 4.4 Systems Administration

The environment should demonstrate:

- Windows Server administration
- Linux administration
- DNS configuration
- User and group administration
- System configuration
- Patch/update procedures
- PowerShell and Bash automation

### 4.5 Monitoring and Logging

The environment must provide:

- Centralized log collection
- VM monitoring
- Basic infrastructure health monitoring
- Configured alerts
- Investigation of selected security or operational events
- Documented monitoring procedures

### 4.6 Security

The environment must implement:

- Network segmentation
- Least-privilege access
- RBAC
- MFA where applicable
- Restricted management access
- Secure credential/secrets handling
- Basic workload hardening
- Security logging
- Documented security controls

### 4.7 Automation

The project must include infrastructure or configuration automation using:

- Terraform
- Azure CLI
- PowerShell and/or Bash

Infrastructure should be reproducible from code wherever practical.

### 4.8 Backup and Recovery

The environment must include:

- A defined backup strategy
- Recovery objectives
- At least one documented recovery procedure
- A simulated recovery scenario
- Documentation of limitations and assumptions

---

## 5. Non-Functional Requirements

### Security

The environment should minimize unnecessary exposure and follow least-privilege principles.

Administrative services should not be unnecessarily exposed to the public internet.

### Reliability

The environment should include documented procedures for identifying and recovering from common infrastructure failures.

### Observability

Important infrastructure components should generate sufficient logs and metrics to support troubleshooting.

### Maintainability

Infrastructure configuration should be documented and reproducible.

### Cost Management

Resources should be sized appropriately for a lab environment.

The project should avoid unnecessary paid services and include cost-control measures such as resource cleanup and automatic shutdown where appropriate.

### Performance

Workloads should have sufficient resources for their intended lab functions without unnecessary over-provisioning.

---

## 6. Security Requirements

The following security principles will guide the design:

- Least privilege
- Defense in depth
- Network segmentation
- Strong authentication
- Restricted administrative access
- Centralized logging
- Secure credential management
- Minimal public exposure
- Regular access review
- Documented security decisions

Security controls should be justified rather than implemented solely for demonstration.

---

## 7. Operational Requirements

The project must include documentation for:

- Initial deployment
- Administrative access
- User provisioning
- System maintenance
- Monitoring
- Backup/recovery
- Troubleshooting
- Incident response
- Resource cleanup

---

## 8. Incident Scenarios

The completed environment will be used to simulate and document infrastructure incidents.

Initial scenarios will include:

### Incident 001 — DNS Failure

An internal workload cannot resolve a required hostname.

Objective:

- Identify the failure
- Determine root cause
- Restore service
- Document investigation and remediation

### Incident 002 — Network Access Failure

A workload that previously communicated successfully becomes unreachable.

Objective:

- Trace the network path
- Investigate NSG and routing configuration
- Identify the root cause
- Restore approved connectivity

### Incident 003 — Authentication Failure

A user is unable to authenticate to a required resource.

Objective:

- Investigate identity and authorization
- Determine whether the issue involves authentication or permissions
- Restore appropriate access
- Document the resolution

### Incident 004 — Workload Failure

A server or application becomes unavailable.

Objective:

- Detect the failure
- Determine whether the issue is infrastructure, operating system, or service related
- Restore service
- Document the incident lifecycle

---

## 9. Documentation Deliverables

The final project will include:

- Architecture diagram
- Network diagram
- Identity/RBAC model
- Network/subnet plan
- NSG rules
- Security controls
- Threat model
- Terraform infrastructure
- Automation scripts
- Monitoring configuration
- KQL queries
- Deployment runbook
- Backup/recovery procedure
- Incident response runbooks
- Incident postmortems

---

## 10. Success Criteria

The project will be considered complete when:

- Infrastructure can be deployed reproducibly from code.
- Network architecture is documented.
- Identity and access controls are documented.
- Windows and Linux workloads are operational.
- Monitoring and logging are functional.
- Security controls are implemented and justified.
- At least four infrastructure incidents have been investigated and documented.
- Backup/recovery procedures have been tested.
- Infrastructure can be safely decommissioned.
- The complete architecture can be explained without relying on the Azure Portal.
