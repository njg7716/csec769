1. What is the problem or maybe research question? In sec, it may translate to: What is the threat?
	
	The problem is that WPA2 is so complex it is hard to research. This is true because there have not been nearly as many analysis' done on it as other security protocols and WPA2 is something that pretty much everyone uses heavily.
	
2. Is it an important problem? Who cares? (motivation)
	
	It is an important problem because of the amount of people that it has an effect on. Everyone should care about the security of WPA2 but for this particular paper, other researchers care because it creates a logical representation of WPA2 to test use cases in the future.

3. What is the scenario under consideration?
	In sec, it often includes: What can the attacker do?
	
	They test all scenarios using a test model. They really set out to test KRACK attacks and their variations but they unintentionally test more that just that.
	
4. What is the proposed attack or mitigation idea/approach?

	They concluded that "the patched versions of IEEE 802.11’s WPA2 indeed meet their core security requirements in the face of complex attacks"

5.  Is the idea really novel, practical, and convincing?
	Is there enough evidence to support the claims?
	
	I am not sure I would say "novel" since it models a very complex system. However, it seems practical. I will say that I am not a expert in wireless security but the proofs that they stated seemed to check out.

Big Picture: These dudes came up with rules or facts with exceptions to logically simulate WPA2. They then used a computer to analyze those rules to find logical flaws that could then lead to attack vectors. They did this because WPA2 is very complex and was not studied as much as other security protocols. The concluded that the proposed countermeasures are sufficient in preventing rekeying attacks. This model does not help when it comes to finding implementation flaws. Also, WPA2 is still vulnerable to off-line guessing attacks???