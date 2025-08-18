graph TD
  %% --- Level 1 ----------------------------------------------------
  subgraph OFCIO
    OFC(OFCIO)
  end

  %% --- Level 2 ----------------------------------------------------
  subgraph CS[Cybersecurity]
  end

  OFC --> CS

  %% --- Level 3 – Initiatives ---------------------------------------
  %%  Burden reduction
  subgraph BR[Burden reduction]
    CTRL([Control Consolidation])
  end
  CS --> CTRL

  %%  Cloud
  subgraph CLOUD[Cloud]
    SEC([Cloud Security])
    FR([FedRAMP])
  end
  CS --> SEC
  CS --> FR

  %%  EO 14306
  subgraph COMM[Secure Communications]
    SEC_COM([Secure Communications])
  end
  CS --> SEC_COM

  %%  FISMA
  subgraph FISMA[<b>FISMA</b>]
    FCDM([FISMA and CDM Support])
    FMA([FISMA Metrics and Annual Report])
  end
  CS --> FCDM
  CS --> FMA

  %%  Incident Prevention & Response
  subgraph IR[Incident Prevention & Response]
    CDM([Continuous Diagnostics and Mitigation])
    IRO([Incident Response Operations])
    IRP([Incident Response Policy])
    PACC([Persistent Access Capability])
    SOC([Security Operations Center Consolidation])
  end
  CS --> CDM
  CS --> IRO
  CS --> IRP
  CS --> PACC
  CS --> SOC

  %%  Other
  subgraph OTH[Other]
    AI([AI and Cyber])
    CM([Cybersecurity Miscellaneous])
    DR([Drones])
    ST([Secure Telecommunications])
    SS([Space Systems])
    VEP([VEP – Vulnerabilities Equities Process])
  end
  CS --> AI
  CS --> CM
  CS --> DR
  CS --> ST
  CS --> SS
  CS --> VEP

  %%  Oversight
  subgraph OV[Oversight]
    CO([CISA Oversight])
    CNSS([CNSS/NSS])
    CB([Cyber BDR])
    CSF([Cyberstat])
    DCB([Dashboards (Cyber)])
    HVAP([High Value Asset (HVAs) Program])
  end
  CS --> CO
  CS --> CNSS
  CS --> CB
  CS --> CSF
  CS --> DCB
  CS --> HVAP

  %%  Zero Trust
  subgraph ZT[Zero Trust]
    IoT([IoT – Internet of Things])
    LOG([Logging])
    PQC([Post‑Quantum Cryptography (PQC)])
    SSFW([Secure Software])
    WG([Zero Trust Data Security Working Group])
    IM([Zero Trust Implementation Monitoring])
    PD([Zero Trust Policy Development])
  end
  CS --> IoT
  CS --> LOG
  CS --> PQC
  CS --> SSFW
  CS --> WG
  CS --> IM
  CS --> PD
