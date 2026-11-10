# Spanning Tree Protocol (STP) and Rapid Spanning Tree Protocol (RSTP)

## Project Overview

This project demonstrates my hands-on experience configuring, monitoring, and troubleshooting Spanning Tree Protocol (STP) using Cisco Packet Tracer.

The objective is to understand how STP prevents Layer 2 switching loops and maintains network redundancy.

## Topics Covered

* Root Bridge Election
* Root Ports (RP) and Designated Ports (DP)
* Alternate Ports
* Rapid Spanning Tree Protocol (RSTP)

## Lab Objectives

1. Understand how switches elect a Root Bridge using Bridge ID.
2. Identify Root Ports, Designated Ports, and Alternate Ports.
3. Observe how STP prevents Layer 2 switching loops.

## Cisco IOS Commands

### Configuring STP and RSTP
1. spanning-tree vlan 1 root primary (Ensures the selected Switch becomes the Root Bridge)
2. spanning-tree vlan 1 root secondary (Ensures the selected Switch becomes the Secondary Bridge) 
3. spanning-tree vlan 1 mode rapid-pvst (Enables RSTP)

### Verify STP
1. show spanning-tree
2. show spanning-tree vlan 1
3. show spanning-tree summary

### Alternative Configuration Commands
1. spanning-tree vlan 1 priority 0 (The Lowest BID, automatically ensures the selected Switch becomes the Root)


## Lab Verification

Cisco Packet Tracer was used to examine STP port roles, verify switch configurations, and observe how different STP protection mechanisms behave.

## Tools Used

* Cisco Packet Tracer
* Cisco IOS CLI
* Cisco Layer 2 Switches

## Learning Outcomes

These labs are intended to strengthen my practical understanding of Layer 2 switching, network redundancy, STP behaviour, and network troubleshooting.
