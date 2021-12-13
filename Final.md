## 4th Generation (4G)
- 4G - 2011
	- All IP-based communications (IP telephony)
		- Voice over LTE (VoLTE) - HD voice call
	- Increases speed (up to 1 Gbit/s)
	- OFDMA multi-carrier (instead of CDMA)
	- MIMO capability
- Two techs
	1. LTE Advanced (long term evolution advanced)
	2. Mobile WiMAX (IEEE 802.16e) - not very popular in the US
		- last mile wireless broadband access instead of cable and DSL

## OFDMA vs OFDM - A Review
- Orthogonal Frequency Division Multiple Access
![[Pasted image 20211019121313.png]]

## LTE Network Architecture
- Node B -> Evolved Node B (eNodeB) - more responsibilities
- HLR -> Home Subscriber Server (HSS)
![[Pasted image 20211019121450.png]]

## Attach Procedure in LTE
![[Pasted image 20211021112349.png]]
![[Pasted image 20211021112414.png]]
![[Pasted image 20211021112439.png]]

## How NSA Tracks People
- A mobile device continuously announces its location

## IMSI Catchers (Again!)
- Malicious eNodeB advertises itself as legitimate
	- Sniff and duplicate the configuration of a legitimate eNodeB
	- Create higher received signal strength than the legitimate's
- Force all UEs to disclode their IMSI in the clear
	- UE trusts any eNodeB who claims it has never seen that UE
- No need to downgrade to GSM
	- identity_request message is still unauthenticated!
- Open source tools
	- srsRAN (with SDR inside Faraday cage - why?) Against the law

## 4G - Crypto Algorithms
- Available encryption and integrity algorithms
	- Snow 3G (EIA1/EEA1) - mandatory
		- Stream cipher, employs an LFSR (initiated by the key and a 128-bit initialization variable) and a state machine to generate a sequence of 32-bit words
	- AES (EIA2/EEA2) - mandatory
		- Block cipher - Counter mode for confidentiality and cipher-based MAC mode for integrity
	- ZUC (EIA3/EEA3) - optional
		- Stream cipher, with a 128-bit initialization vector
- They all use 128-bit keys

## 4.5th Generation - 2015
- LTE Advanced Pro (4.5G)
	- Up to 3 Gbps (3x LTE Advanced)
		- Aided by 256-QAM support
	- Employs MU-MIMO
- Introduces narrowband IoT (NB-IoT)
	- Bring IoT devices to the cellular networks ecosystem
	- Low cost, long battery life, and high connection density
	- Uses the same security and privacy features of LTE

## 5th Gen (5G) - 2019
- New applications beyond mobile internet
	- drones
	- vehicles
	- IoT/sensors
	- ...
- New frequency bands: 2.5-3.7 GHz, 25-39 GHz
	- In addition to the traditional 600 - 850 MHz band for LTE
	- Different coverage ranges (why?) physics of waves
	- eNodeB -> gNB

## 5G Design Goals
- Extremely low latency
	- ultra-reliable and low-latency communications (URLLC)
		- Less than 1 millisecond
	- Applications: remote surgery, VR, interactive/autonomous vehicles (smart transportation), etc.
- Ubiquitous, high density, high speed connectivity
	- Extreme mobile broadband (xMBB) - up to 10 Gbps
	- Massive machine-type communications (mMTC) - smart city
	- Support higher densities
		- Concerts, stadium, malls, etc

## 5G Ecosystem
![[Pasted image 20211028111522.png]]
- A massively connected community
	- wearables
	- Smart vehicles
	- Appliances
	- Virtual Reality
	- Augmented Reality
	- Public Safety
	- Smart classroom :)
	- Remote surgery
	- ...

## What Brings About 5G?
- Key enabling technologies
	- Millimeter waves and small cells
	- Massive MIMO
	- Beamforming
	- Full duplex
	- Network slicing/virtualization
- Implications:
- Challenges
	- Fast signal decay (why?) needs more gNBs, new hardware, wider attack surface, privacy concerns, ...

## 5G Security
- The same encryption and integrity  algorithms as LTE
- IMSI -> SUbscription Permanent Identifier (SUPI)
	- 5G-GUTI is still supported
- Evolution of security from 2G to 5G:
![[Pasted image 20211102111532.png]]

## 5G Security - SUPI Encryption
- SUPI obfuscated and encrypted (concealed) using public key of HSS
	- HSS (home network) public key is stored in USIM
	- Probabilistic asymmetric encryption using ECC
		- Each time, same SUPI is encrypted with a different ephemeral key to generate a different SUCI (to avoid creating a fixed ID)
![[Pasted image 20211102111903.png]]
	
