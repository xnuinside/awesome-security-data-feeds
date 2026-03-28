# awesome-security-data-feeds
Curated list of machine-readable security feeds, vulnerability databases, advisory sources, and raw security data for automation, aggregation, and vulnerability management.

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

## National and Government Vulnerability Databases
| Name | Label | Agency / Country | Coverage | Direct feed / API | Portal |
| --- | --- | --- | --- | --- | --- |
| NVD (NIST National Vulnerability Database) | `official` | NIST / United States | CVE/NVD | API: https://services.nvd.nist.gov/rest/json/cves/2.0, feeds: https://nvd.nist.gov/vuln/data-feeds | https://nvd.nist.gov/ |
| EUVD (European Vulnerability Database) | `official` | ENISA / European Union | Aggregated vulnerability records, exploited and critical subsets | API docs: https://euvd.enisa.europa.eu/apidoc, latest: https://euvdservices.enisa.europa.eu/api/lastvulnerabilities, exploited: https://euvdservices.enisa.europa.eu/api/exploitedvulnerabilities | https://euvd.enisa.europa.eu/ |
| JVN iPedia / MyJVN | `official` | IPA + JPCERT/CC / Japan | JVN records, domestic vendor advisories, and vulnerability data feeds | feed hub: https://jvndb.jvn.jp/en/feed/, API docs: https://jvndb.jvn.jp/en/apis/index.html, MyJVN API: https://jvndb.jvn.jp/en/apis/myjvn/ | https://jvndb.jvn.jp/en/ |
| BSI CERT-Bund CSAF feeds | `official` | BSI / Germany | Public advisories, WID and CVD feeds | provider metadata: https://wid.cert-bund.de/.well-known/csaf/provider-metadata.json, public BSI feed: https://wid.cert-bund.de/.well-known/csaf/white/bsi-white.json, public WID feed: https://wid.cert-bund.de/.well-known/csaf/white/bsi-wid-white.json, public CVD feed: https://wid.cert-bund.de/.well-known/csaf/white/bsi-cvd-white.json | https://wid.cert-bund.de/ |

## General vulnerability databases
| Name | Label | Coverage | Format / Access | Link |
| --- | --- | --- | --- | --- |
| OSV (Open Source Vulnerabilities) | `aggregator` | Open source ecosystems | API, OSV JSON, HTML | https://osv.dev/ |
| GitHub Advisory Database | `aggregator` | Open source ecosystems | HTML UI, Git repo (JSON/YAML data) | UI: https://github.com/advisories, data: https://github.com/github/advisory-database |
| GitLab Advisory Database | `aggregator` | Open source ecosystems | HTML, advisory pages, source repo-backed data | https://advisories.gitlab.com/ |
| Packagist Security Advisory Feed | `aggregator` | PHP / Composer | API/JSON, HTML; downstream of GHADB via GitHub Security Advisories and also aggregates FriendsOfPHP; represented in OSV (Packagist ecosystem) | https://packagist.org/security-advisories/ |
| Sonatype OSS Index | `aggregator` | Open source ecosystems | API, HTML | https://ossindex.sonatype.org/ |
| CISA Known Exploited Vulnerabilities (KEV) | `official` | Known exploited CVEs | HTML catalog, raw data repo (JSON/CSV) | Catalog: https://www.cisa.gov/known-exploited-vulnerabilities-catalog, data: https://github.com/cisagov/kev-data |

## Language ecosystems
| Name | Label | Ecosystem | Notes | Link |
| --- | --- | --- | --- | --- |
| Go Vulnerability Database | `official` | Go | HTML, API/JSON; primary Go vuln feed; overlaps GHADB (documented GitHub import source); represented in OSV | https://vuln.go.dev/ |
| npm audit advisory endpoints | `official` | JavaScript / npm | API/JSON via registry audit endpoints (`Bulk Advisory` and `Quick Audit`) used by `npm audit` | https://docs.npmjs.com/cli/v8/commands/npm-audit/ |
| NuGet Vulnerability Info API | `official` | .NET / NuGet | API/JSON vulnerability files; Microsoft docs use GitHub Advisories Database as an example upstream, but nuget.org backing source not verified here; represented in OSV (NuGet ecosystem) | https://learn.microsoft.com/en-us/nuget/api/vulnerability-info |
| RustSec Advisory Database | `official` | Rust | Git repo (TOML advisories); overlaps GHADB (documented GitHub import source); represented in OSV | https://github.com/RustSec/advisory-db |
| RubySec Advisory Database | `official` | Ruby | Git repo (YAML advisories); overlaps GHADB (documented GitHub import source) | https://github.com/rubysec/ruby-advisory-db |
| FriendsOfPHP Security Advisories | `official` | PHP / Composer | Git repo (YAML advisories); overlaps GHADB (documented GitHub import source) | https://github.com/FriendsOfPHP/security-advisories |
| PyPA Advisory Database | `official` | Python / PyPI | Git repo (OSV JSON advisories); overlaps GHADB (documented GitHub import source); represented in OSV | https://github.com/pypa/advisory-database |
| PyUp Safety DB | `aggregator` | Python / PyPI | Git repo (JSON/insecure_full.json) | https://github.com/pyupio/safety-db |
| Haskell Security Advisories | `official` | Haskell | Git repo (OSV-style advisories); represented in OSV | https://github.com/haskell/security-advisories |

