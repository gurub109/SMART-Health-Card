# SMART-Health-Card

In the previous article [Decentralized Identity (DID) and Verifiable Credentials (VC)](https://github.com/gurub109/Decentralized-Identity-and-Verifiable-Credentials) we looked at why we need DIDs, VCs and its related components. In this article we will cover SMART Health Card and how it leverages the DID and VC technology to issue, share and validate vaccination records bound to an individual identity.

## Vaccine Credential Initiative (VCI)

VCI is a voluntary coalition of public and private organizations whose charter is to empower individuals to receive vaccination records as verifiable credentials (VCs) from issuers such as pharmacy, doctor's office or state immunication registry. Individuals can use those VCs for medical purposes and to demonstrate their vaccination status to safely return to work, school, travel, etc. Participating members have developed a SMART Health Cards Framework Implementation Guide which is based on the [W3C Verifiable Credentials Standard](https://www.w3.org/TR/vc-data-model/) and [Health level 7 (HL7) SMART on FHIR Standard](https://docs.smarthealthit.org/).

## SMART Health Cards Framework

The framework provides an implementation guide for **"Health Cards"** which can work across organizational and jurisdictional boundaries through open standards and decentralized infrastructure.

### FHIR Implementation Guide (IG)

The [FHIR Implementation Guide](https://www.hl7.org/fhir/implementationguide.html) describes the clinical information necessary to create [SMART Health Card](https://healthwallet.cards/) identifying vaccination and laboratory testing status for infectious diseases such as [COVID-19](https://www.cdc.gov/coronavirus/2019-ncov/index.html).

The implementation guide (IG) defines how **Issuers** who are entities repossible for giving vaccinations or reporting laboratory results such as health systems, pharmacies, clinical labs, doctor offieces, etc., should produce the FHIR resources. The **Holder** who received the vaccination can represent the credentials to **Verifiers** who read and analyze the FHIR resoruces described in the IG. The data flow follows the standard defined by [W3C Verifiable Credentials Standard](https://www.w3.org/TR/vc-data-model/).

![image](https://user-images.githubusercontent.com/26188338/124400768-2cf67100-dce2-11eb-824b-c58c9c3465dc.png)

### Health Card

The SMART Health Cards are 2D barcode (QR code) containing the clinical information, such as vaccination history or test results. Per IG, the **Health Card** issued should consider the scenarios where a **Holder** may not have a smart phone, internet access, and/or printer. Hence a holder can receive the card in the following ways:

* A paper copy of the QR code may be handed by the issuer at the time of the vaccination or test visit
* A paper copy may be mailed by the issuer after the visit
* Holder can download the card from a issuer website or app hosted and print a copy and/or save it as a digital file
* Holder can connect their health records to an app that implements SMART Health Card specification

Based on the modality of the SMART Health Card, the holder can share with the verifier just like sharing a paper copy of immunization records with a school, faxing medical records to a physician's office or using a credit card at a restaurant. The verifier can manually scan the presented QR code or provide a self-service kiosk. 


