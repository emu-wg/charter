Name: EAP Method Update

Acronym: EMU

Area: SEC

Personnel

 * Chairs: Joe Salowey and Mohit Sethi
 * Area Director: Roman Danyliw

# Charter for Working Group

The Extensible Authentication Protocol (EAP) [RFC 3748] is a network access authentication framework used, for instance, in VPN and mobile networks. EAP itself is a simple protocol and actual authentication happens in EAP methods. Several EAP methods have been developed at the IETF and support for EAP exists in a broad set of devices. Previous larger EAP-related efforts at the IETF included rewriting the base EAP protocol specification and the development of several standards track EAP methods.

EAP methods are generally based on existing security technologies such as TLS and mobile network Authentication and Key Agreement (AKA). Our understanding of security threats is continuously evolving. This has driven the evolution of several of these underlying technologies. As an example, IETF has standardized a new and improved version of TLS in RFC 8446. The group will therefore provide guidance and update EAP method specifications where necessary to enable the use of new versions of these underlying technologies.

At the same time, some new use cases for EAP have been identified. EAP is now more broadly in mobile network authentication. The group will update existing EAP methods such as EAP-AKA' to stay in sync with updates to the referenced 3GPP specifications. RFC 7258 notes that pervasive monitoring is an attack. Perfect Forward Secrecy (PFS) is an important security property for modern protocols to thwart pervasive monitoring. The group will therefore work on an extension to EAP-AKA' for providing Perfect Forward Secrecy (PFS).

Out-of-band (OOB) refers to a separate communication channel independent of the primary in-band channel over which the actual network communication takes place. OOB channels are now used for authentication in a variety of protocols and devices (draft-ietf-oauth-device-flow-13, WhatsApp Web, etc.). Many users are accustomed to tapping NFC or scanning QR codes. However, EAP currently does not have any standard methods that support authentication based on OOB channels. The group will therefore work on an EAP method where authentication is based on an out-of-band channel between the peer and the server.

EAP authentication is based on credentials available on the peer and the server. However, some EAP methods use credentials that are time or domain limited (such as EAP-POTP), and there may be a need for creating long term credentials for re-authenticating the peer in a more general context. The group will investigate minimal mechanisms with which limited-use EAP authentication credentials can be used for creating general-use long-term credentials.

In summary, the working group shall produce the following documents:

	* An update to enable the use of TLS 1.3 in the context of EAP-TLS (RFC 5216). This document will update the security considerations relating to EAP-TLS, document the implications of using new vs. old TLS versions, add any recently gained new knowledge on vulnerabilities, and discuss the possible implications of pervasive surveillance.

	* Several EAP methods such EAP-TTLS and EAP-FAST use an outer TLS tunnel. Provide guidance or update the relevant specifications explaining how those EAP methods (PEAP/TTLS/TEAP) will work with TLS 1.3. This will also involve maintenance work based on errata found in published specifications (such as EAP-TEAP).

	* Define session identifiers for fast re-authentication for EAP-SIM, EAP-AKA, EAP-PEAP and EAP-AKA’. The lack of this definition is a recently discovered bug in the original RFCs.

	* Update the EAP-AKA' specification (RFC 5448) to ensure that its capability to provide a cryptographic binding to network context stays in sync with updates to the referenced 3GPP specifications. The document will also contain any recently gained new knowledge on vulnerabilities or the possible implications of pervasive surveillance.

	* Develop an extension to EAP-AKA' such that Perfect Forward Secrecy can be provided. There may also be privacy improvements that have become feasible with the  introduction of recent identity privacy improvements in 3GPP networks.

	* Gather experience regarding the use of large certificates and long certificate chains in the context of TLS based EAP methods, as some implementations and access networks may limit the number of EAP packet exchanges that can be handled. Document operational recommendations or other mitigation strategies to avoid issues.

	* Define a standard EAP method for mutual authentication between a peer and a server that is based on an out-of-band channel. The method itself should be independent of the underlying OOB channel and shall support a variety of OOB channels such as NFC, dynamically generated QR codes, audio, and visible light.

	* Define mechanisms by which EAP methods can support creation of long-term credentials for the peer based on initial limited-use credentials.

The working group is expected to stay in close collaboration with the EAP deployment community, the TLS working group (for work on TLS based EAP methods), and the 3GPP security architecture group (for EAP-AKA' work)



## Milestones

 * November 2019: WG last call on operational recommendations for large certificate and chain sizes 

 * November 2019: WG last call on definition of session identifiers for fast re-authentication in EAP-SIM and EAP-AKA 

 * November 2019: WG adopts initial draft addressing the errata found in EAP-TEAP

 * November 2019: WG adopts initial draft on an EAP method for mutual authentication based on an OOB channel

 * November 2019: WG adopts draft providing guidance for use of TLS 1.3 with TLS based EAP methods

 * Jan 2020: WG adopts initial draft on creation of long-term credentials for EAP peer based on initial limited-use credentials 

 * March 2020: WG last call on extension to EAP-AKA to support forward secrecy 
