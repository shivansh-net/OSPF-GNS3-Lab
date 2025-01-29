# Wireshark Filters for OSPF Traffic Analysis

## Overview

This document provides useful Wireshark filters for analyzing OSPF traffic in a GNS3 lab environment. These filters help isolate specific OSPF packet types for better troubleshooting and understanding of OSPF operations.

---

## Capture All OSPF Traffic

To display all OSPF packets:

```sh
ospf
```

This filter will show all OSPF-related packets, including Hello, DBD, LSA, and Acknowledgment packets.

---

## Capture Specific OSPF Packet Types

To filter individual OSPF packet types based on the **Wireshark column information**, use:

- **Database Description (DBD) Packets:**
  ```sh
  _ws.col.Info == "DB Description"
  ```

- **Link-State Request (LSR) Packets:**
  ```sh
  _ws.col.Info == "LS Request"
  ```

- **Link-State Update (LSU) Packets:**
  ```sh
  _ws.col.Info == "LS Update"
  ```

- **Link-State Acknowledgment (LSAck) Packets:**
  ```sh
  _ws.col.Info == "LS Acknowledge"
  ```

### **Packet Types Explained:**

| Packet Type                | Description                                     |
| -------------------------- | ----------------------------------------------- |
| **DB Description (DBD)**   | Used in the OSPF database exchange process.     |
| **LS Request (LSR)**       | Requests specific LSAs from a neighbor.        |
| **LS Update (LSU)**        | Carries Link-State Advertisements (LSAs).       |
| **LS Acknowledge (LSAck)** | Confirms receipt of LSAs.                       |

This filter helps focus on OSPF topology exchange packets while excluding Hello packets.

---

## Conclusion

These Wireshark filters will assist in efficiently analyzing OSPF packet exchanges, allowing better debugging and understanding of network behavior.
