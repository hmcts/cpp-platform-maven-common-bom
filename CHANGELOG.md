#Change Log
All notable changes to this project will be documented in this file, which follows the guidelines on [Keep a CHANGELOG](http://keepachangelog.com/).

This project adheres to [Semantic Versioning](http://semver.org/).

## Unreleased

## [17.102.2] - 2025-03-28
### Changed
- Include netty-bom instead of individual netty library versions.

## [17.102.1] - 2025-03-17
### Changed
- Bump version to 17.102.x for next release
- Update maven-common-bom to 17.102.0 in order to:
  - Add dependency for commons-codec 1.17.2
  
## [17.102.0] - 2025-02-26
### Changed
- Removed dependency on commons.codec as the dependency has moved to and is imported from maven-common-bom
- Commons-codec upgraded to version 1.17.2

## [17.101.0] - 2025-01-10
### Added
- Add maven-sonar-plugin to pluginManagement (through maven-parent-pom)
- Add dependency for weld-junit5 1.2.2.Final
- Add dependency for org.owasp.encoder 1.2.3
- Add junit-jupiter-engine dependency
### Changed
- Update framework-comon-bom to 17.101.1
- Update parent-pom to 17.10.12
- Update postgresql.driver.version to 42.3.2 (through framework-common-bom/maven-parent-pom)
### Security
- Update commons.io to 2.18.0 to fix **security vulnerability CVE-2024-47554**
  Detail: https://nvd.nist.gov/vuln/detail/CVE-2024-47554 and https://cwe.mitre.org/data/definitions/400.html
- Update com.jayway.json-path to version 2.9.0 to fix **security vulnerability CWE-787**
  Detail: https://cwe.mitre.org/data/definitions/787.html

## [17.21.12] - 2024-10-21
### Changed
- service parent pom enforcer rule now checks for latest major and minor versions and ignores patch version (via cpp.platform.maven.parent-pom)

## [17.21.11] - 2024-08-02
### Changed
- Provide capability to configure jgitflow develop branch name through 'jgitflow.maven.developBranchName' property (via cpp.platform.maven.parent-pom)

## [17.21.10] - 2024-07-17
### Fixed
- Downgrade azure-storage-file-datalake to 12.10.1 to stop incompatible netty jars getting included in wars

## [17.21.9] - 2024-07-16
### Added
- Add enforcer rules to verify core domain and service parent pom are on latest release version (via cpp.platform.maven.parent-pom)

## [17.21.8] - 2024-07-16
### Changed
- Updated all azure libraries to latest versions
### Added
- Added azure-storage-blob 12.27.0-beta.1 as replacement for azure-storage
- Added azure-resourcemanager 2.40.0 as replacement for azure
### Removed 
- Removed azure-storage 
- Removed azure

## [17.21.6] - 2024-06-20
- Remove duplicate jgitflow maven plugin (through cpp.platform.maven.parent-pom)

## [17.21.5] - 2024-06-20
- Add sonar-maven-plugin plugin (through cpp.platform.maven.parent-pom)

## [17.21.4] - 2024-06-17
- Add jgitflow maven plugin (through cpp.platform.maven.parent-pom)
- Add docmosis dependency to dependency management

## [17.21.3] - 2023-11-28
### Added
- Added dependency on netty version 4.1.77.Final
- Added dependency on lettuce version 5.2.1.RELEASE
- Added dependency on commons-pool2 version 2.9.0
- Added dependency on fast-classpath-scanner version 2.0.8
- Added dependency on jboss.resteasy version 4.3.0.Final

## [17.21.2] - 2023-11-27
### Added
- Added dependency on javax.el-api version 3.0.0
- Added dependency on random-beans version 3.7.0
- Added dependency on generex version 1.0.2
- Added dependency on sardine version 5.7
### Changed
- Moved io.rest-assured:xml-path to framework common-bom
- Updated framework common-bom to 17.2.1
- Updated pdfbox from 2.0.11 to 2.0.24 and removed fontbox version and referred pdfbox to fontbox
- Update azure-core version from 1.9.0 to 1.16.0
### Removed
- Removed third-party boms in favour of defining them by contexts to avoid dependency version clash

## [17.21.1] - 2023-11-09
### Changed
Remove transformation anonymise dependencies as these will be managed by contexts 

## [17.21.0] - 2023-11-09
### Changed
- Centralise all generic library dependencies and versions into maven-common-bom
- This common bom now depends on and imports the GitHub common-bom
- Update framework common-bom to 17.2.0
### Added
- Added dependency on drools-mvel required by drools
### Changed 
- Update drools-mvel to version 2.4.13.Final
### Security
- Update org.json to version 20231013 to fix **security vulnerability CVE-2023-5072**
  Detail: https://nvd.nist.gov/vuln/detail/CVE-2023-5072
- Update plexus-codehaus to version 3.0.24 to fix **security vulnerability CVE-2022-4244**
  Detail: https://nvd.nist.gov/vuln/detail/CVE-2022-4244
- Update apache-tika to version 1.28.3 to fix **security vulnerability CVE-2022-30973**
  Detail: https://nvd.nist.gov/vuln/detail/CVE-2022-30973
- Update google-guava to version 32.0.0-jre to fix **security vulnerability CVE-2023-2976**
  Detail: https://nvd.nist.gov/vuln/detail/CVE-2023-2976
- Updated drools to 7.60.0.Final to fix **security vulnerability CVE-2021-41411**
  Detail: https://nvd.nist.gov/vuln/detail/cve-2021-41411

## [17.10.3] - 2023-08-02
### Changed
- Update to junit5
- Update surefire and failsafe plugin version to 3.1.2 (through parent-pom)
- Update wiremock-test-utils version

## [17.10.2] - 2023-07-06
### Changed
Fix jacoco coverage issue (by releasing 17.10.1 parent-pom)

## [17.0.1] - 2023-06-14
### Changed
- Updated Wiremock version to 2.27.2 to match the new version in the framework wiremock war
- Updated wiremock-test-utils to the latest java 17 framework version
- Updated commons.io to version 2.7 to match version in framework
### Added
- Added junit4-dataprovider dependency
- Added jaxws-api dependency

## [17.0.0] - 2023-05-23
### Changed
- Update to Java 17
- Updated JEE to JEE 8.0
- Updated libraries to Java 17:
  - Jayway JsonPath to 2.4.0
  - OpenEjb to 8.0.6
  - DeltaSpike to 1.9.4
- Upgrade mockito, hamcrest versions
- Update hibernate-types version to 2.20.0
- Update commons.lang to version 3.4
- Update deltaspike to version 1.9.6
- Update openejb to version 8.0.13
- Update plugins.jaxb2.version to 0.15.2
- Update jackson version to 2.12.7
- Update jboss-logging version to 3.5.0.Final
- Update slf4j/log4j bridge jar from slf4j-log4j12 to slf4j-reload4j
- Update hamcrest-optional to 2.0.0
- Update update to liquibase to 4.10.0
- Update update to log4j2 version 2.17.2
- Update update slf4j to 1.7.36
- Update restassured version to 4.4.0
- Update awaitility version to 4.1.0
- Update resteasy version to 3.15.1
- Update activiti version to 5.23.0
### Added
- Added byte-buddy as a replacement for cglib
- Added commons-text dependency
- Added org.apache.activemq:activemq-ra required for deltaspike repository tests
### Removed
- Remove dependencies on log4j 1.x.x
- Removed log4j-over-slf4j as it is now replaced by slf4j-reload4j
### Security
- Updated hibernate to version 5.4.24.Final
- Updated jackson.databind to version 2.12.7.1

## [8.0.3] - 2022-02-17
### Changed
- Bumped version to 8.0.3 to stop classes with erroneous releases

## [8.0.0] - 2022-02-17
### Changed
- Bumped version to 8.0.0 to match framework 8.x.x

## [7.3.0] - 2021-12-24
### Added
- ElasticSearch client upgrade to 7.16.2

## [7.2.1] - 2020-12-04
### Added
- Added to dependency management
  - saaj-impl version 1.3.15
  - jaxp-ri version 1.4.5

## [7.2.0] - 2020-11-13
### Added
- Added to dependency management
  - azure-core version 1.9.0
  - azure-data-appconfiguration version 1.1.6
  - azure-identity version 1.1.3
  - jackson-dataformat-xml 2.8.11

## [7.1.1] - 2020-10-16
### Changed
- Added junit4-dataprovider version 2.6 to dependency management at test scope

## [7.1.0] - 2020-10-15
### Changed
- Updated various library dependencies to fix security vulnerabilities:
  - junit:                4.12    ->   4.13.1      https://github.com/advisories/GHSA-269g-pwp5-87pp
  - commons.beanutils:    1.9.2   ->   1.9.4       https://github.com/advisories/GHSA-6phf-73q6-gh87
  - commons.guava:        19.0    ->   29.0-jre    https://github.com/advisories/GHSA-mvr2-9pj6-7w5j

## [7.0.5] 2020-10-05
###Added
- Upgraded h2.version to 1.4.196 to match the version in the framework-libraries common bom

## 7.0.4 2020-07-26
###Added
-Moved properties and dependencies used by activiti embedded rest to common-bom

### 7.0.2
- Bumped up Wiremock version to 1.5.8
- Introduced Elastic search version 7.4.0 and dependencies

### 7.0.0
- Bump up version to match framework 7.0.0

## [2.2.0] - 2019-05-01
### Changed
- Reverted Deltaspike to version 1.6.1, due to issues with 1.7.0 when testing

## [2.1.3] - 2019-02-12
- Added apache pdfbox

## [2.1.3] - 2019-02-05
- Upgrade Deltaspike to 1.7.0

## [2.1.2] - 2018-05-18
- Upgrade Jackson to 2.8.11 to fix Jackson security issues

## [2.1.0] - 2017-12-11
### Changed
- Removed File Service, Test Utils and Wiremock Test Utils dependencies.  These are now in the Service Parent POM and the Library Parent POM.

## [2.0.29] - 2017-10-26
### Changed
- Updated drools version to 6.5.0.Final

## [1.0.1] - 2017-06-23
### Changed
- Add hamcrest optional dependency
