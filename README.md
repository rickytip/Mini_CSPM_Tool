# Mini CSPM (Cloud Security Posture Management) Tool

## Overview

This project is a Python-based mini Cloud Security Posture Management (CSPM) tool designed to identify common cloud misconfigurations in an AWS environment.

The goal of this project is to build hands-on experience with:

- Python scripting

- AWS security services and APIs

- Cloud security posture management concepts

- Writing maintainable, extensible security tooling

This tool performs read-only security checks and produces structured findings that can be used for visibility, reporting, and future automation.

## What This Tool Checks (v0.1)

The initial version focuses on high-impact, commonly abused misconfigurations:

### 1. S3 Public Access

  - Identifies S3 buckets that may be publicly accessible

  - Evaluates public access block settings and policy exposure

### 2. Security Groups with Open Sensitive Ports

  - Detects inbound rules allowing 0.0.0.0/0 or ::/0

  - Flags exposure on sensitive ports (e.g., SSH, RDP, database ports)

### IAM Policy Wildcards

  - Identifies IAM policies with overly permissive permissions

  - Flags wildcard actions and/or wildcard resources in Allow statements

Each check produces structured findings with severity, evidence, and remediation guidance.
