# awesome-security-data-feeds
Curated list of Security Data Feeds of vendors, programming languages ecosystem, etc

## Scope
- Focus: machine-consumable security data feeds, advisory databases, and primary upstream sources
- Labels:
  - `official` - primary upstream source maintained by the vendor, project, or ecosystem
  - `aggregator` - combines or republishes data from multiple upstream sources
  - `legacy` - older source kept for reference or compatibility

## General vulnerability databases
- NVD (NIST National Vulnerability Database) [`official`] - https://nvd.nist.gov/
- OSV (Open Source Vulnerabilities) [`aggregator`] - https://osv.dev/
- GitHub Advisory Database [`aggregator`] - UI: https://github.com/advisories, data: https://github.com/github/advisory-database
- GitLab Advisory Database [`aggregator`] - https://advisories.gitlab.com/
- Sonatype OSS Index [`aggregator`] - https://ossindex.sonatype.org/
- CISA Known Exploited Vulnerabilities (KEV) [`official`] - catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog, data: https://github.com/cisagov/kev-data

## Language ecosystems
- Go Vulnerability Database [`official`] - https://vuln.go.dev/
- RustSec Advisory Database [`official`] - https://github.com/RustSec/advisory-db
- RubySec Advisory Database [`official`] - https://github.com/rubysec/ruby-advisory-db
- FriendsOfPHP Security Advisories [`official`] - https://github.com/FriendsOfPHP/security-advisories
- PyPA Advisory Database [`official`] - https://github.com/pypa/advisory-database
- PyUp Safety DB [`aggregator`] - https://github.com/pyupio/safety-db
- Haskell Security Advisories [`official`] - https://github.com/haskell/security-advisories
- Node.js Security WG [`official`, process/advisories] - https://github.com/nodejs/security-wg

## Vendor advisories
- Microsoft MSRC Update Guide [`official`] - https://msrc.microsoft.com/update-guide
- Apple Security Updates [`official`] - https://support.apple.com/en-us/HT201222
- Adobe Security Bulletins [`official`] - https://helpx.adobe.com/security.html
- Android Security Bulletins [`official`] - https://source.android.com/docs/security/bulletin
- Cisco Security Advisories [`official`] - https://tools.cisco.com/security/center/publicationListing.x
- Oracle Critical Patch Updates and Security Alerts [`official`] - https://www.oracle.com/technetwork/topics/security/alerts-086861.html
- Chainguard Security Advisories [`official`] - https://images.chainguard.dev/security/

## OS and distro feeds
- Amazon Linux Security Center (ALAS) [`official`] - https://alas.aws.amazon.com/
- Red Hat Security Updates [`official`] - https://access.redhat.com/security/security-updates/
- Ubuntu Security Notices (USN) [`official`] - https://ubuntu.com/security/notices
- Debian Security Tracker [`official`] - https://security-tracker.debian.org/tracker/
- Arch Linux Security Tracker [`official`] - https://security.archlinux.org/
- Alpine SecDB [`official`] - https://secdb.alpinelinux.org/
- Gentoo Linux Security Advisories (GLSA) [`official`] - https://security.gentoo.org/glsa/
- Oracle Linux Security Advisories [`official`] - https://linux.oracle.com/security/
- AlmaLinux Errata [`official`] - https://errata.almalinux.org/
- Rocky Linux Errata [`official`] - https://errata.build.resf.org/
- SUSE Security Updates [`official`] - https://www.suse.com/support/update/
- FreeBSD Security Advisories [`official`] - https://www.freebsd.org/security/advisories/
- OpenBSD Security Advisories [`official`] - https://www.openbsd.org/security.html

## Enrichment and prioritization
- FIRST EPSS (Exploit Prediction Scoring System) [`official`] - site: https://www.first.org/epss, API: https://api.first.org/data/v1/epss
- CISA Vulnrichment [`official`] - https://github.com/cisagov/vulnrichment

## Machine-readable vendor advisories (CSAF/VEX)
- Red Hat Security Data API [`official`] - security data: https://access.redhat.com/security/data, CSAF API: https://access.redhat.com/hydra/rest/securitydata/csaf.json
- Siemens ProductCERT Advisories [`official`] - advisory hub: https://www.siemens.com/en-us/content/cert-services/, CSAF feed available from advisory hub
- Cisco Security Advisories [`official`] - advisory pages provide downloadable CSAF, example: https://sec.cloudapps.cisco.com/security/center/content/CiscoSecurityAdvisory/
- OPC Foundation Security Advisories [`official`] - https://github.com/OPCFoundation/OPC-SecurityAdvisories

## Raw data repos and source mirrors
- CVE Project cvelistV5 [`official`] - https://github.com/CVEProject/cvelistV5
- CVE Project cvelist [`legacy`] - https://github.com/CVEProject/cvelist

## Malware and typosquatting datasets
- OSSF Malicious Packages [`official`] - https://github.com/ossf/malicious-packages
- DataDog Malicious Software Packages Dataset [`aggregator`] - https://github.com/DataDog/malicious-software-packages-dataset
- FOSSA Malware Impacted Packages [`aggregator`] - https://github.com/fossas/fossa-malware-impacted-packages
- Malware Packages (community list) [`aggregator`] - https://github.com/whodinner/malware-packages
- Typosquatting Dataset [`aggregator`] - https://github.com/ecosyste-ms/typosquatting-dataset

## Schemas and standards
- OSSF OSV Schema - https://github.com/ossf/osv-schema

## Tools and secondary indexes
- cve-search - https://github.com/cve-search/cve-search
- Awesome CVE PoC - https://github.com/qazbnm456/awesome-cve-poc
- Awesome Security - https://github.com/sbilly/awesome-security
