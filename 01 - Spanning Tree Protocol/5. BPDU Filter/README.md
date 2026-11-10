# Bridge Protocol Data Unit Filter (BPDU Filter)

## Description

This Cisco Packet Tracer lab demonstrates how **BPDU Filter** controls the transmission and reception of Bridge Protocol Data Units (BPDUs) on switch interfaces.

BPDU Filter is an STP feature that can prevent switches from exchanging BPDUs, allowing administrators to control STP participation on specific interfaces.

For example, when connecting a customer network to an ISP network, BPDU Filter can be used to prevent STP information from being exchanged between the two networks.

When BPDU Filter is explicitly enabled on an interface, the switch stops sending and processing BPDUs on that interface.

## Key Points

* Prevents the sending and processing of BPDUs on protected interfaces.
* Can prevent STP information from being exchanged between separate networks.
* Does not place interfaces into an err-disabled state.
* Does not place interfaces into a root-inconsistent or loop-inconsistent state.
* Must be configured carefully because suppressing BPDUs can introduce Layer 2 loops.

## Cisco Configuration

To enable BPDU Filter on a specific interface:

```bash
Switch(config)# interface gigabitEthernet0/1
Switch(config-if)# spanning-tree bpdufilter enable
```

To disable BPDU Filter:

```bash
Switch(config)# interface gigabitEthernet0/1
Switch(config-if)# no spanning-tree bpdufilter enable
```

## Verification Commands

```bash
show spanning-tree summary
show spanning-tree interface gigabitEthernet0/1 detail
show running-config interface gigabitEthernet0/1
```

## Important Note

BPDU Filter behaves differently depending on how it is configured.

**Interface-level BPDU Filter:**

* Suppresses incoming and outgoing BPDUs on the configured interface.
* Does not automatically disable itself when BPDUs are received.

**Global BPDU Filter (PortFast):**

* Applies to PortFast-enabled interfaces.
* Allows the port to lose its PortFast operational status and resume normal STP participation when a BPDU is received.

## Conclusion

BPDU Filter allows network administrators to control BPDU exchanges between switches and network segments.

Although useful in specific scenarios, it should be implemented carefully because preventing BPDU exchanges can interfere with STP's ability to detect and prevent network loops.
