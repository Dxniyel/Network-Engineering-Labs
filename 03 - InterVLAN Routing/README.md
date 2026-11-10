### 3. Router-on-a-Stick (ROAS) Configuration
**File:** `Router-On-A-Stick Configuration.pkt`

This lab demonstrates how to configure inter-VLAN routing using a router and a Layer 2 switch.

- Configure VLANs and assign access ports to end devices.
- Configure an 802.1Q trunk link between the router and switch.
- Create router subinterfaces for each VLAN.
- Assign IP addresses to subinterfaces to serve as default gateways.
- Enable communication between devices in different VLANs.

### 4. Inter-VLAN Routing via Layer 3 Switch (SVI)
**File:** `InterVlan Routing via Layer 3 Switch (SVI).pkt`

This lab demonstrates how to configure inter-VLAN routing using Switch Virtual Interfaces (SVIs) on a Layer 3 switch.

- Create VLANs and assign access ports to end devices.
- Configure an SVI for each VLAN using `interface vlan`.
- Assign IP addresses to SVIs to serve as default gateways.
- Enable Layer 3 routing using `ip routing`.
- Allow devices in different VLANs to communicate without an external router.
