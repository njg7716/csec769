# Week 1 Class 1
- Networks connect multiple computing devices to exchange data
- There are different types, wired, wireless, optical
- We are going to focus on wireless in this class

## Goals
- Understand current and emerging wireless systems from security perspective
- Insight into recent research trends in wireless sec
- Experience on steps of small research project

## Terms to Know
- Symmetric cipher: Uses same key to encrypt and decrypt
- Asymmetric Cipher: Uses different key to encrypt and decrypt

## Wireless Security (Research)
- in a nutshell: radio waves are broadcasted in open space and everyone can see it
    - radio waves can go through walls

# Week 1 Class 2

## Types of Wireless Attacks
- Passive (privacy related)
    - Intercept/Evesdrop
    - Infer (user, location, traffic)
- Active
    - Block (jamming)
    - Deceive
        - Message modification
        - Spoofing/Masquerading
        - MitM
- WPA3 is at Layer 2 and Layer 1
- The difference between physical and wireless networks are at layer 1 and 2

## Cryptographic Countermeasures
- Symmetric-key cryptography
    - Encryption for confidentiality
    - Message authentication and integrity
- Public-key cryptography
    - Digital signatures for authentication
    - asymmetric encryption
- Secure hash functions
- Pseudorandom number generators
    - secret frequency hopping

## Are We Still Innsecure?
- Unfortunately, yes!
- Attackers are evolving too!
    - access to open source crypto
    - unexplored analysis methods
    - abuse of privacy infrastructure
    - (advanced) radio softwarization
        - decreases cost
    - Constrained devices in a highly-connected ecosystem
- More needs to be done to make the world safer

## Wireless Security Research
- What is it?
    - offensive security vs defensive security
    - in research, we apply a scientific method to study/assess or design a system or protocol
- Examples
    - cryptography
    - protocol analysis
    - traffic analysis
    - formal analysis
    - testbed implementation

# Above is on first quiz

# Wireless Communications

## Acoustic Waves

## Electromagnetic Waves
- transport energy through open space, stored in propagating electric and magnetic fields

## Periodic Wave
- max amplitude
- phase
- frequency
- time period
- sampling rate
- sampling interval

## Wavelength
- The distance a wave travels in a time period
    - Depends on propagation speed
    - For EM waves
        - c = 3*10^8 m/s speed of light
        - f = 1/T frequecy
        - lamda = c/f (meters) wavelength

## Wireless Channel
- An open, shared medium for signal propagation
    - Broadcast nature -> noise, ,interference, cogestion
    - Easier for eavesdropping, jamming, etc.
- Simplified mathematical representation: y = hx + n
    - y = recieved signal
    - x = transmitted signal
    - n = noise
    - h = channel

## Signals and Channel Representation
- Each signal has an amplitde and a phase
    - complex numbers have an amplitude and a phase, too
    - So, it is natural - and easier - to use a complex number to represent a symbol/signal (x) or a channel (h)
- Symbols: Short signals to convey digital bits
    - different symbols have different waveforms (e.g, phases)

# Week 2 Class 1

## Review of last week
- Physical layer between wire and wireless are different

## Digital Modulation
- map input digital bits to analog symbols
    - modulation alaphabet: a finite set of distict symbols
    - demodulation: find bits corresponding to recieved symbols
- Basic digital modulation methods
    - amplitude shift keying (ASK)
    - Frequency Shift Keying (FSK)
    - Phase Shift Keying (PSK)
    - Quadrature Amplitude MModulation (QAM)
        - combines ASK and PSK

## Constellation Diagram
- a representation of ASK and PSK symbols on a 2D diagram in the complex plane
    - it shows amplitude and phase of a symbol

## Symbol (Baud) Rate
- m distinct symbols can represent log2(m) bits
    - for example to represent 4 bits we need 2^4 = 16 symbolls
    - m is modulation order
- symbol rate of n:n possible changes per second
    - m and n determine the trasnmission (bit) rate
    - ex. assume symbol rate is 100 symbols/second and modulation order is 32 what is the bit rate?
        - 100 * log2(32) = 500 bits

## Signal in Time/ Frequency Domain
- A signal may be composed of multiple waves, each with a different frequency (and phase/amplitude)
    - It can be used to send multiple symbols simultaneously

## Fourier Transform (FT)
- To represent (express) a time-domain signal v(t) based on its frequency components

