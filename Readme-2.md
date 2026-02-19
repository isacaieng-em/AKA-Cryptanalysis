 Formal Cryptanalysis and Robust AKA Protocol Design for IIoT

[![ProVerif](https://img.shields.io/badge/Verification-ProVerif2.04-blue)](https://proverif.inria.fr/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![IIoT Security](https://img.shields.io/badge/Field-IIoTSecurity-orange)]()

This repository serves as the official companion to the paper "A Robust Multifactor Authentication and Key Agreement Protocol in Industrial Internet of Things". It contains the full formal verification artifacts using the automated symbolic reasoner ProVerif and theoretical mathematical derivations of vulnerabilities in contemporary SOTA schemes.

 Key Contributions

- Automated Proofs: Complete ProVerif models for Category A (Secrecy), B (KCI Resilience), and C (Rotation Integrity).
- SOTA Cryptanalysis: Theoretical and symbolic attack models for 6 major protocols (Han et al., ERASMIS, LEAF-IIoT, REAP-IIoT, RePUF-IoT, SKAP).
- Proposed Scheme: A robust, asymmetric computational design reducing sensor load by 99.9% while ensuring Perfect Forward Secrecy (PFS).

 

 Repository Structure

 [1. Proposed Scheme (Codes & Logs)](./Ours____ProposedScheme____ProVerif-Analysis-(Codes&Logs)/)
Formal verification of our rectified protocol.
- [A.pv](./Ours____ProposedScheme____ProVerif-Analysis-(Codes&Logs)/A.pv): Core Secrecy & Mutual Authentication model.
- [B.pv](./Ours____ProposedScheme____ProVerif-Analysis  (Codes&Logs)/B.pv): KCI & Insider Attack resistance model.
- [C.pv](./Ours____ProposedScheme____ProVerif-Analysis  (Codes&Logs)/C.pv): Key Rotation & Desynchronization verification.
- [Logs](./Ours____ProposedScheme____ProVerif-Analysis  (Codes&Logs)/A-Log.txt): Raw ProVerif execution outputs.

 [2. Han et al. Cryptanalysis](./SOTA____Han  et  al____ProVerif-Analysis (Codes-Logs)/)
Demonstrating KCI and Sensor Impersonation (CRT) vulnerabilities.
- [Theoretical Analysis](./SOTA____Han  et  al____Theoretical-Cryptanalysis/AKA-YIran-HAn.pdf)
- [ProVerif Attack Models](./SOTA____Han  et  al____ProVerif-Analysis  (Codes&Logs)/proverif-Han-ok-1.pv)

 [3. LEAF-IIoT & REAP-IIoT Cryptanalysis](./SOTA____LEAF-IIoT____Theoretical-Cryptanalysis/)
Evidence of tracking, desynchronization, and forward secrecy failures.
- [LEAF Models](./SOTA____LEAF-IIoT____ProVerif-Analysis  (Codes&Logs)/LEAF-IIoT-2-OK.pv)
- [REAP Models](./SOTA____REAP-IIoT____ProVerif-Analysis  (Codes&Logs)/proverif-REAP-IIoT-1-ok.pv)

 [4. ERASMIS, RePUF & SKAP](./SOTA____SKAP____Theoretical-Cryptanalysis/)
Evaluation of heavy-weight ECC dependencies and logical flaws.
- [RePUF Logic](./SOTA____RePUF-IIoT____ProVerif-Analysis  (Codes&Logs)/ProVerif-RePUF-1-ok.pv)
- [SKAP LaTeX/Theoretical](./SOTA____SKAP____Theoretical-Cryptanalysis/SKAP----6.tex)



  How to Reproduce

To run the formal verification models:

1.  Install ProVerif: Download from [ProVerif Official Website](https://prosecco.gforge.inria.fr/software/proverif/).
2.  Execute a model:
 
    proverif Ours____ProposedScheme____ProVerif-Analysis\ (Codes\&Logs)/A.pv
 
3.  Analyze Logs: Compare the output with the `.txt` log files provided in the corresponding directories.


 

Contact
For academic inquiries or collaboration, please contact the lead researcher:
Hassan Nasiraee - nasiraee@ausmt.ac.ir