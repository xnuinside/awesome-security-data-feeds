# awesome-security-data-feeds
Curated list of machine-consumable security data feeds, advisory databases, and primary upstream sources.

## Scope
- Includes: advisory databases, vulnerability feeds, machine-readable vendor advisories, raw upstream data repos, enrichment datasets
- Excludes: generic security link collections unless they are useful as secondary discovery indexes

## Labels
- `official` - primary upstream source maintained by the vendor, project, or ecosystem
- `aggregator` - combines or republishes data from multiple upstream sources
- `legacy` - older source kept for reference or compatibility

## GitHub Advisory Database overlap
- `overlaps GHADB` - advisory content is documented as also appearing in GitHub Advisory Database
- `downstream of GHADB` - source consumes or republishes GitHub Advisory Database content

## OSV overlap
- `represented in OSV` - source or ecosystem is documented as present in OSV.dev data

## General vulnerability databases
| Name | Label | Coverage | Format / Access | Link |
| --- | --- | --- | --- | --- |
| NVD (NIST National Vulnerability Database) | `official` | CVE/NVD | API, JSON feeds, website | https://nvd.nist.gov/ |
| OSV (Open Source Vulnerabilities) | `aggregator` | Open source ecosystems | API, OSV format, website | https://osv.dev/ |
| GitHub Advisory Database | `aggregator` | Open source ecosystems | UI + raw data repo | UI: https://github.com/advisories, data: https://github.com/github/advisory-database |
| GitLab Advisory Database | `aggregator` | Open source ecosystems | Website + advisory records | https://advisories.gitlab.com/ |
| Packagist Security Advisory Feed | `aggregator` | PHP / Composer | API-backed advisory feed; downstream of GHADB via GitHub Security Advisories and also aggregates FriendsOfPHP; represented in OSV (Packagist ecosystem) | https://packagist.org/security-advisories/ |
| Sonatype OSS Index | `aggregator` | Open source ecosystems | API, website | https://ossindex.sonatype.org/ |
| CISA Known Exploited Vulnerabilities (KEV) | `official` | Known exploited CVEs | Catalog + raw data repo | Catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog, data: https://github.com/cisagov/kev-data |

## Language ecosystems
| Name | Label | Ecosystem | Notes | Link |
| --- | --- | --- | --- | --- |
| Go Vulnerability Database | `official` | Go | Primary Go vuln feed; overlaps GHADB (documented GitHub import source); represented in OSV | https://vuln.go.dev/ |
| NuGet Vulnerability Info API | `official` | .NET / NuGet | Machine-readable vulnerability files consumed by NuGet clients; Microsoft docs use GitHub Advisories Database as an example upstream, but nuget.org backing source not verified here; represented in OSV (NuGet ecosystem) | https://learn.microsoft.com/en-us/nuget/api/vulnerability-info |
| RustSec Advisory Database | `official` | Rust | Community-maintained upstream advisory DB; overlaps GHADB (documented GitHub import source); represented in OSV | https://github.com/RustSec/advisory-db |
| RubySec Advisory Database | `official` | Ruby | Ruby ecosystem advisories; overlaps GHADB (documented GitHub import source) | https://github.com/rubysec/ruby-advisory-db |
| FriendsOfPHP Security Advisories | `official` | PHP / Composer | PHP package advisories; overlaps GHADB (documented GitHub import source) | https://github.com/FriendsOfPHP/security-advisories |
| PyPA Advisory Database | `official` | Python / PyPI | PyPA-maintained advisory DB; overlaps GHADB (documented GitHub import source); represented in OSV | https://github.com/pypa/advisory-database |
| PyUp Safety DB | `aggregator` | Python / PyPI | Third-party curated database | https://github.com/pyupio/safety-db |
| Haskell Security Advisories | `official` | Haskell | Haskell ecosystem advisories; represented in OSV | https://github.com/haskell/security-advisories |
| Pub.dev package advisories via GitHub Advisory Database | `official` | Dart / Pub | Downstream of GHADB; pub.dev directs package advisories to GitHub Security Advisories / GitHub Advisory Database; represented in OSV (Pub ecosystem) | https://pub.dev/security |

## Vendor advisories
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Microsoft MSRC Update Guide | `official` | Microsoft products | Website, APIs | https://msrc.microsoft.com/update-guide |
| Apple Security Updates | `official` | Apple products | Website | https://support.apple.com/en-us/HT201222 |
| Adobe Security Bulletins | `official` | Adobe products | Website | https://helpx.adobe.com/security.html |
| Android Security Bulletins | `official` | Android | Website | https://source.android.com/docs/security/bulletin |
| Cisco Security Advisories | `official` | Cisco products | Website, downloadable CSAF on advisory pages | https://tools.cisco.com/security/center/publicationListing.x |
| Oracle Critical Patch Updates and Security Alerts | `official` | Oracle products | Website | https://www.oracle.com/technetwork/topics/security/alerts-086861.html |
| Chainguard Security Advisories | `official` | Chainguard images/packages | Website | https://images.chainguard.dev/security/ |