## OFDM
- Orthogonal Frequency Division Multiplexing
    - widely used in nearly all modern systems
    - careflly selects frequency components of a signal
        - ex. use only the frequencies that are multiple of f1
        - subcarriers = frequency components
        - orthogonal subcarriers
## Noise and SNR
- Noise: undesired random energy that degrades the signal's quality at Rx
- SNR: Signal-to-Noise Ratio
    - measured in dB
- Interference: Energy coming from other transmissions
    - SINR: Signal-to-interference-plus-noise ratio
    - Interntional vs. Inintentional

## dBm
- dBm is the dB value when referenced to P0 = 1mw

## Wireless Channel - Definitions
- Channel bandwidth
    - the width of the set of frequencies used to create a signal
    - example: 100 kHz, 5MHz, etc.
    - It is different from bandwidth (Data rate) in computing
- Channel cpacity
    - theoretical upper-bound on the data rate over a band width B
    - When noise is additive white Gaussian (AWGN)

## QAM Order vs. SINR
- recall c = B * log2(1 + SINR)

## Wireless DoS
- RF jamming 9 or intentional interference (Physical Layer)
    - Maliciously reduce channel capacity
    - Constant / Persistent jamming
        - signal generators, magnetrons
    - Random jamming
    - Selective/Reactive jamming
        - Jam only when a particular transmission is detected
- Flooding (deceptive jamming) (Layer 2)
    - Disassociation attacks in Wi-Fi

# Week 2 Class 2
- Quiz next week
	- Equation on dB and dBm
	- Know concepts
## EM Wave Phenomena over Channel
- Gain / Loss
	- Shadowing
	- Absorption
- Multi-path Distortion
	- Reflection
	- Scattering
	- Differaction
	- Refraction
- Doppler Fading (mobility)

## Line of Sight
- A straight line from the Tx antenna to that of the Rx
- Non-Line-of-Sight 
	- No visual LOS betweeen Tx and Rx

## Free-Space Path Loss
- Attenuation of EM energy from the Tx to the Rx over the obstacle-free space (LOS channel)
- The wider the propagation area, the less power will be recieved by a single antenna
- Free-space path loss (sphere wavefront case)

## Signal Superposition - Concept
- WHen two signals arrive (almost) at the same time, they superpose on each other
	- We say the two signals interfere -- or collide
	- The superposed (combined) signal may look very different than the individual ones
- Its kind of like sound waves, they can combine to be stronger if they line up correctly but for the most part they collide and destroy each other
- This can be intentional (jamming) or unintentional

## Multipath Propagation and Fading 
- In case of signal reflections
	- contructive vs. descructive interference (fading)
	- depends on how far the reflection object is (a+b) and lamda/2
		- in phase vs. out of phase
		![[Pasted image 20210902113332.png]]
	
## Multi-Path Channel-Mitigations
- Mitigating multi-path fading at the Rx
	- Estimate and account for LOS and NLOS channel components to recover the original symbol
	- Channel State Information (CSI): a representation of the multi-path channel
- Mitigating inter-symbol interference (ISI)
	- 1. OFDM - details not discussed here
	- 2. Spread Spectrum (SS) techniques (discussed later)

## schematic View of PHY - layer
- Putting all together
![[Pasted image 20210902113750.png]]
- This process isnt perfect, things can go wrong

## MIMO
- So far we assumed SISO system
	- single input, single output
- Tx, Rx, or both can be equipped with multiple antennas
	- Multiple-Input Multiple-Output
		- MISO, SIMO, MIMO
	- Multiple antennas can improve SNR, transmission rate, transmission security, etc.


## MIMO Channel
- SISO channel model
	- y = hx + n
- MIMO channel model
	- Y = HX + N
	- p transmit antennas and q recieve antennas
- Example MIMO System:
	- ![[Pasted image 20210902115600.png]]

## A PHY-Layer Approach to Security
- A paradigm to exploit features and mechanisms at the PHY layer to launch or mitigate attacks
	- Not everything can be protected by upper-layer security mechanisms!
	- PHY/MAC headers, RSS value, operating frequency, channel coefficients, hardware features, etc. are unprotected!
- PHY-layer security can complement upper-layers' approached
	- examples: friendly jamming, hardware fingerprints, uniqueness of wireless channel, hiding data in noise,...

