# Bridge Protocol Data Unit Guard (BPDU Guard)

## Description

This Cisco Packet Tracer lab demonstrates how **BPDU Guard** protects a network from unauthorized switches connecting to ports intended for end devices.

BPDU Guard is an STP security feature commonly configured alongside PortFast on access ports connected to PCs, printers, and servers.

When BPDU Guard detects an incoming BPDU on a protected ported, it immiately places the interface into an **err-disabled state**, preventing the connected switch from affecting the existing STP topology.

## Key Points

* Protects access ports from unexpected BPDU messages.
* Commonly configured together with PortFast.
* Automatically disables the interface when a BPDU is detected.
* Prevents unauthorized switches from participating in STP through the protected port.
* Requires manual intervention or configured automatic recovery to restore the interface.

## Cisco Configuration

```bash
Switch(config)# interface fastEthernet0/1
Switch(config-if)# spanning-tree portfast
Switch(config-if)# spanning-tree bpduguard enable
```

## Verification Commands

```bash
show spanning-tree summary
show interfaces status
show interfaces status err-disabled
show errdisable recovery
```

## Recovery

To manually restore an err-disabled interface after removing the cause:

```bash
Switch(config)# interface fastEthernet0/1
Switch(config-if)# shutdown
Switch(config-if)# no shutdown
```

## Conclusion

BPDU Guard helps maintain a stable STP topology by shutting down protected ports that receive unexpected BPDUs. It is particularly useful for securing access ports connected to end devices.
