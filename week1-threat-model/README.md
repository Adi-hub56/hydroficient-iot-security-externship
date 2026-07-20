# Week 1: IoT System Architecture & Threat Model

## Objective
Map Hydroficient's HYDROLOGIC IoT water management system as deployed at 
The Grand Marina Hotel, and produce a professional threat model identifying 
where the system could be attacked.

## What's Inside
- [`Grand_Marina_Threat_Model.pdf`](./Grand_Marina_Threat_Model.pdf) — full 
  threat model covering system architecture, asset inventory (CIA priorities), 
  a STRIDE analysis across 4 system components (24 threat scenarios total), 
  risk prioritization, and recommended mitigations.

## Approach
- Used the **CIA Triad** (Confidentiality, Integrity, Availability) to prioritize 
  which assets matter most and why
- Applied the **STRIDE framework** (Spoofing, Tampering, Repudiation, Information 
  Disclosure, Denial of Service, Elevation of Privilege) systematically across 
  the HYDROLOGIC devices, web dashboard, cloud API, and remote shutoff/gate controls
- Rated each threat by likelihood × impact and prioritized mitigations accordingly

## Key Finding
The most critical gap identified: the command channel that carries emergency 
shutoff instructions doesn't verify the sender's identity — meaning a forged 
"shutoff" command could cut water to all 500 rooms with no authentication check 
in place. This became the top-priority recommendation.

## Skills Demonstrated
Threat modeling, STRIDE analysis, risk assessment, security documentation 
for non-technical stakeholders
