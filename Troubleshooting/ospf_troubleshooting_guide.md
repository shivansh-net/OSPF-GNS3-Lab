# OSPF Troubleshooting Guide

## Overview
This document provides guide for troubleshooting OSPF-related issues in a GNS3 lab environment. It includes common problems and analysis techniques to diagnose and resolve OSPF misconfigurations and failures.

---

## 1. OSPF Neighbor Issues

### Symptoms:
- OSPF neighbors not forming.
- Stuck in INIT, EXSTART, or EXCHANGE state.

### Possible Causes:
- Mismatched area number.
- Mismatched IP address settings.
- Same Router-ID among different routers.
- Different OSPF hello/dead timers.
- Incorrect OSPF network type.

### Debugging Commands:
```sh
show ip protocols
show ip ospf interface 
show ip ospf neighbor
```

### Solutions:
- Verify interface IP address settings.
- Ensure hello and dead intervals match.
- Check OSPF network types and adjust if necessary.
- Verify area number.
- Look for same Router-IDs used in different Routers.

---

## 2. Missing OSPF Routes

### Symptoms:
- Routes not appearing in `show ip route ospf`.

### Possible Causes:
- Interface is shutdown.

### Debugging Commands:
```sh
show ip interface brief
```

### Solutions:
- Verify if the interface is administratively down. 

---

## Conclusion
This guide provides structured troubleshooting techniques to diagnose and resolve OSPF-related issues. Utilizing debugging commands and Wireshark packet analysis will help identify and fix problems efficiently.