## Possible PHY-Layer Attacks
- Eavesdropping on open medium - sniffing
- RF jamming (reduce transmission rate)
- Unintentional EM emanatin
	- TEMPEST
- Privacy violation
	- multipath channel coeffiecients - location characterization
- Modulation classification


## Mechanisms/Applications
- Spread spectrum (frequenct hopping)
- Authentication
	- Device fingerprints, channel characteristics, watermarking
- Traffic/Transmission attribute obfuscation
	- Header (full-frame) encryption, modulation obfuscation
- Covert communications in noise
- Key generation
	- the channel tends to be unique -> Source of randomness

## Frequency Hopping SS (FHSS)
- Continuously change transmission frequency
	- Anti-jamming - only if a subset of channels are jammed
		- Also, mitigates narrow-band interference or eavesdropping
	- It can mitigate ISI too: transmissions on a feq are spaced
	- But, requires wide/high total bandwidth and maybe a secret hopping pattern
	![[Pasted image 20210902121439.png]]

## Direct Sequence SS
- Each bit is converted to a compact bit sequence using orthogonal spreading sequence
	- If we use FT, we observe the signal bandwith is spread
![[Pasted image 20210902121423.png]]
	- The Rx uses the same spreading sequence to recover the bit
	- Increases resistence to ISI, interderence and eavesdropping
		- Anti-jamming/eavesdropping if spreading sequence is secret
		
## Orthogonal Spreading Sequences
- An Rx uses this specific sequence to 
	- detect and synchronize with the transmitted signal
	- eliminate a delayed copy of a spread signal, and
	- Cancel out uncorrelated noise and interference


# Week 3 Class 1

## Wi-Fi 802.11
- Defines MAC and PHY for a wireless (WLAN)
- First adopted in 1997 by IEEE
	- >42 variations since then
- Address the following key issues
	- Coordination of devices within a WLAN and their mobility
	- Privacy and security of the user and its data
- 
## Infra Basic Service Set
- BSS with an Access Point (AP)
	- AP connects wireless and wired networks
	- Basic Service Set Identifier (BSSID)
		- BBSSID = AP's MAC Address
- Extended Service Set (ESS)
	- Service Set IDentifier (SSID/ESSID)
- Distribution System
	- connects multiple APs, increasing coverage

## AP Beacon
- Broadcast every 10-100 ms by the AP
- Includes
	- Timestamp
	- SSID
	- Supported data rates (modulation and coding schemes)
	- Currect channel number
	- Supported security protocols

## 802.11 Medium Access Control (MAC)
- Distributed Coordination Function (DCF)
	- For asynchronous data service (best effort service)
	- Nodes (including AP) contend for access to medium
- Point Coordinationn Function (PCF) (optional)
	- For time-bounded service
	- Polling from AP
- Hybrid Coordination Function (HCF)
	- Traffic categories priorities

## Distributed Coordination: CSMA/CA
- Carrier Sense Multiple Access (CSMA) with Collision Avoidance
- Collision avoidance methods
	- Physical carrier sense
		- Checks if RSS (Recieved Signal Strength) is above a threshold
	- Virtual carrier sense
		- Wait for the duration another Tx "announced" it will be active 
	- RTS (Request To Send) / CTS (Clear To Send) mode
		- explicit channel reservation
## CSMA/CA Algorithm
![[Pasted image 20210907114506.png]]
- NAV: The remaining duration fo others' transmissions

## CSMA/CA Data and ACK
- Sender (physical carrier sense)
	- If channel idle for DIFS*: transmit entire data fram
		- If later on collision detected: increase backoff time next time
	- If chnnel bust: backoff
- Receiver
	- If received OK, return ACK after SIFS

## Evolution of Wi-Fi
![[Pasted image 20210907115233.png]]

## Wi-Fi Frequency Bands
- Supported channel bandwidths
	- 10 (.11p), 20, 40, 80 and 160 MHz
- Radio frequency range (spectrum):
	- As per FCC "New Rules" (2015)
![[Pasted image 20210907115639.png]]

## 802.11n (2009) - Wi-Fi 4
- Frequency bands: 2.4 GHz and 5GHz
	- 20 and 40 MHz channels
- Achieves high throughput using MIMO-OFDM
	- 48 subcarriers per bandwidth
	- Up to 4 antennas (2x2 MIMO up to 270 Mbps)
