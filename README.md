# Stadium_Network
This is the second part of my final high school project
This network simulation models the entire stadium infrastructure using Cisco Packet Tracer. The design is segmented into multiple zones using VLANs to ensure secure and efficient communication across different functional areas. The key segments include:

Office Network (VLAN 10):

Purpose: Provides secure connectivity for administrative workstations and management systems.
IP Range: 192.168.10.0/24
Devices: PCs, servers, and printers located in the administration offices.
Ticketing Network (VLAN 20):

Purpose: Dedicated network for ticket sales terminals (POS devices) and related systems.
IP Range: 192.168.20.0/24
Devices: POS terminals, ticket kiosks, and related peripherals.
Guest Wi‑Fi (VLAN 30):

Purpose: Provides visitors with Internet access while isolating guest traffic from the internal networks.
IP Range: 192.168.30.0/24
Devices: Smartphones, tablets, and laptops connecting via a wireless access point.
IoT/Smart Devices & Security (VLAN 40):

Purpose: Supports IoT devices used for automated functions (such as smart lighting and irrigation) as well as security systems like IP cameras and motion sensors.
IP Range: 192.168.40.0/24
Devices: IoT sensors, smart relays, IP cameras, and other security-related devices.
Core Components:

Router-on-a-Stick Configuration:
A central router is used with subinterfaces for each VLAN to route traffic between the different segments. Each subinterface is assigned an IP address serving as the default gateway for that VLAN.

Switches:
A core switch connects the router to multiple access switches. Each access switch serves a specific VLAN/zone, ensuring physical and logical separation of traffic.

Wireless Access Point (AP):
The guest Wi‑Fi network is provided by an AP configured to broadcast the SSID (e.g., StadiumWiFi) with WPA2 Personal security. The AP is connected to the core switch and tagged with VLAN 30.

DHCP Configuration:
DHCP servers (either integrated into the router or as separate devices) are configured for each VLAN to automatically assign IP addresses to connected devices.

Testing & Validation:

Ping Tests: Devices within each VLAN can ping their respective default gateways (e.g., 192.168.10.1 for Office).
Inter-VLAN Routing: The router is configured to allow communication between VLANs, subject to security policies.
Wireless Connectivity: Guest devices should automatically obtain IP addresses from the DHCP server and successfully connect to the Internet via the AP.
