# Changelog

## 1.3.1 — 12 October 2026

Editorial, accessibility, print-production and design corrections applied after an independent review of the published site.

- **Fixed the contents order.** The network troubleshooting flow is listed in the table of contents at the position it actually occupies in the document, and now links to a real heading anchor.
- **Generated IDs for every heading**, so all 77–99 in-page links per edition resolve instead of pointing nowhere.
- **Added a caption to all 89 tables**, giving each one an accessible name.
- **Added `<main id="main">` and `<footer>` landmarks and a skip link** to each edition.
- **Replaced four competing stylesheets** with one clean stylesheet, removing 30 `!important` declarations and the rules that could never match.
- **Print: switched from US Letter to A4**, set body text to 10.5 pt, and removed the forced break that left a page 87% empty. Browsers are now told to print A4.
- **Added page numbers and a running head** to the supplied PDFs and Word documents.
- **Corrected the type scale**: the title is no longer oversized, table of contents entries are no longer smaller than body text, and mobile table text is larger.
- **Repaired three dead links** (GNS3 documentation, NetBox, IPv6 subnet calculator).
- **Added page metadata** to every page: description, canonical URL, Open Graph and Twitter tags, favicon and theme colour.
- **Added dark mode**, a skip link, reduced-motion support and larger anchor scroll margins so headings are not hidden behind the sticky toolbar.
- **Redesigned the landing page** so it matches the design system used inside the documents, with aligned cards, clearer link hierarchy and a topology diagram.

## 1.3 — 12 October 2026


- Differentiated Basic, Intermediate and Advanced editions with level-specific troubleshooting guidance, examples and scenarios.
- Added an accessible visual network troubleshooting flow with decision branches.
- Expanded escalation triggers, evidence capture and change-safety guidance.
- Added targeted intermediate subnetting, VLAN/SVI, DHCP/DNS and packet-capture workbench.
- Added advanced routing, ACL/firewall, OSPF, EtherChannel, IPv6 and automation scenarios.
- Clarified Cisco CCNA v1.1/v2.0 timing to avoid describing the future v2.0 exam as already active.
- Updated the DHCPv6 standards reference to RFC 9915 (January 2026), which obsoletes RFC 8415.
- Standardised release/version wording, publication disclosure and GitHub download paths.
- Regenerated HTML, editable DOCX, printable PDF and release ZIPs; QA limitations are listed separately.
