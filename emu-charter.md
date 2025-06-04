Name: EAP Method Update

Acronym: EMU

Area: SEC

Personnel

 * Chairs: Joe Salowey and Peter Yee
 * Area Director: Paul Wouters

# Charter for Working Group

The Extensible Authentication Protocol (EAP) [RFC 3748] is a network access authentication framework used, for instance, in VPN and mobile networks. EAP itself is a simple protocol and actual authentication happens in EAP methods. Several EAP methods have been developed at the IETF and support for EAP exists in a broad set of devices. Previous larger EAP-related efforts at the IETF included rewriting the base EAP protocol specification and the development of several standards track EAP methods. This group will therefore provide guidance and update EAP method specifications where necessary to enable the use of new versions of these underlying technologies.

EAP authentication is based on credentials available on the peer and the server. However, some EAP methods use credentials that are time or domain limited (such as EAP-POTP), and there may be a need for creating long term credentials for re-authenticating the peer in a more general context. This group will investigate minimal mechanisms with which limited-use EAP authentication credentials can be used for creating general-use long-term credentials.

EDHOC (Ephemeral Diffie-Hellman Over COSE) is a very compact and lightweight authenticated Diffie-Hellman key exchange with ephemeral keys that is suitable in constrained environments in which many of the existing EAP methods are not a good fit. EDHOC offers the useful properties of mutual authentication, forward secrecy, and identity protection. This group will accordingly produce a specification for an EAP method incorporating the EDHOC mechanism (RFC 9528).

While TLS-based EAP mechanisms provide strong channel protections, if the client does not authenticate and validate the server's credentials properly (possibly owing to a lack of provisioned information necessary to undertake that validation), an EAP mechanism running over TLS that relies on passwords is vulnerable to client credential theft, much the same as password authentication over plain TLS is. The FIDO Alliance and the W3C have developed a passwordless authentication scheme known as FIDO2, which combines elements of the W3C's WebAuthn and FIDO's CTAP standards. This group will devise an EAP method suitable for use with passwordless authentication schemes such as the CTAP2 version of FIDO2.

While some EAP methods can provide some privacy there still can be a leakage of information as to which networks a particular user is accessing. Privacy pass protocols and tokens provide mechanisms to protect the user's privacy in this situation. This group will work on an EAP method based on Privacy Pass that provides privacy by preventing a visited network or service from knowing the identity of a user, and for keeping the user's identity provider from tracking what networks or services the user is accessing.
 

In summary, the working group shall produce the following standards track documents:

	* Documents for the maintenance and update of existing EAP protocols 

	* Define mechanisms by which EAP methods can support creation of long-term credentials for the peer based on initial limited-use credentials.

	* Develop an EAP method for use in constrained environments that wish to leverage the EDHOC key exchange mechanism.

	* Devise a passwordless EAP method that can incorporate use of CTAP2 or other similar authentication mechanism.

 	* EAP method based on Privacy Pass that provides privacy by preventing a visited network or service from knowing the identity of a user, and for keeping the user's identity provider from tracking what networks or services the user is accessing.

The working group is expected to stay in close collaboration with the EAP deployment community, the TLS working group (for work on TLS based EAP methods), the FIDO Alliance, and the 3GPP security architecture group (for EAP-AKA' work).

## Milestones

 * June 2025: WG adopts initial draft on an EAP method based on Privacy Pass
 * June 2025: EAP-TLSPOK - submit to IESG
 * Sept 2025: TEAP - resubmit to IESG
 * Nov 2025: EAP-EDHOC - submit to IESG
 * July 2026: EAP-FIDO - Submit to IESG

