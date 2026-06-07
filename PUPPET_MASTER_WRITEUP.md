# Hack The Box - Puppet Master OSINT Challenge Writeup

**Author:** Yash (Dead Pirate Society)  
**Date:** June 2026  
**Difficulty:** Medium  
**Category:** OSINT (Open Source Intelligence)

---

## Executive Summary

The Puppet Master challenge presents a multi-layered OSINT investigation centered around a military vehicle identification scenario. This writeup details the methodology, tools, and thought process used to successfully extract all required intelligence artifacts.

---

## Challenge Overview

**Initial Access:** Upon starting the challenge, we are presented with a web interface containing an image of a military vehicle and a series of intelligence-gathering questions.

**Objective:** Extract specific technical and historical data about the vehicle through systematic OSINT techniques.

---

## Intelligence Gathering Methodology

### Phase 1: Image Analysis & Vehicle Identification

**Tool Selection:**
- Primary: Vehicle AI (specialized image recognition)
- Secondary: Google Gemini (verification and cross-referencing)

**Process:**
1. Downloaded the provided military vehicle image
2. Fed the image through Vehicle AI for initial classification
3. Cross-verified results using Gemini's multimodal capabilities
4. Successfully identified vehicle model and manufacturer

**Key Insight:** Using multiple AI models for verification reduces false positives and increases confidence in identifications.

---

### Phase 2: Historical Research & Operational Deployment

**Challenge:** Determining the year of first operational deployment

**Initial Approach (Failed):**
- Extensive document analysis
- Scanned hundreds of military documents
- Searched specialized defense databases

**Breakthrough:**
- Pivoted to Wikipedia as a structured data source
- Located the vehicle's main article
- Scanned entire page content
- **Critical Discovery:** Infobox at the top of the page displayed "1997–present"

**Lesson Learned:** Sometimes the answer is in plain sight. Always check infoboxes, summaries, and metadata before diving deep into document bodies.

**Answer:** `1997`

---

### Phase 3: Geolocation & Corporate Intelligence

**Question:** Country/Region of Origin

**Methodology:**
1. Identified manufacturer: **Thales Australia**
2. Analyzed corporate structure:
   - Thales (French multinational)
   - Thales Australia (subsidiary)
3. Cross-referenced with vehicle production facilities
4. Confirmed Australian origin through:
   - Company registration data
   - Manufacturing facility locations
   - Defense procurement records

**Answer:** `Australia`

---

### Phase 4: Technical Specifications

**Question:** Passenger Capacity

**Approach:**
- Leveraged Gemini's knowledge base
- Queried: "Passenger capacity of [vehicle model]"
- Verified against multiple sources:
  - Manufacturer specifications
  - Military manuals
  - Defense forums

**Answer:** [Specific passenger count - verified via AI assistance]

---

## Tools & Resources Utilized

| Tool | Purpose | Effectiveness |
|------|---------|---------------|
| Vehicle AI | Initial image classification | High |
| Google Gemini | Verification & technical queries | Very High |
| Wikipedia | Historical data & specifications | Medium-High |
| Manual OSINT | Cross-referencing & validation | Essential |

---

## Advanced OSINT Techniques Demonstrated

### 1. **Multi-Model Verification**
Using multiple AI systems creates a verification layer that increases accuracy and reduces reliance on single-source failures.

### 2. **Structured Data Mining**
Wikipedia infoboxes, corporate registration databases, and technical specification sheets often contain answers that paragraph-text searches miss.

### 3. **Corporate Genealogy Analysis**
Tracing Thales → Thales Australia revealed the vehicle's true origin, demonstrating the importance of understanding corporate structures in OSINT.

### 4. **Pivot Strategy**
When document-based research failed (Phase 2), the ability to pivot to alternative sources (Wikipedia) was crucial.

---

## Challenges & Solutions

### Challenge 1: Document Overload
- **Problem:** Hundreds of documents, no clear answer
- **Solution:** Pivoted to structured encyclopedia sources
- **Takeaway:** Know when to abandon a failing approach

### Challenge 2: Ambiguous Manufacturer Data
- **Problem:** Thales is French, but vehicle is Australian
- **Solution:** Researched subsidiary relationships
- **Takeaway:** Corporate structures matter in OSINT

### Challenge 3: Verification of AI Output
- **Problem:** Ensuring AI-provided answers are accurate
- **Solution:** Cross-referenced with multiple sources
- **Takeaway:** AI assists; verification validates

---

## Operational Security (OPSEC) Considerations

During real-world OSINT operations:
- Avoid predictable search patterns
- Use VPNs and anonymity tools
- Be aware of digital footprint
- Document methodology for reproducibility

---

## Skills Demonstrated

✅ Image recognition and classification  
✅ Multi-source intelligence correlation  
✅ Historical research techniques  
✅ Corporate structure analysis  
✅ AI-assisted verification  
✅ Adaptive research strategies  
✅ Technical specification extraction  

---

## Lessons for Future CTF Challenges

1. **Start Simple:** Check infoboxes and summaries first
2. **Verify Everything:** AI is a tool, not an oracle
3. **Pivot Fast:** Don't marry one approach
4. **Document as You Go:** Methodology matters as much as answers
5. **Corporate Intelligence:** Subsidiaries and partnerships reveal hidden connections

---

## Conclusion

Puppet Master demonstrates the layered nature of modern OSINT challenges. Success requires:
- Technical tool proficiency
- Adaptive research strategies
- Cross-source verification
- Patience and systematic approaches

The challenge reinforces that OSINT is not about finding a single "smoking gun" document, but rather synthesizing intelligence from multiple sources to build a complete picture.

**Flag Captured:** ✅  
**Intelligence Objectives Met:** ✅  
**Skills Sharpened:** ✅

---

## References & Further Reading

- NATO OSINT Handbook
- Bellingcat's OSINT Methodology
- Corporate structure databases (OpenCorporates, etc.)
- Vehicle recognition guides (Jane's Defense, etc.)

---

**Team:** Dead Pirate Society  
**Specialization:** Ethical Hacking & Digital Forensics

---

*"In OSINT, the answer is rarely hidden—it's just waiting to be recognized."*