## Project and framework advisories
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Spring Security Advisories | `official` | Spring ecosystem | Security advisories hub | https://spring.io/security/ |
| Django security releases | `official` | Django | Security release archive | https://docs.djangoproject.com/en/6.0/releases/security/ |
| Drupal Security Advisories | `official` | Drupal | Security advisories hub | https://www.drupal.org/security |
| Ruby on Rails security releases | `official` | Ruby on Rails | Security release pages | https://rubyonrails.org/category/releases |
| PostgreSQL security information | `official` | PostgreSQL | Security advisories hub | https://www.postgresql.org/support/security/ |
| nginx security advisories | `official` | nginx | Advisory pages | https://nginx.org/en/security_advisories.html |
| curl security advisories | `official` | curl | CVE and advisory pages | https://curl.se/docs/security.html |
| Apache HTTP Server vulnerabilities | `official` | Apache HTTP Server | Advisory pages and JSON vulnerability feed | https://httpd.apache.org/security/vulnerabilities-httpd.json |
| Apache Tomcat security pages | `official` | Apache Tomcat | Version-specific vulnerability pages | https://tomcat.apache.org/security-9 |
| Apache Kafka CVE list | `official` | Apache Kafka | CVE list with fixed versions | https://kafka.apache.org/community/cve-list/ |
| Apache ZooKeeper security | `official` | Apache ZooKeeper | Security page with CVEs and affected versions | https://zookeeper.apache.org/security.html |
| Elastic product security advisories | `official` | Elastic products | Security announcements and advisories | https://www.elastic.co/product-security/ |

## OS and distro feeds
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Amazon Linux Security Center (ALAS) | `official` | Amazon Linux | Website | https://alas.aws.amazon.com/ |
| Red Hat Security Updates | `official` | Red Hat | Website, APIs | https://access.redhat.com/security/security-updates/ |
| Ubuntu Security Notices (USN) | `official` | Ubuntu | Website, notices | https://ubuntu.com/security/notices |
| Debian Security Tracker | `official` | Debian | Tracker website, data backend | https://security-tracker.debian.org/tracker/ |
| Arch Linux Security Tracker | `official` | Arch Linux | Tracker website | https://security.archlinux.org/ |
| Alpine SecDB | `official` | Alpine Linux | Security DB; represented in OSV | https://secdb.alpinelinux.org/ |
| Gentoo Linux Security Advisories (GLSA) | `official` | Gentoo | Advisory pages | https://security.gentoo.org/glsa/ |
| Oracle Linux Security Advisories | `official` | Oracle Linux | Advisory pages | https://linux.oracle.com/security/ |
| AlmaLinux Errata | `official` | AlmaLinux | Errata portal; represented in OSV | https://errata.almalinux.org/ |
| Rocky Linux Errata | `official` | Rocky Linux | Errata portal; represented in OSV | https://errata.build.resf.org/ |
| SUSE Security Updates | `official` | SUSE | Advisory pages | https://www.suse.com/support/update/ |
| FreeBSD Security Advisories | `official` | FreeBSD | Advisory pages | https://www.freebsd.org/security/advisories/ |
| OpenBSD Security Advisories | `official` | OpenBSD | Advisory pages | https://www.openbsd.org/security.html |

## Enrichment and prioritization
| Name | Label | Purpose | Format / Access | Link |
| --- | --- | --- | --- | --- |
| FIRST EPSS (Exploit Prediction Scoring System) | `official` | Exploit likelihood prioritization | Site + API | Site: https://www.first.org/epss, API: https://api.first.org/data/v1/epss |
| CISA Vulnrichment | `official` | CVE enrichment | Raw data repo | https://github.com/cisagov/vulnrichment |

## Machine-readable vendor advisories (CSAF/VEX)
| Name | Label | Type | Notes | Link |
| --- | --- | --- | --- | --- |
| Red Hat Security Data API | `official` | CSAF / security data API | Strong example of machine-readable vendor data | Security data: https://access.redhat.com/security/data, CSAF API: https://access.redhat.com/hydra/rest/securitydata/csaf.json |
| CISA CSAF Security Advisories | `official` | CSAF repository | Machine-readable IT/OT advisories | https://github.com/cisagov/CSAF |
| Siemens ProductCERT Advisories | `official` | CSAF-capable advisory hub | Advisory hub with machine-readable content | https://www.siemens.com/en-us/content/cert-services/ |
| Cisco Security Advisories | `official` | Advisory pages with CSAF | CSAF available on advisory pages | https://sec.cloudapps.cisco.com/security/center/content/CiscoSecurityAdvisory/ |
| SUSE CSAF / VEX | `official` | CSAF + VEX | Security advisories and CVE-indexed VEX documents | https://www.suse.com/support/security/csaf/ |
| OPC Foundation Security Advisories | `official` | CSAF/VEX-style repository | GitHub-hosted machine-readable advisories | https://github.com/OPCFoundation/OPC-SecurityAdvisories |

## Raw data repos and source mirrors
| Name | Label | Purpose | Notes | Link |
| --- | --- | --- | --- | --- |
| CVE Project cvelistV5 | `official` | Current CVE source data | Preferred upstream bulk repo | https://github.com/CVEProject/cvelistV5 |
| CVE Project cvelist | `legacy` | Historical CVE source data | Legacy repository | https://github.com/CVEProject/cvelist |

## Malware and typosquatting datasets
| Name | Label | Scope | Notes | Link |
| --- | --- | --- | --- | --- |
| OSSF Malicious Packages | `official` | Malicious open source packages | OpenSSF-maintained | https://github.com/ossf/malicious-packages |
| DataDog Malicious Software Packages Dataset | `aggregator` | Malicious packages | Third-party curated dataset | https://github.com/DataDog/malicious-software-packages-dataset |
| FOSSA Malware Impacted Packages | `aggregator` | Malware-impacted packages | Third-party curated dataset | https://github.com/fossas/fossa-malware-impacted-packages |
| Malware Packages (community list) | `aggregator` | Malware packages | Community-maintained list | https://github.com/whodinner/malware-packages |
| Typosquatting Dataset | `aggregator` | Typosquatting packages | Derived dataset | https://github.com/ecosyste-ms/typosquatting-dataset |