- Access mode: Hybrid Coordination Function (HCF)
	- Extension of DCF and PCF
	- Different priority levels for voice, video, background and best-effort data services
- Other features
	- Beam forming using MIMO
	- Channel bonding (combining 20 MHz channels, creating 40 MHz ones)
	- HT-mixed mode
		- Backwards compatible
	- Greenfield Mode (for n devices only)
## 802.11ac (2013) - Wi-Fi 5
- Very High Throughput (VHT) WLAN
- 5 GHz only
- Extended channel bonding
	- Mandatory 80 MHz and option 160 MHz
- 256 QAM (up from 64 QAM in 802.11n)

## Multi-User MIMO (MU - MIMO)
- One transmitting MIMO device, multiple MIMO receivers (users) simultaneously
	- Antenna coordination to nullify the stream of one user at other users
![[Pasted image 20210907120357.png]]

## 802.11ac - Wave 2 (2016)
- MU-MIMO
	- Up to four downlink clients
- More antennas for up to eight spatial streams (vs. up to four in 802.11n)
	- Explicit CSI feedback for better antenna coordination
	- In practice, Wave 2 devices only have 4 antennas
- Support for more 5 GHz channels

## 802.11ax (2021) - Wi-Fi 6
- Technical name: High Efficiency WLAN (HEW)
	- GHz band, whatever allowed to use
		- Wi-Fi 6E: Wi-Fi 6 Etended to the 6GHz band
	- Wake time scheduling (for power savings)
	- Multi-user MIMO in both downlinks and uplink
- OFDMA (Orthogonal FD Multiple Access)
	- Time-frequency resource units (RUs)
	- Per user RUs
![[Pasted image 20210907120819.png]]
- Data rate: up to 11 Gbps
	- Supports 1024-QAM (Higher than 256-QAM in 802.11ac)
- Spatial frequency reuse
	- Dynamically adjusting transmit power and signal detetion threshold for simultaneous transmissions
- 802.11be (Wi-Fi 7)
	- Extremely High Throughput (EHT)
	- Currently at its early development stages, targeting 2024
	-  320 MHz bandwidth? 16 spatial streams/ MIMO

# Week 3 Class 2
## Wi-Fi Security Protocols
### Timeline
- 1999: Wired Equivalent Privacy (WEP)
	- 2000 first weakness
	- 2004 derecated
	- 2020 obsolete
- 2004 802.11i (WPA2)
	- 2012 WPA (TKIP- only) deprecated

### WPA2 in a nutshell
- Wi-Fi Protected Access II
![[Pasted image 20210909110409.png]]

### Joining WLAN - Initiation
- 1. Probing (scanning) to find an AP
	- Active scanning
		- Prob request/response frames
	- Passive Scanning
		- Listen for beacon frames
- 2. Auth - default mode in WPA2: open
	- Auth request/response frames
- 3. Association: AP and stations swap info
	- Association request/response frames
	- Transmit rates, cipher suite, MAC addresses, etc.

### IEEE 802.1X
- Auth for IEEE 802-based WLANs
	- Flexible, mature, scalable, and interoperable framework
		- Not an auth method
		- Requires deploying a server (not always possible)
	- Prevents unauth access to layer 2 (port-based)
	- User-specific key and user-based authentication
- Roles
	- Supplicant - the visitor (laptop)
	- Authenticator - the gate keeper (AP)
	- Authentication server - the decision maker

### 802.1X/EAP - Definitions
- EAP: Extensible Authentication Protocol
	- A variety of auth methods
	- EAPOL: Encapsulation of EAP over LAN
- RADIUS: Remote Access Dial-In User Service
	- Set of common functiionalities across auth servers
	- a protocol that allows access those functionalities/services
- WPA2 with 802.1X is called WPA2-enterprise
	- Appropriate for medium and large enterprises, and more recently, public Wi-Fi networks
	
	### Pairwise Key Hierarchy
- 1. Maser Session Key (MSK)
	- Generated after mutual authentication fo the supplicant and auth server (AS)
- 2. Pairwise Master Key (PMK)
	- In 802.1X mode: derived from MSK, and is client-specific
	- In pre-shared key mode: PMK = PSK (based on passphrase)
- 3. Pairwise Transient Key (PTK) - Derived from PMK
	- Generated after supplicant and AP's mutual auth

### First Step 802.11 Association
![[Pasted image 20210909111627.png]]

