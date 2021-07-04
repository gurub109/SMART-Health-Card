# SMART-Health-Card

The article [Decentralized Identity (DID) and Verifiable Credentials (VC)](https://github.com/gurub109/Decentralized-Identity-and-Verifiable-Credentials) covered the need for DIDs, VCs and its related components. The present article discusses the SMART Health Card Framework and how it leverages VC technology to issue, share and validate vaccination records bound to an individual identity.

## Vaccine Credential Initiative (VCI)

VCI is a voluntary coalition of public and private organizations whose charter is to empower individuals to receive vaccination records as verifiable credentials (VCs) from issuers such as **pharmacy, doctor's office or state immunization registry.** Individuals can use those VCs for medical purposes and to demonstrate their vaccination status to safely return to work, school, travel, etc. Participating members have developed a SMART Health Cards Framework Implementation Guide which is based on the [W3C Verifiable Credentials Standard](https://www.w3.org/TR/vc-data-model/) and [Health Level 7 (HL7) SMART on FAST Health Interoperability Resources (FHIR) Standard](https://docs.smarthealthit.org/).

## SMART Health Cards Framework

The framework provides an implementation guide for **"Health Cards"** which can work across organizational and jurisdictional boundaries through open standards and decentralized infrastructure.

### FHIR Implementation Guide (IG)

The [FHIR Implementation Guide](https://www.hl7.org/fhir/implementationguide.html) describes the clinical information necessary to create [SMART Health Card](https://healthwallet.cards/) identifying vaccination and laboratory testing status for infectious diseases such as [COVID-19](https://www.cdc.gov/coronavirus/2019-ncov/index.html).

The implementation guide (IG) defines how **Issuers** who are entities responsible for giving vaccinations or reporting laboratory results such as health systems, pharmacies, clinical labs, doctor offices, etc., should produce the FHIR resources. The **Holder** who received the vaccination can present the credentials to **Verifiers** who read and analyze the FHIR resources described in the IG. The data flow follows the standard defined by [W3C Verifiable Credentials](https://www.w3.org/TR/vc-data-model/).

![image](https://user-images.githubusercontent.com/26188338/124400768-2cf67100-dce2-11eb-824b-c58c9c3465dc.png)

### Health Card

The SMART Health Cards are 2D barcode (QR code) containing the clinical information, such as vaccination history or test results. Per FHIR IG, the **Health Card** issued should consider the scenarios where a **Holder** may not have a smart phone, internet access, and/or printer. Hence a holder can receive the card in the following ways:

* A paper copy of the QR code may be handed by the issuer at the time of the vaccination or test visit
* A paper copy may be mailed by the issuer after the visit
* Holder can download the card from the issuer website or app hosted and print a copy and/or save it as a digital file
* Holder can connect their health records to an app that implements SMART Health Card specification

Based on the modality of the SMART Health Card, the holder can share with the verifier just like sharing a paper copy of immunization records with a school, faxing medical records to a physician's office or using a credit card at a restaurant. The verifier can manually scan the presented QR code or provide a self-service kiosk. 

## SMART Health Card Design Goals

* Anyone can issue Health cards and a verifier can make its own decision about which issuer to **trust.** Verifiers can discover public keys associated with an issuer via **/.well-known/jwks.json URLs**
* Cryptographic keys are generated and resolved using 256 bit Elliptic Curve
* Holder can disclose minimum amount of information necessary for a given use case 
* Issuer should limit the data elements to the requirements of the Health Card FHIR profile

### Credential Types

In the implementation guide (IG) the following Verifiable Credential (VC) and its sub-types are defined:

* A VC designed to convey a "Health Card" which is bound to a subject's identity with their clinical data
  * A Health Card designed to convey COVID-19 details
  * A Health Card designed to convey immunization details
  * A health Card designed to convey laboratory results

# References

* [Verifiable Credential Initiative](https://vci.org/)
* [SMART Health Cards Framework](https://spec.smarthealth.cards/)
* [Health Cards](https://smarthealth.cards/)
* [SMART Health Card Implementation Guide (IG)](https://github.com/smart-on-fhir/health-cards)
* [FAST Health Interoperability Resources (FHIR)](https://hl7.org/fhir/)



 



