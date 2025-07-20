 CertStack  Decentralized Credential Verification System

CertStack is a blockchainbased credential verification platform that enables educational institutions to issue tamperproof certificates and allows employers to instantly verify academic credentials with complete trust and transparency.

 Features

 TamperProof Certificates: All certificates are stored on the blockchain with cryptographic hashes
 Instant Verification: Employers can verify credentials in realtime without contacting institutions
 Authorized Institutions: Only verified educational institutions can issue certificates
 Batch Verification: Employers can verify multiple certificates simultaneously
 Expiry Management: Support for certificates with expiration dates
 Comprehensive Metadata: Store detailed certificate information including type and custom metadata

 Smart Contract Functions

 Authorization Management
 authorizeinstitution: Add an educational institution to the authorized list (owner only)
 revokeinstitution: Remove an institution from the authorized list (owner only)
 isinstitutionauthorized: Check if an institution is authorized to issue certificates

 Certificate Issuance
 issuecertificate: Issue a new certificate (authorized institutions only)
   Parameters: recipient, certificatehash, expirydate, certificatetype, metadata
   Returns: unique certificate ID

 Verification Functions
 verifycertificate: Get complete certificate details by ID
 verifycertificatehash: Verify if provided hash matches stored certificate hash
 iscertificatevalid: Check if certificate is still valid (not expired)
 batchverifycertificates: Verify multiple certificates at once

 Query Functions
 getrecipientcertificates: Get all certificate IDs for a specific recipient
 getinstitutioncertificates: Get all certificate IDs issued by an institution
 getcertificatecount: Get total number of certificates issued

 Usage

 For Educational Institutions
1. Get authorized by the contract owner
2. Issue certificates using issuecertificate with recipient details and certificate hash
3. Track issued certificates using getinstitutioncertificates

 For Employers
1. Use verifycertificate to get complete certificate details
2. Use verifycertificatehash to verify certificate authenticity
3. Use iscertificatevalid to check if certificate hasn't expired
4. Use batchverifycertificates for multiple credential verification

 For Certificate Recipients
1. View your certificates using getrecipientcertificates
2. Share certificate IDs with potential employers for verification

 Security Features

 Access Control: Only authorized institutions can issue certificates
 Immutable Records: Once issued, certificates cannot be modified
 Hash Verification: Certificate authenticity verified through cryptographic hashes
 Expiry Management: Automatic validation of certificate expiration dates

 Getting Started

1. Deploy the contract to Stacks blockchain
2. Authorize educational institutions using authorizeinstitution
3. Institutions can begin issuing certificates
4. Employers can verify credentials using the verification functions

 Technical Details

 Built with Clarity smart contract language
 Compatible with Stacks blockchain
 Supports up to 100 certificates per recipient
 Supports up to 1000 certificates per institution
 Certificate metadata limited to 500 characters
 Certificate type limited to 50 characters

 Error Codes

 u100: Owner only operation
 u101: Institution not authorized
 u102: Certificate already exists
 u103: Certificate not found
 u104: Invalid input parameters

 License
This project is licensed under the MIT License - see the LICENSE file for details.