### EAP Authentication (802.1X Only)
![[Pasted image 20210909111709.png]]

### Final Step: 4-Way Handshake
![[Pasted image 20210909111743.png]]

### Results of 4-way Handshake
- 1. Supplicant and authenticator both proved the knowledge of the shared PMK
	- Mutual auth
	- acommon step in both enterprise and personal
- 2. A fresh ptk is derived
- 3. both parties have synced and turned on encryption of unicast (and group) packets

## AES-CCMP
- provides a very high level of confidentiality, integrity and replay protection of 802.11
- Relies on AES
	- 128 bit key
- CCMP: Counter mode with ciipher-block chaining MAC protocol
	- 1. AES counter mode block cipher for encryption
	- 2. AEES cipher-block-chaining MAC (CBC-MAC) for integrity

## Block Cipher Modes (1)
- Electronic Codebook (ECB) - serial mode
	- reveals the patterns in the original data - not used in WPA2
	![[Pasted image 20210914111238.png]]
	
	## Block Cipher Modes (2)
	- Electronic Codebook (ECB) - parallel mode
		- Reveals the patterns in the original data - not used in WPA2
![[Pasted image 20210914111354.png]]

## Block Cipher Modes (3)
- Counter mode with AES - used in WPA2
	- Hide any pattern by using counter
![[Pasted image 20210914111444.png]]

## Nonce + Counter
- The counter is prepended by a nonce
	- 104-bit nonce only changes from one packet to another
	- The counter starts at , and counts up as encryption proceeds
![[Pasted image 20210914111602.png]]

## Cipher-Block Chaining (CBC)
- Used to generate message integrity code (MIC)
	- Algorithm is initialized by nonce
![[Pasted image 20210914111701.png]]

## Computing MIC
- Used CBC-MAC with 128-bit blocks
- The first block for computing MIC is comprised of
	- 1. Flag, which is a constatn
	- 2. The same 104-bit nonce used in counter mode encryption
	- Dlen, which is the length of data
- Second block: Additional Authentication Data
	- MAC Addresses, the fragment number, and QOS identifier
- Then data blocks

## CCM Protocol (CCMP)
- CCM: COunter with CBC-MAC combination
- Three features
	- Specification of a nonce for each packet
		- Seccessive packets encrypted separately
		- Detects replay attacks
	- Achieve both message integrity and encryption with single ptk
	- Extension of integrity to cover data not encrypted (e.g., MAC addresses)

## CCMP MPDU
- MAC and CCMP headers are not encrypted
![[Pasted image 20210914112141.png]]


# Week 4 Class 2
## Pairwise Key Hierarchy - Review
- 1. Master Session Key (MSK) - Generated after 802.1X auth
- 2. Pairwise Master Key (PMK) 
	- In 802.1X mode: derived from MSK
	- In pre-shared key mode:
- 3. Pairwise Transient Key (PTK) - Collection of operational keys
	- Key Confirmation Key (KCK) - used for integrity-checks for key distribution and to prove possession of PMK
	- Key Encryption Key (KEK) - used to encrypt and distribute keys, e.g., Group Transient Key (GTK)
	- Temporal Key (TK) - used to encrypt data traffic
![[Pasted image 20210916105715.png]]

## WPA2-Personal is Vulnerable
- Simple passphrases -> dictionary attacks
	- PSK = PBKDF2(HMAC-SHA1, passphrase,ssid,4096,256)
		- PBKDF2: A password-based key derivation function
	- Capture one MIC, try different pssphrases offline
		- Deriving PTK needs SNonce and ANonce too (sent in plaintext)
		- Even easier for other clients of the same network
	- coWPAtty: A tool for cracking/auditing pre-shared key (PSK)
- Fixed in WPA3

## IEEE 802.11w (2009)
- Protect management frames
	- Confidentiality, integrity, authenticity, and replay (via CCMP)
- Frames protected by 802.11w
	- Disassociation and deauthentication
	- Radio measurement action frame
	- QoS action frame
- Frames infeasible to protect
	- Any packet sent before 4-way handshake (e.g., beacon, probe, authentication and association)

## Challenges of Header Encryption
- interruption in virtual carrier sense
	- Other stations cannot read Duration field
- Sender identification dilemma
	- When MAC address is encrypted, the Rx (Bob) cannot easily retrive the right decryption key