## Vendor advisories
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Microsoft MSRC Update Guide | `official` | Microsoft products | HTML, API | https://msrc.microsoft.com/update-guide |
| Apple Security Updates | `official` | Apple products | HTML | https://support.apple.com/en-us/HT201222 |
| Adobe Security Bulletins | `official` | Adobe products | HTML | https://helpx.adobe.com/security.html |
| Android Security Bulletins | `official` | Android | HTML | https://source.android.com/docs/security/bulletin |
| Atlassian Security Advisories | `official` | Atlassian products | HTML advisory archive | https://www.atlassian.com/trust/security/advisories |
| Cisco Security Advisories | `official` | Cisco products | HTML, downloadable CSAF | https://tools.cisco.com/security/center/publicationListing.x |
| HashiCorp security updates | `official` | HashiCorp products | HTML, RSS/email subscriptions | https://discuss.hashicorp.com/c/security/52 |
| Kaspersky List of Advisories | `official` | Kaspersky products | HTML advisory archive | https://support.kaspersky.com/vulnerability/list-of-advisories |
| Oracle Critical Patch Updates and Security Alerts | `official` | Oracle products | HTML | https://www.oracle.com/technetwork/topics/security/alerts-086861.html |
| Chainguard Security Advisories | `official` | Chainguard images/packages | HTML | https://images.chainguard.dev/security/ |

## Project and framework advisories
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Spring Security Advisories | `official` | Spring ecosystem | HTML advisory hub | https://spring.io/security/ |
| Django security releases | `official` | Django | HTML archive | https://docs.djangoproject.com/en/6.0/releases/security/ |
| Drupal Security Advisories | `official` | Drupal | HTML advisory hub | https://www.drupal.org/security |
| WordPress security releases | `official` | WordPress | HTML security archive focused on vulnerability and security-release announcements | https://wordpress.org/news/category/security/ |
| Patchstack vulnerability database | `aggregator` | WordPress ecosystem | HTML database/search; large vulnerability database for WordPress plugins and themes | https://patchstack.com/database |
| Eclipse Known Vulnerabilities | `official` | Eclipse Foundation projects | Dedicated vulnerability/advisory page for Eclipse projects and Eclipse-operated sites | https://www.eclipse.org/security/known/ |
| OpenJDK Vulnerability Advisories | `official` | OpenJDK / Java | HTML advisory archive with affected/fixed release tables, CVE references, and risk matrices | https://openjdk.org/groups/vulnerability/advisories/ |
| OpenSSH security page | `official` | OpenSSH | HTML security notices archive with vulnerability-specific entries and release references | https://www.openssh.org/security.html |
| NixOS security advisories | `official` | Nix / NixOS ecosystem | Dedicated security advisory category with vulnerability-specific posts, affected configurations, fixes, and upgrade guidance | https://discourse.nixos.org/c/announcements/security/56 |
| PostgreSQL security information | `official` | PostgreSQL | HTML advisories hub | https://www.postgresql.org/support/security/ |
| nginx security advisories | `official` | nginx | HTML advisory pages | https://nginx.org/en/security_advisories.html |
| curl security advisories | `official` | curl | HTML advisory pages | https://curl.se/docs/security.html |
| OpenSSL security advisory list (JSON) | `official` | OpenSSL | JSON advisory list | https://openssl-library.org/news/secjson/ |
| Jenkins security advisories | `official` | Jenkins | HTML archive, RSS | https://www.jenkins.io/security/advisories/ |
| Grafana security advisories | `official` | Grafana ecosystem | HTML searchable advisory database | https://grafana.com/security/security-advisories/ |
| Apache HTTP Server vulnerabilities | `official` | Apache HTTP Server | JSON feed, HTML advisory pages | https://httpd.apache.org/security/vulnerabilities-httpd.json |
| Apache Tomcat security pages | `official` | Apache Tomcat | HTML version-specific pages | https://tomcat.apache.org/security-9 |
| Apache Kafka CVE list | `official` | Apache Kafka | HTML CVE list | https://kafka.apache.org/community/cve-list/ |
| Apache ZooKeeper security | `official` | Apache ZooKeeper | HTML advisory page | https://zookeeper.apache.org/security.html |
| Elastic product security advisories | `official` | Elastic products | HTML announcements and advisories | https://www.elastic.co/product-security/ |
| Linux kernel CVE announcements | `official` | Linux kernel | Mailing-list archive dedicated to assigned kernel CVEs; per-entry advisories include descriptions, commits, and affected/fixed versions | https://lore.kernel.org/linux-cve-announce/ |