# Security of Vehicle-to-Everything Communications
## Roadways of the Future
![[Pasted image 20211104110319.png]]

## Connected Vehicles (CV)
- Let vehicles "talk" to enhance proximity awareness
	- Can reduce > 60% of the deaths on the roads
		- 98% of accidents today are due to human errors :(
	- Increase transportation system efficiency
		- Reduced travel time, less traffic, and less pollution
	- Comfort while driving, social inclusion (mobility for all), ...
		- Autonomous, semi-autonomous, and non-autonomous cars
- Emerging technology with rapid growth
	- Projected market value by 2028: $12.8 Billion
	- Volkswagen, BMW, Ford, Tesla, Nissan, Cadillac, Audi, etc.
## Types of Connected Vehicles
- exploit wireless waves to talk
- Depending on whom a vehicle talks to
	- Vehicle-to-Vehicle (V2V)
	- Vehicle-to-Network
	- Vehicle-to-Pedestrian
	- Vehicle-to-Infrastructure
	- Vehicle-to-\[insert your choice\] -> V2X
		- Cellular V2X - Vehicles as new citizens in future 5G ecosystem

## Vehicle to Infrastructure
- Roadside Units (RSU)
	- Devices installed along the roadway
	- Capable of relaying V2X messages
	- Can interface with traffic management systems like traffic light controllers

## Vehicle to Vehicle Communications
- Provide 360 degree awareness of nearby vehicles
	- Wirelessly exchange safety and non-safety messages
	- Complement the sensors: see (in NLOS) wjat sensors cant
		- Sensors ![[Pasted image 20211104111241.png]]
		- V2V ![[Pasted image 20211104111302.png]]
		- V2V is expected to have the largest share of the CV market

## Basic Safety Messages (BSMs)
- Broadcasted periodically by each vehicle
	- Contains position, velocity, direction, acceleration, ...
- BSM examples
	- Forward Collision Warning
	- Emergency Electronic Brake Light
	- Blind Spot Warning
	- Do not Pass Warning
	- Left Turn Assist
	- Intersection Movement Assist
![[Pasted image 20211104111602.png]]

## V2X Technology Evolution
![[Pasted image 20211109110719.png]]

## DSRC Basics
- Dedicated Short-Range Communications
	- Commonly deployed in EU and Japan
		- Somewhat limited in the US, < 0.0057% of the current 274 million vehicles on the road
	- Based on Wi-Fi technology (IEEE 802.11p or 802.11bd)
		- Layers 1 & 2 (PHY and MAC)
- Network and transport layers, and security services: IEEE 1609 family
- Payload definitions and performance requirements: SAE standards

## IEEE 802.11bd (2022?)
- Enhancements for next-gen V2X
	- Maneuver, live camera feeds, platooning, remote driving, ...
- Design goals
	- Latency < 5ms
	- Double the throughput of 802.11p
	- Double the relative velocities to 500 km/h
	- Double the communication range to > 1 km
	- Coexistence & backward compatibility
- How? Using advanced Phy-layer tech

## C-V2X
- 3GPP Cellular V2X
	- Release 16 (2020): platooning, automated/remote driving
	- Direct communication vs. Network communication
- Direct C-V2X compared with 802.11p-based V2X
	- Increases communication range
	- Provides better non-line-of-sight (NLOS) performance
	- Enhances reliability and latency with low complexity

## 5G New Radio (NR) V2X
- NR-V2X
	- Phy & MAC layers
	- Upper layers: like DSRC
		- IEEE 1609
		- SAE
- Advanced use cases
	- URLLC for latency
	- eMBB for 3D maps
![[Pasted image 20211109112001.png]]

# V2V Security
## Possible Attacks
- V2V creates new attack surfaces!
	- Eavesdropping and tracking (identity,velocity, trace, etc.)
	- Spoofing, including replaying (manipulated) messages
	- Jamming
- BSM-specific attacks
	- Spoofing, message modification, replay, etc.
	- Can be life threatening, specifically for autonomous vehicles

## Attack Example 1
- With jamming and then BSM spoofing, an attacker can feed false information and cause an incident
![[Pasted image 20211111105836.png]]

## Attack Example 2
- Falsified BSMs indicating a traffic jam ahead could cause vehicles to stop suddenly for no reason
![[Pasted image 20211111110011.png]]

## Security Requirements for V2V
1. A message originates from a trustworthy and legitimate vehicle
2. A message is not modified between sender and receiver - integrity
3. Misbehaving units are removed from the system
4. Tracking vehicles is not possible beyond a short interval
5. Life-long solutions

## BSM Authentication and Integrity
- Achieved by using Elliptic Curve digital signature algorithms (ECDSA)
	- Includes time and location (to prevent replay/relay attacks) Defined in IEEE 1609.2 standard
- Uses PKI and (short) certificates to sign BSMs
	- A public-key infrastructure (PKI) is needed to verify the certs of the public keys
	- Why using asymmetric keys instead of symmetric ones?
		- You would need to store EVERY vehicles key when using symmetric keys
	- Short-lived pseudonym certificates to prevent tracking

## V2X Public Key Infrastructure
![[Pasted image 20211111111410.png]]

# Security of Wireless IoT Protocols
## Internet-of-Things (IoT)
- A network of Internet-enabled "things"
	- Resource-constrained and often tiny devices
		- Limited in power/battery, memory, processing capability, transimission capability, ...
	- May connect to the Internet through hub/gateway
	- Smart world (smart grids, smart homes, smart cities, smart vehicles, smart transportation)
- 75 Billion IoT devices by 2025
	- 10+ billion Bluetooth chips, 5+ billion Industrial IoT devices, > 50% of new vehicles

## IoT Communication Protocols
- Wireless protocols (PHY/Link layer)
	- Bluetooth, Zigbee, Wi-Fi, Z-Wave, NB-IoT, ...
	- Vary in bandwith, range, cost, and power consumption
- Network/Adaptation layer
	- 6LoWPAN (IPv6)
- Transport layer messaging
	- CoAP, MQTT, Google QUIC, etc.

## Bluetooth Evolution
- In 1998, a consortium of companies - Ericsson, IBM, Intel, Nokia, and Toshiba - formed a special internet group (SIG), codenamed "Bluetooth"
	- Goal: low-cost, flexible, and protable wireless platform for short-range communication (<~30m)
![[Pasted image 20211116111609.png]]

## Example Applications
- Smart phones
- Digital pen and board
- Smart appliances
- Hands-free driving
- Presentation controllers
- Wireless speaker/headset
- FitBit/Healthcare devices
- Blue Diamond App
- Contact tracing (COVID-19)

## Definitions
- Bluetooth: a flexible and portable personal area network protocol stack
- Specification: how the technology works
	- Bluetooth 2.0, 4.2, 5.1, etc
- Profile: a vertical slice through the protocol stack
	- Defines mandatory options at each layer for interoperability
	- Example 1: Audio/Video Remote Control Profile (AVRCP)
		- To control TVs, audio streaming in car navigation system, etc
	- Example 2: Blood Pressure Profile (BLP) - starting 4.0

## Bluetooth Protocol Stack
![[Pasted image 20211116112030.png]]

## 1. Radio Specification
- Defines a Bluetooth transceiver operating on 2.4 Ghz ISM band
	- Frequency-hopping spread spectrum for coexistence
	- Hopping rate: 1600 times/s for data/voice
	- Bluetooth Classic: 79 channels 1MHz apart
	- BLE: Hopping over 40 channels spaced 2 MHz apart
- Defines power classes (four classes in BLE)
	- Tx power 0 - 20 dBm -> 1 - 100m distance
- Data rate: 1-3 Mbps (Bluetooth 5 achieves 2 Mbps)

## 2. Baseband Specification
- Link Controller on top of the radio
	- Works with the Link Manager (at upper layer) for addressing and carrying out link connection and power control
	- Performs advertising (in BLE) to discover nearby BLuetooth devices
- Two major controller states
	- Standby state - default state
	- Connection state
## Connection Setup
- Initiated by any node
- Method in Bluetooth Classic: inquiry and paging
	- Inquiry is used when no information is available about the remote device
	- Paging is used when the remote device is known
- Method in BLE: advertising
	- Advertising device emits small packets containing data deemed useful to scanning devices
	- Sent over 1-3 advertising channels
	- Used for connection requestd OR broadcast beacons

## Upper Layers
- Link Manager (LM) carries out
	- Link setup and configuration 
		- Discovers and communicates with remote LMs via LM protocol
	- Authentication and encryption
	- Host Controller Interface (HCI): Used to access to baseband
- Service Discovery Protocol (SDP) - middleware layer
	- Provides a means for devices to discover available services and their characteristics on each other
		- In Bluetooth environment, available services dynamically change based on the RF proximity of devices in motion
## Host Controller Interface (HCI)
- Provides a command interface between the host and the baseband controller
	- The controller is responsible for the lower layers (Radio, Baseband, and Link Control/Management). Its functions are controlled by a Bluetooth adaptor
	- The host is responsible for the higher layer protocols, such as Service Discovery Protocol (SDP). Its functions are preformed by a computing device like a latop or smartphone
- Also, provides a uniform method of accessing the Bluetooth baseband capabilities

## Bluetooth Low Energy (Smart)
- BLE v4.0-4.2
	- Adopted as of 2011-2014
- Rapid build-up of simple links
- Lower power but similar communication range
- Not backward-compatible
	- Dual-mode devices - Bluetooth Classic was upgraded too!
- New profiles
	- Healthcare and medical (e.g., Blood Pressure Profile - BLP)
	- Sports and fitness

## Bluetooth 5
- v5.0 - 2016
	- Focused on internet of things
		- Specifically, home automation
	- Quadruple the range
		- Using increased transmit power or coded physical layer/FEC
- v5.1 - 2019
	- Direction finding (angle of arrival estimation)
	- Randomized advertising channel index
- v5.2 - 2020: Concurrent connections

## Pairing
- Control which devices can connect to each other
	- no AP/eNodeB available to moderate the process
- Pairing -> shared link key -> bond (authentication)
	- After that, devices can connect as soon as in range
- Legacy pairing: PIN codes
	- Prior to 2.1
	- PIN is used to derive the key
	- Not all devices have the capability of entering PIN codes

## Secure Simple Pairing (SSP)
- Starting Bluetooth v2.1
- More flexible association models
	- Just works - minimum user interaction (MitM attack)
	- Passkey entry - show on one device, enter in the other one
	- Numeric comparison (BLE 4.2) - requires user involvement
		- Requires only YES/NO buttons, most secure method
	- Out of Band - use an external means to exchange info
		- e.g., Near-field communication (NFC)

## Link Key Generation for SSP
- Using ECDH public key pairs (P-192 or P-256)
![[Pasted image 20211123110608.png]]

## ZigBee
- Intended to be simpler and less expensive than Bluetooth and Wi-Fi
	- Low power: 0-20 dBm (1-100mW)
	- Low data rate: 250 kbps
	- Short range: 10-100m line of sight
	- Little mobility support
	- Security: Strong 128-bit symmetric encryption (AES)
- Built on IEEE 802.15.4
	- Defines PHY and MAC layers for a Personal Area Network (PAN)

## ZigBee Applications
- Home energy monitors (Smart Energy)
- Traffic management systems
- Building management systems
- Building automation
- Light switches
- Industrial control
- Medical data collection
- ...

## ZigBee Principals
- Coordinator - Centralized model
	- Model capable device, Trust Center (TC) for security keys
	- Cannot sleep!
- Router
	- Intermediate node, cannot sleep either
- End device
	- Low power
	- E.g., sensors, bulbs, etc

## 802.15.4 (PHY/MAC)
- 2.4 GHz ISM band worldwide
	- America and Australia: 902 - 928 MHz ISM band
- 16 channels with 2 MHz bandwidth
	- 5 MHz apart
- Uses direct-sequence spread spectrum (DSSS)
	- Digital modulation: QPSK (OQPSK)
- 64-bit IEEE (MAC) address
- Security: CCM* with upper layer keys

## Keys - Network Layer
- At network layer
	- A 128-bit shared NWK  key
	- Used for broadcast communications
	- Needs to be securely distributed first (How?)
- AES-CCM for encryption
- CBC-MAC for authentication

## Keys - Application Support Layer
- 128-bit global link key (pre-cofigured)
	- Used to encrypt and distribute the network key
	- ZigBee-defined (ZigbeeAlliance09) or manufacture-defined
- 128-bit pair-specific link keys - optional
	- pre-configured unique link key (for exclusive key distribution) - Centralized model
		- Derived from Install Code (a QR code)
	- Trust Center link key: To encrypt unicast traffic to/from TC
	- Application link key: To encrypt unicast traffic btw. nodes

## Z-Wave
- Low-Power, interoperable, RF mesh networking	
	- Control and monitoring
	- Primarily for home automation
- Radio
	- Low power: 0 dBm
	- Very low data rate: 40 - 100 kbps
	- Medium range: 40m
	- 908.42 and 916MHz (North America)
	- 300 kHz bandwidth

## Z-Wave Security
- AES-128 encryption
- Security 2 - Starting Jan 2017
	- Stronger AES-128 encryption
	- Signal jam detection
	- Elliptic curve DH key exchange
	- Authentication using unique PIN (+ optional QR)

## Other IoT Protocols
- Thread 
	- uses 802.15.4 and 6LoWPAN, secure IPv6 addressable mesh with high level of auth and encryption
- LoRa (Long Range)
	- 433 and 915 MHz, long-range with low power, < 27 kbps
- Near-field communication (NFC)
	- Extremely short range <4cm over 13.56 MHz band, no pairing, used for payments or conn bootstrapping
- RFID Radio frequency id - not for IoT
	- A tiny radio tag to store and transmit an id number