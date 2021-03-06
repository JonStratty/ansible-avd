
# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed |
| ----------- | ------------------ | ------------------ |
| 25 | 20 | 5 |

### Summary Totals Devices Under Tests

| DUT | Total Tests | Tests Passed | Tests Failed | Categories Failed |
| --- | ----------- | ------------ | ------------ | ----------------- |
| leaf-1a |  25 | 20 | 5 | Interface State, MLAG, BGP |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed |
| ------------- | ----------- | ------------ | ------------ |
| NTP |  1 | 1 | 0 |
| Interface State |  10 | 9 | 1 |
| LLDP Topology |  4 | 4 | 0 |
| MLAG |  1 | 0 | 1 |
| BGP |  6 | 3 | 3 |
| Routing Table |  2 | 2 | 0 |
| Loopback0 Reachability |  1 | 1 | 0 |

## Failed Test Results Summary

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 9 | leaf-1a | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | FAIL | interface status: down - line protocol status: down |
| 16 | leaf-1a | MLAG | MLAG State active & Status connected | MLAG | FAIL | state: inactive - negotiation_status: connecting |
| 18 | leaf-1a | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.128.1 | FAIL | Session state "Active" |
| 20 | leaf-1a | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.1.2 | FAIL | Session state "Active" |
| 22 | leaf-1a | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 1.1.1.2 | FAIL | Session state "Active" |

## All Test Results

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | leaf-1a | NTP | Synchronised with NTP server | NTP | PASS | - |
| 2 | leaf-1a | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet11 - MLAG_PEER_leaf-1b_Ethernet11 | PASS | - |
| 3 | leaf-1a | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet12 - MLAG_PEER_leaf-1b_Ethernet12 | PASS | - |
| 4 | leaf-1a | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_SPINE-1_Ethernet1 | PASS | - |
| 5 | leaf-1a | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_SPINE-2_Ethernet1 | PASS | - |
| 6 | leaf-1a | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel11 - MLAG_PEER_leaf-1b_Po11 | PASS | - |
| 7 | leaf-1a | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 8 | leaf-1a | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 9 | leaf-1a | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | FAIL | interface status: down - line protocol status: down |
| 10 | leaf-1a | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 11 | leaf-1a | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 12 | leaf-1a | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet11 - remote: leaf-1b_Ethernet11 | PASS | - |
| 13 | leaf-1a | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet12 - remote: leaf-1b_Ethernet12 | PASS | - |
| 14 | leaf-1a | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: spine-1_Ethernet1 | PASS | - |
| 15 | leaf-1a | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: spine-2_Ethernet1 | PASS | - |
| 16 | leaf-1a | MLAG | MLAG State active & Status connected | MLAG | FAIL | state: inactive - negotiation_status: connecting |
| 17 | leaf-1a | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 18 | leaf-1a | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.128.1 | FAIL | Session state "Active" |
| 19 | leaf-1a | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.1.0 | PASS | - |
| 20 | leaf-1a | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.1.2 | FAIL | Session state "Active" |
| 21 | leaf-1a | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 1.1.1.1 | PASS | - |
| 22 | leaf-1a | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 1.1.1.2 | FAIL | Session state "Active" |
| 23 | leaf-1a | Routing Table | Remote VTEP address | 2.2.2.11 | PASS | - |
| 24 | leaf-1a | Routing Table | Remote Lo0 address | 1.1.1.11 | PASS | - |
| 25 | leaf-1a | Loopback0 Reachability | Loopback0 Reachability | Source: leaf-1a - 1.1.1.11 Destination: 1.1.1.11 | PASS | - |