## OS and distro feeds
| Name | Label | Scope | Format / Access | Link |
| --- | --- | --- | --- | --- |
| Amazon Linux Security Center (ALAS) | `official` | Amazon Linux | HTML | https://alas.aws.amazon.com/ |
| ALT Linux errata | `official` | ALT Linux | HTML errata pages with package/version metadata and linked `BDU` + `CVE` entries per bulletin | https://packages.altlinux.org/en/errata |
| Red Hat Security Updates | `official` | Red Hat | HTML, API | https://access.redhat.com/security/security-updates/ |
| Ubuntu OVAL data | `official` | Ubuntu | OVAL XML / bz2 streams for supported Ubuntu releases and cloud images | https://ubuntu.com/security/oval |
| Ubuntu Security Notices (USN) | `official` | Ubuntu | HTML notices, RSS/OVAL available | https://ubuntu.com/security/notices |
| Debian Security Tracker | `official` | Debian | HTML tracker, backend data files | https://security-tracker.debian.org/tracker/ |
| Arch Linux Security Tracker | `official` | Arch Linux | HTML tracker | https://security.archlinux.org/ |
| Alpine SecDB | `official` | Alpine Linux | SecDB data, HTML; represented in OSV | https://secdb.alpinelinux.org/ |
| Fedora Bodhi security updates | `official` | Fedora | HTML, updateinfo metadata/API-backed system | https://bodhi.fedoraproject.org/ |
| openSUSE updateinfo metadata | `official` | openSUSE | Repository metadata with signed `updateinfo.xml` / `updateinfo.xml.zst` in official update repos; useful for package-level advisory parsing | https://download.opensuse.org/download/update/leap/15.6/oss/repodata/ |
| AlmaLinux OVAL streams | `official` | AlmaLinux | Public OVAL XML / bz2 streams for supported AlmaLinux releases | https://security.almalinux.org/oval/ |
| Mageia Advisories (MGASA) | `official` | Mageia | Advisory pages plus public raw `.adv` source files in official Mageia SVN; structured fields include `type`, `CVE`, package lists, references, and advisory ID | https://advisories.mageia.org/ |
| Wolfi advisory data | `official` | Wolfi | Git repo (advisory YAML/data) | https://github.com/wolfi-dev/advisories |
| Gentoo Linux Security Advisories (GLSA) | `official` | Gentoo | XML advisories in the Gentoo repository (`metadata/glsa`) plus RSS/HTML publication | https://security.gentoo.org/glsa/ |
| SUSE OVAL data | `official` | SUSE Linux Enterprise / SUSE products | OVAL XML data sets in patch and vulnerability styles, including compressed variants and direct file index | https://www.suse.com/support/security/oval/ |
| Oracle Linux security data | `official` | Oracle Linux | Consolidated and per-product OVAL definitions plus repository `updateinfo.xml.gz` metadata in official yum repos | https://linux.oracle.com/security/ |
| Oracle Linux Security Advisories | `official` | Oracle Linux | HTML advisory pages | https://linux.oracle.com/security/ |
| AlmaLinux Errata | `official` | AlmaLinux | HTML errata portal; represented in OSV | https://errata.almalinux.org/ |
| Rocky Linux Errata | `official` | Rocky Linux | Errata portal with documented API/RSS and repository `updateinfo.xml` metadata for package-level advisories | https://errata.build.resf.org/ |
| NetBSD pkgsrc `pkg-vulnerabilities` | `official` | pkgsrc / NetBSD packages | Flat file, gzip/bzip2 variants, GPG-signed workflow for package vulnerability auditing | https://cdn.netbsd.org/pub/NetBSD/packages/vulns/pkg-vulnerabilities |
| OpenWrt Security Advisories | `official` | OpenWrt | Security-specific HTML advisory archive with per-advisory pages listing CVEs, affected versions, mitigations, and fix commits | https://openwrt.org/advisory/start |
| Astra Linux security bulletins | `official` | Astra Linux | Security-bulletin archive for operational updates; bulletin pages describe affected components, update packages, and linked update media/repos | https://wiki.astralinux.ru/category/security-bulletins |
| РЕД ОС security bulletins | `official` | РЕД ОС | HTML bulletins with CVE, package versions, fixes, and CVSS | https://redos.red-soft.ru/support/secure/uyazvimosti-red-os-8-0/ |
| VMware Photon OS security advisories | `official` | Photon OS | HTML advisory pages | https://vmware.github.io/photon/docs-v5/security-advisories/ |
| SUSE Security Updates | `official` | SUSE | HTML advisory pages | https://www.suse.com/support/update/ |
| FreeBSD VuXML | `official` | FreeBSD and FreeBSD Ports Collection | XML vulnerability database with plain/compressed copies (`vuln.xml`, xz, zstd) and rendered indexes | https://vuxml.freebsd.org/freebsd/ |
| FreeBSD Security Advisories | `official` | FreeBSD | HTML advisory pages | https://www.freebsd.org/security/advisories/ |
| OpenBSD Security Advisories | `official` | OpenBSD | HTML advisory pages | https://www.openbsd.org/security.html |

