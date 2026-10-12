# Quality assurance report — Release 1.3.1

Review date: 12 October 2026

## Release contents and format checks

| Edition | HTML words | DOCX tables | PDF pages | Page size | PDF text extracted |
|---|---:|---:|---:|---|---|
| Advanced Networking & CCNA | ~10,500 | 31 | 61 | A4 | Yes |
| Intermediate Networking | ~8,800 | 30 | 55 | A4 | Yes |
| Basic Networking | ~8,500 | 28 | 52 | A4 | Yes |

Supplied PDFs are **A4 (210 × 297 mm)**. Previous releases shipped US Letter (216 × 279 mm), which is not the standard paper size in Australia, the UK or the EU.

## Automated checks performed on this build

- All three editions: single stylesheet, three `!important` declarations remaining, zero dead selectors.
- Table captions: 31 / 30 / 28 tables and 31 / 30 / 28 captions respectively.
- In-page links: every anchor target resolves — zero unresolved across all three editions.
- Table of contents order matches document order in all three editions.
- Landmarks present: `main`, `footer`, skip link; `lang="en-AU"`.
- Metadata present on all pages: description, canonical, Open Graph, Twitter card, favicon, theme colour.
- External links: 123 of 126 reachable. Thirteen return HTTP 403 to automated requests only (Cloudflare-protected sites such as Stack Overflow, Reddit and Cloudflare Learn); three previously failed with 404 and have been repaired.
- No blank pages in any generated PDF. Mean page fill 84%, median 89%.

## Technical fact-checks and corrections

- **CCNA exam timing:** verified against Cisco's own announcements. The 200-301 CCNA v1.1 exam is available through 2 February 2027 and v2.0 testing begins 3 February 2027. The advanced edition labels v2.0 as forward-looking preparation and directs readers to match the blueprint to their exam date.
- **DHCPv6:** the standards reference was updated from RFC 8415 to **RFC 9915**, published January 2026, which obsoletes RFC 8415 and is now an Internet Standard (STD 102).
- **IPv6:** link-local, global unicast, unique local and multicast ranges are correctly distinguished; NDP versus ARP and SLAAC versus DHCPv6 are separated; the default router is described as normally learned through Router Advertisements, not DHCPv6.
- **SMTP:** TCP 25 relay, TCP 587 submission with STARTTLS and TCP 465 implicit-TLS submission are distinguished, with a caveat that provider configuration varies.
- **Wi-Fi:** symptom-first workflow retained, with WPA2-Personal separated from WPA2-Enterprise / 802.1X.
- **Subnetting and media:** /16–/23 reference values retained, and the conventional usable-host calculation is explicitly not applied to /31 and /32. Copper and fibre figures remain qualified by installation, channel, transceiver and standard.

## Changes made in this release

- The exported HTML pages were rebuilt with one stylesheet instead of four cascading blocks, removing the need for the earlier `36em` override.
- Print rules were consolidated: A4, 10.5 pt body text, `orphans`/`widows` extended to list items, repeated table headers across split tables, and no forced break after the contents.
- Landing page redesigned to share the documents' design tokens.

## Known limitations

- The HTML internal links and landing-page paths were checked automatically. A targeted set of authoritative references was checked via current search results, including Cisco CCNA, IETF RFC 9915, RFC 4861, RFC 4862, RFC 6409, RFC 8314 and Microsoft wireless troubleshooting. **Not every external URL was independently opened or tested end-to-end**, and linked pages can change.
- PDFs are generated from the HTML rather than from the editable Word files. They therefore paginate differently from the Word version, although they carry the same content, the same A4 page size and the same page numbering. If the Word file is edited, the PDF should be regenerated from it.
- Dark mode is enabled on the landing page and in the editions. Print output is always light.
- This is an educational reference, not a guarantee of correctness for every vendor, software version or network design. Verify critical commands and changes in an authorised lab or an approved change window.
