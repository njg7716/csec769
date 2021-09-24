# The 5 Questions
1. What is the problem or maybe research question? In sec, it may translate to: What is the threat?
- Make beacon frames more secure

2. Is it an important problem? Who cares? (motivation)
- 

3. What is the scenario under consideration? In sec, it often includes: What can the attacker do?
- Silencing Attacks: AP tells client to stop transmitting
	- Attacks can spoof this to prevent clients from transmitting
- Abusing CSMA
	- max out backoff window and informs client it is a low priority
- Battery Depletion
	- Client tells AP it is going to sleep but AP keeps telling client it has buffered frames even though it doesnt so client stays awake
- 

4. What is the proposed attack or mitigation idea/approach?
- The mitigation is to authenticate the beacon frames after the connection to discover if it is legit or a rogue AP
- Needs to be effiecient because of how often beacons are set
- Use new information element 
	- beacon integrity packet number BIPN
	- beacon integrity group temporal key BIGTK
	- authenticity only validated after connection to AP
- 

5. Is the idea really novel, practical, and convincing?	Is there enough evidence to support the claims?
 