# Spanning Tree Protocol (STP) – Loop Guard & Root Guard

This repository contains Cisco Packet Tracer labs demonstrating how **Loop Guard** and **Root Guard** protect network switches from potential Layer 2 issues.

## 1. Loop Guard (STP)

**Description:**

Loop Guard is an STP protection feature that prevents network loops from occurring when a switch unexpectedly stops receiving BPDUs (Bridge Protocol Data Units).

Normally, switches exchange BPDUs to maintain a loop-free network topology. If a port that should be receiving BPDUs suddenly stops receiving them, STP may incorrectly transition that port into a Designated Port, potentially creating a network loop.

Loop Guard prevents this by placing the affected port into a **loop-inconsistent state**, blocking traffic until BPDUs are received again.

**Key Points:**

* Prevents network loops caused by missing BPDUs.
* Typically configured on Root Ports and Alternate Ports.
* Places affected ports into a loop-inconsistent state.
* Automatically restores the port when BPDUs are received again.

**Cisco Configuration:**

```bash
Switch(config)# interface gigabitEthernet0/1
Switch(config-if)# spanning-tree guard loop
```

**Verification:**

```bash
Switch# show spanning-tree inconsistentports
```

---

## 2. Root Guard (STP)

**Description:**

Root Guard is an STP protection feature that prevents unauthorized or unexpected switches from becoming the Root Bridge.

In a network, switches participate in STP elections by exchanging BPDUs. If another switch advertises a superior BPDU, it may take over as the Root Bridge.

Root Guard prevents this by placing the receiving port into a **root-inconsistent state** whenever a superior BPDU is detected.

This ensures that the designated Root Bridge remains in control of the STP topology.

**Key Points:**

* Prevents unexpected Root Bridge changes.
* Typically configured on Designated Ports facing downstream switches.
* Places affected ports into a root-inconsistent state when superior BPDUs are received.
* Automatically restores the port when superior BPDUs are no longer received.

**Cisco Configuration:**

```bash
Switch(config)# interface gigabitEthernet0/1
Switch(config-if)# spanning-tree guard root
```

**Verification:**

```bash
Switch# show spanning-tree inconsistentports
```

---

## Summary

| Feature       | Loop Guard                   | Root Guard                               |
| ------------- | ---------------------------- | ---------------------------------------- |
| Purpose       | Prevent network loops        | Prevent unauthorized Root Bridge changes |
| Trigger       | Expected BPDUs stop arriving | Superior BPDU received                   |
| Port State    | Loop-inconsistent            | Root-inconsistent                        |
| Recovery      | Automatic when BPDUs return  | Automatic when superior BPDUs stop       |
| Typical Ports | Root / Alternate Ports       | Designated Ports                         |
