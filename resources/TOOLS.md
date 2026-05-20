# OSINT Tools Catalogue — Community Baseline

This catalogue is a curated starting point for MOC members. It is organised by functional category, includes suggested tags to aid filtering, and provides a short-risk and verification note for each entry.

Purpose:
- Provide a safe, pragmatic map of OSINT tools and workflows for education, reproducible research, and defensive awareness.
- Encourage consistent source assessment using a standard grading approach (see Admiralty/NATO guidance below).

Usage rules (always):
- Validate findings using multiple independent sources and record reference links and timestamps.
- Redact or avoid sharing personal data unless there is a clear, lawful, and documented purpose.
- Observe the Code of Conduct, Code of Ethics, and the Personal Data Protection Act 2010 [Act 709], including the Personal Data Protection (Amendment) Act 2024.

Tags (recommended):
- Scope: `Global`, `MY-focused` (Malaysia), `Regional`.
- Discipline: `GEOINT` (geospatial), `IMINT` (image), `SOCMINT` (social media), `OSINT` (general), `Metadata`, `Corp` (corporate), `Infra` (infrastructure/passive), `Verification`, `Automation`, `Mapping`, `Search`.
- Access: `Free`, `Freemium`, `Open`, `Paid`, `Requires-Account`.

How to read an entry:
- Name — Short description.  
- Tags: [Scope] / [Discipline] / [Access]
- Link: official project or documentation URL
- Notes: short practical note, legal/ethical flags, verification hints, and example use-case.

---

## Key Categories & Example Tools

### 1) Search & Discovery
- Purpose: find accounts, mentions, archived pages and raw leads.

- Google Dorks — Advanced search operators for targeted discovery.
	- Tags: Global / OSINT / Search / Free
	- Link: https://developers.google.com/search/docs/advanced/operators
	- Notes: Powerful but requires care to avoid targeting private resources. Record queries and timestamps.

- OSINT Framework — Organised index of OSINT tools and workflows.
	- Tags: Global / OSINT / Search / Open
	- Link: https://osintframework.com
	- Notes: Use as a reference directory; vet each tool before operational use.

  - Epieos / Email and phone reverse lookup
	- Tags: Global / Search / Open
    - Link: https://epieos.com/
	- Notes: If concerned about personal data, please go to https://epieos.com/privacy, the site do highlight how to delete personal data from the site.

### 2) Username & Account Footprinting
- Purpose: map public account footprints across platforms.

- Sherlock — Enumerates usernames across many public platforms.
	- Tags: Global / SOCMINT / Automation / Open
	- Link: https://github.com/sherlock-project/sherlock
	- Notes: Respect terms of service, do not attempt account takeover or credential checks.

- Social Searcher / Platform native search
	- Tags: Global / SOCMINT / Search / Paid/Free
    - Link: https://www.social-searcher.com/
	- Notes: Use layered verification; cross-reference profile details and posting histories.

 - holehe / Cross checking email accorss multiple sites
	- Tags: Global / SOCMINT / Free
    - Link: https://github.com/megadose/holehe 
	- Notes: Useful for cross referencing email across multiple sites. 

### 3) Geolocation & Mapping (GEOINT)
- Purpose: infer location from imagery, cues, and environmental detail.

- Google Maps / Street View
	- Tags: Global / GEOINT / Mapping / Free
	- Link: https://maps.google.com
	- Notes: Use street view, historical imagery and satellite layers; record imagery capture dates.

- OpenStreetMap & QGIS
	- Tags: Global / GEOINT / Mapping / Open
	- Link: https://www.openstreetmap.org, https://qgis.org
	- Notes: Combine OSM features with geospatial analysis in QGIS for reproducible mapping.

### 4) Imagery & Video Analysis (IMINT)
- Purpose: assess provenance, metadata, scene matching and manipulation.

- FotoForensics / InVID (video verif)
	- Tags: Global / IMINT / Verification / Open/Free
	- Notes: Useful for basic error level analysis and frame-level checks; always corroborate with other sources.

- Reverse image search (Google / TinEye / Bing)
	- Tags: Global / IMINT / Verification / Free
	- Notes: Useful for provenance checks and finding duplicates or original posts.

### 5) Metadata & File Analysis
- Purpose: inspect file headers, EXIF, and embedded technical attributes.

- ExifTool
	- Tags: Global / Metadata / Open
	- Link: https://exiftool.org
	- Notes: Extracts embedded metadata; beware of stripped or altered metadata and of leaking investigator metadata when sharing.

- Hachoir / binwalk (for advanced file inspection)
	- Tags: Global / Metadata / Open
	- Notes: For structured binary inspection; only used for defensible, lawful research.

