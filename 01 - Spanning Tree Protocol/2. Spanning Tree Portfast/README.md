# Spanning Tree PortFast Configuration Lab

## Overview

This lab demonstrates how to configure and verify PortFast using Cisco Packet Tracer.

PortFast allows switch ports connected to end devices to immediately enter the Forwarding state, bypassing the traditional STP Listening (15 seconds) and Learning (15 seconds) states.

## Network Topology

* 3 Cisco Catalyst 2960 switches
* 1 PC
* 1 Virtualization Server
* Redundant switch connections for STP testing

## Configuration

**1. Enable PortFast on an interface**
```bash
interface fa0/1
spanning-tree portfast
```

**2. Enable PortFast globally**
```bash
spanning-tree portfast default
```

**3. Disable PortFast**
```bash
interface fa0/1
spanning-tree portfast disable
```

**4. Enable PortFast on a trunk interface**
```bash
interface gi0/2
spanning-tree portfast edge trunk
```

## Verification Commands
```bash
show spanning-tree interface gi0/2 detail
show spanning-tree summary
```

## Key Learning Points

* PortFast allows end-device ports to forward traffic immediately.
* PortFast can be configured per interface or globally.
* PortFast trunk can be used for suitable endpoints, such as virtualization servers and ROAS routers.
* PortFast does not disable STP or prevent BPDU reception.
* PortFast should not be enabled on normal switch-to-switch connections.

## Tools Used

Cisco Packet Tracer | Cisco IOS CLI | Catalyst 2960
