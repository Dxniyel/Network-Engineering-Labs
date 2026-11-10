# EtherChannel Configuration

### 1. Static EtherChannel
**File:** `Static Etherchannel.pkt`

This lab demonstrates how to configure Static EtherChannel between Cisco switches.

- Bundle multiple physical interfaces into a single logical link.
- Configure Static EtherChannel using `channel-group 1 mode on`.
- Understand how EtherChannel provides increased bandwidth and redundancy.
- Verify EtherChannel configurations using `show etherchannel summary`.

### 2. Port Aggregation Protocol (PAgP) EtherChannel
**File:** `Port Aggregation Protocol (PAgP) Etherchannel.pkt`

This lab demonstrates how to configure EtherChannel using Cisco's proprietary PAgP protocol.

- Configure EtherChannel using `desirable` and `auto` modes.
- Understand how PAgP dynamically negotiates EtherChannel formation.
- Bundle multiple physical interfaces into a single logical Port-Channel.
- Verify EtherChannel status using `show etherchannel summary`.

### 3. Link Aggregation Control Protocol (LACP) EtherChannel
**File:** `Link Aggregation Control Protocol (LACP) Etherchannel.pkt`

This lab demonstrates how to configure EtherChannel using the IEEE-standard LACP protocol.

- Configure EtherChannel using `active` and `passive` modes.
- Understand how LACP dynamically negotiates EtherChannel formation.
- Combine multiple physical interfaces into a single logical link.
- Verify EtherChannel configurations using `show etherchannel summary`.

### 4. Layer 3 EtherChannel
**File:** `Layer 3 Etherchannel.pkt`

This lab demonstrates how to configure a Layer 3 EtherChannel between multilayer switches.

- Configure EtherChannel as a routed logical interface.
- Disable Layer 2 switching using `no switchport`.
- Assign IP addresses directly to Port-Channel interfaces.
- Enable IP routing for communication between different networks.
- Verify connectivity and EtherChannel status.

### 5. PAgP, LACP and Layer 3 EtherChannel Configuration
**File:** `PAgP, LACP, Layer 3 Etherchannel Configuration.pkt`

This lab demonstrates the implementation of multiple EtherChannel technologies within a single network topology.

- Configure PAgP EtherChannel using Cisco's proprietary negotiation protocol.
- Configure LACP EtherChannel using the IEEE-standard negotiation protocol.
- Implement Layer 3 EtherChannel for routed communication between switches.
- Understand the differences between Layer 2 and Layer 3 EtherChannel.
- Verify EtherChannel configurations, routing and network connectivity.
