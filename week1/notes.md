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

