# Understanding OSPF Packet Types in Wireshark

OSPF uses five main packet types:

| Packet Type | Description |
|-------------|------------|
| **Hello (Type 1)** | Establishes and maintains neighbor relationships. |
| **Database Description (DBD) (Type 2)** | Summarizes LSAs for synchronization. |
| **Link-State Request (Type 3)** | Requests missing LSAs from neighbors. |
| **Link-State Update (Type 4)** | Distributes new LSA information. |
| **Link-State Acknowledgment (Type 5)** | Confirms receipt of LSAs. |

## Example: OSPF Hello Packet Fields
Captured in `01_OSPF_Hello_Packets.pcapng`:
- **OSPF Version:** 2
- **Area ID:** 0.0.0.0
- **Hello Interval:** 10 seconds
- **Dead Interval:** 40 seconds

## Example: OSPF LSA Update Fields
Captured in `02_OSPF_LSA_Updates.pcapng`:
- **LSA Type:** 1 (Router LSA)
- **Advertising Router:** 10.1.1.1
- **LS Age:** 30 seconds