### 6) Corporate & Records Research
- Purpose: map corporate ownership, filings, and public registry records.

- Maltego (Community/Pro)
	- Tags: Global / Corp / OSINT / Paid/Requires-Account
	- Link: https://www.maltego.com
	- Notes: Graph-based linkage analysis; vet sources and document provenance.

- Company registry portals (Malaysia: SSM MyCoID)
	- Tags: MY-focused / Corp / Official / Paid/Free depending on source
	- Notes: Use official registries for authoritative corporate data; log source links and retrieval dates.

### 7) Infrastructure & Passive Network Recon
- Purpose: domain/IP history, certificates, DNS, hosting and passive data enrichment.

- VirusTotal / Censys / Shodan
	- Tags: Global / Infra / Search / Freemium
	- Notes: Useful for historical artefacts and passive profiling; do not probe or attempt unauthorised access.

### 8) Verification & Attribution
- Purpose: frameworks and checklists for assessing claims and evidence.

- InVID verification plugin, Bellingcat methodologies
	- Tags: Global / Verification / Open
	- Notes: Follow structured verification steps; document each check with links and screenshots where permitted.

### 9) Automation & Data Processing
- Purpose: workflow automation, data cleaning, and enrichment.

- OpenRefine, Python (pandas), Google Sheets
	- Tags: Global / Automation / Data / Open
	- Notes: Keep scripts and transforms versioned and auditable; avoid re-publishing raw personal data.

### 10) Mapping, Visualisation & Reporting
- Purpose: create reproducible visualisations and evidence packages.

- QGIS, Kepler.gl, d3.js (for advanced visualisation)
	- Tags: Global / GEOINT / Mapping / Open
	- Notes: Produce reproducible maps with data sources and export raw data where permitted.

---

## Admiralty / NATO Source Reliability & Confidence (recommended)

MOC recommends using a structured source and information grading system to communicate confidence. The Admiralty (NATO) system is a widely used model. At minimum, each written analysis should record:

- Source Reliability: graded A (Completely reliable) → E (Unreliable) according to source history and verifiability.
- Information Credibility: graded 1 (Confirmed) → 5 (Improbable) based on corroboration and evidence.

Example statement: "Source X (B/2) — Source reliability B (usually reliable); information assessed 2 (probably true) with geolocation and timestamp corroboration from independent imagery."

Use the grading to reduce misinformation risk and to make implicit uncertainty explicit for readers.

### Admiralty Matrix

| Source reliability | Meaning | Information credibility | Meaning |
| --- | --- | --- | --- |
| A | Completely reliable | 1 | Confirmed by other sources |
| B | Usually reliable | 2 | Probably true |
| C | Fairly reliable | 3 | Possibly true |
| D | Not usually reliable | 4 | Doubtful |
| E | Unreliable | 5 | Improbable |
| F | Cannot be judged | 6 | Cannot be judged |

Notes:
- Use the matrix to communicate both who the source is and how strong the information appears.
- If either side cannot be assessed, write that explicitly rather than guessing.
- Keep the grading separate from the final analytical judgement.

---

## Contribution Template (for adding tools)

When proposing a new tool entry, submit using this format in a PR against `resources/TOOLS.md`:

- Name — Short description
- Tags: [Scope] / [Discipline] / [Access]
- Link: Official homepage or documentation
- Purpose: one-sentence primary use-case
- Verification notes: what checks are suggested to validate outputs from this tool
- Legal/Risk Flags: any terms-of-service, privacy or misuse concerns
- Example/Quick use: 1–2 line example or command
- Maintainer / Contributor: GitHub handle or community contact

All submissions must follow MOC contribution standards: include Purpose, Context, Verification and Risk Check. Do not add tools that enable unauthorised access, exploitation, or evasion techniques.

---

## Curator Notes & Suggested Improvements

- Add short screencast examples for high-value tools (hosted privately for members where necessary) to speed onboarding.
- Maintain a small matrix (CSV) of tools with columns for `Name, Tags, URL, License, VerificationNotes, RiskFlags` to enable automated filtering.
- Consider a regular quarterly review of the catalogue by the Research & Technical pillar to remove outdated or harmful entries.

---

## Quick Reminders

- Always document source URLs, capture timestamps, and the steps used to derive conclusions.  
- When sharing examples, redact personal identifiers unless you have lawful justification and consent.  
- If unsure, pause and seek guidance from the Operations or Community Support pillars.

---

This catalogue is a living document. Contributions are welcome under the rules in `CONTRIBUTING.md`.