## Enrichment and prioritization
| Name | Label | Purpose | Format / Access | Link |
| --- | --- | --- | --- | --- |
| FIRST EPSS (Exploit Prediction Scoring System) | `official` | Exploit likelihood prioritization | HTML, API/CSV | Site: https://www.first.org/epss, API: https://api.first.org/data/v1/epss |
| CISA Vulnrichment | `official` | CVE enrichment | Git repo (JSON data) | https://github.com/cisagov/vulnrichment |

## Machine-readable vendor advisories (CSAF/VEX)
| Name | Label | Type | Notes | Link |
| --- | --- | --- | --- | --- |
| Red Hat Security Data API | `official` | CSAF / security data API | JSON, CSAF API; strong example of machine-readable vendor data | Security data: https://access.redhat.com/security/data, CSAF API: https://access.redhat.com/hydra/rest/securitydata/csaf.json |
| CISA CSAF Security Advisories | `official` | CSAF repository | Git repo, CSAF JSON | https://github.com/cisagov/CSAF |
| Siemens ProductCERT Advisories | `official` | CSAF-capable advisory hub | HTML advisory hub, machine-readable content available | https://www.siemens.com/en-us/content/cert-services/ |
| Cisco Security Advisories | `official` | Advisory pages with CSAF | HTML, CSAF downloads | https://sec.cloudapps.cisco.com/security/center/content/CiscoSecurityAdvisory/ |
| Kaspersky ICS CERT Advisories | `official` | ICS / CERT advisories | HTML advisory archive for industrial control systems and products | https://ics-cert.kaspersky.com/advisories/ |
| SUSE CSAF / VEX | `official` | CSAF + VEX | CSAF/VEX documents | https://www.suse.com/support/security/csaf/ |
| OPC Foundation Security Advisories | `official` | CSAF/VEX-style repository | Git repo, machine-readable advisories | https://github.com/OPCFoundation/OPC-SecurityAdvisories |

## Raw data repos and source mirrors
| Name | Label | Purpose | Notes | Link |
| --- | --- | --- | --- | --- |
| CVE Project cvelistV5 | `official` | Current CVE source data | Git repo (CVE JSON), preferred upstream bulk repo | https://github.com/CVEProject/cvelistV5 |
| CVE Project cvelist | `legacy` | Historical CVE source data | Git repo, legacy repository | https://github.com/CVEProject/cvelist |

## Malware and typosquatting datasets
| Name | Label | Scope | Notes | Link |
| --- | --- | --- | --- | --- |
| OSSF Malicious Packages | `official` | Malicious open source packages | Git repo data | https://github.com/ossf/malicious-packages |
| DataDog Malicious Software Packages Dataset | `aggregator` | Malicious packages | Git repo curated dataset | https://github.com/DataDog/malicious-software-packages-dataset |
| FOSSA Malware Impacted Packages | `aggregator` | Malware-impacted packages | Git repo curated dataset | https://github.com/fossas/fossa-malware-impacted-packages |
| Malware Packages (community list) | `aggregator` | Malware packages | Git repo community list | https://github.com/whodinner/malware-packages |
| Typosquatting Dataset | `aggregator` | Typosquatting packages | Git repo derived dataset | https://github.com/ecosyste-ms/typosquatting-dataset |

## Schemas and standards
| Name | Purpose | Link |
| --- | --- | --- |
| OSSF OSV Schema | Advisory/vulnerability exchange schema | https://github.com/ossf/osv-schema |

## Tools and secondary indexes
| Name | Type | Notes | Link |
| --- | --- | --- | --- |
| cve-search | Tool | Consumer/index over vulnerability data sources | https://github.com/cve-search/cve-search |
| Docker Scout advisory database | Secondary index / aggregator | Documents upstream advisory sources used for container image analysis | https://docs.docker.com/scout/deep-dive/advisory-db-sources/ |
| Awesome CVE PoC | Secondary index | Useful discovery list, not a primary feed | https://github.com/qazbnm456/awesome-cve-poc |
| Awesome Security | Secondary index | Broad security list, not focused on feeds | https://github.com/sbilly/awesome-security |