## Exposed MAC Address
- One can use unique, plaintext MAC addresses to track and identify users
	- Ex
		- smart trash cans to track/learn peoples shopping patters
		- Grocery stores created profile for their shoppers
- MAC address randomization for higher privacy
	- Standardized as part of IEEE 802.11aq amendment (2018)
- It should not disrupt an ongoing (encrypted) session
	- So it can be changed only in unassociated state (why?)
		- Used for prob requests per connection or per network/SSID

## 802.1X/EAP -WLAN Model
![[Pasted image 20210916111720.png]]

## EAP-TLS
- Based on Transport Layer Security (TLS) protocol
	- One of the most secure EAP standards
- Needs public key infrastructure
	- Requires certs for server and client (mutual auth)
	- Advantages
		- A compromised client password is not enough to illegitimately connect to the network
		- MitM attack against a client is difficult too; the attacker would need a valid server certificate
![[Pasted image 20210921111901.png]]

## PEAP
- Protected EAP
- In EAP, identity request/response messages are not encrypted
	- PEAP provides secure communication channel (tunnel)
- PEAP auth has two phases
	- 1. EAP-TLS with anon users
		- Server-side public key certs (optional client auth)
	- 2. Regular EAP
- EAP in EAP
![[Pasted image 20210921112118.png]]

## Passpoint for Public Networks
- What if you want auth in a public network
- Wi-Fi Passpoint (Hotspot 2.0)
	- Secure Wi-Fi enterprise was a success -> extend it beyond an enterprise
	- Requires online sign-up and 802.1X
		- Auth using creds or the SIM
	- Automatic network discovery & selection, seamless roaming
		- Based on 802.11u (2011)
	- Used, among others, for WiFi4EU (Free Wi-Fi for Europeans)
	
	# WPA3 and Public Wi-Fi
	
	## WPA3 in a nutshell
	- WPA3: Wi-Fi Protected Access III - 2018
		- Next generation of Wi-Fi security
	![[Pasted image 20210923150235.png]]
	- Dotted box is new in WPA3

## WPA3 - New Features
1. Mandatory Protected Management Frames - PMF (802.11w)
2. Individualized encryption in public/open networks
	- Enhanced Open
3. Interact with the AP for each password attempt in WPA3-personal (dragonfly handshake)
4. 192-bit security for WPA3-enterprise (optional)
5. Alternative interface for configuring IoT devices
	- Easy Connect

## WPA3-Personal
- Simultaneous Authentication of Equals (SAE)
	- Also called dragonfly handshake
	- Replaces PSK generation in WPA2-personal
	- Robust against offline dictionary attacks
		- Allows Natural Password Selection - select easy passwords
		- Also, provides forward Secrecy; unlike the passphrase, the PMK will have high entropy and no longer will be constant
- Manage (IoT) devices with limited or no interface
	- Device Provisioning Protocol (DPP)
	- Device's public key is communicated using QR, NFC, or BT

## Dragonfly Handshake
- Two phases: Commit and Confirm
	1. Commit exchange: at both sides
		a.) commit to a signle guess of the password
		b.) exchange a random scalar and a masked password element (can be a point on an Elliptic curve), then
		c.) generate a common key (PMK) using the exchanged random numbers and the password element
	2. Confirm: derive a token using the secret, then exchange to confirm the guess

## SAE Messages
- WPA2 authentication messages (with open-system auth) were almost useless, SAE uses and expands them!
![[Pasted image 20210923151225.png]]

## Cracking SAE?
- Random numbers and password element are masked->Attacker cannot obtain them to check if a guessed passphrase (from dictionary) is correct
	- In contrast, the inputs to PBKDF2 function were known
	- ANonce and SNonce were also easy to capture
- Attcker would need a network interaction to confirm each guessed password
	- Idea: slow down the rate of an attempted attack
	- Temporal limit on password checks

## After All, Why Public/Open Wi-Fi?
- A public open network may not be secure
	- In a restaurant/cafe, stadium, library, airport/airplane, hotel
- Possible reasons
	- Lower cost (free Wi-Fi)
	- Better indoor coverage than cellular
	- Running out of cellular data allowance (<30% remaining)

## WPA3 for Open Networks
- Unauthenticated encryption
- Based on Opportunistic Wireless Encryption (OWE)
![[Pasted image 20210923152210.png]]
