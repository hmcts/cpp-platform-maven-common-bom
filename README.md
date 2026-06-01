# cpp-platform-maven-common-bom

`uk.gov.moj.cpp.common:common-bom`

The CPP platform dependency bill of materials. It extends the framework-tier `maven-common-bom` with additional library versions specific to the platform and bounded-context tier, covering domain-specific frameworks (Activiti), additional Apache Commons modules, document processing, SOAP/CXF, and CPP-specific library versions.

## Position in the hierarchy

```
cpp-platform-maven-parent-pom
└── cpp-platform-maven-common-bom  ← this project
```

This BOM is imported by `cpp-platform-maven-service-parent-pom` and `cpp-platform-libraries`, making all versions available to every `cpp-context-*` service.

## Maven coordinates

| Property | Value |
|---|---|
| `groupId` | `uk.gov.moj.cpp.common` |
| `artifactId` | `common-bom` |
| Parent | `uk.gov.moj.cpp.common:parent-pom` |

## What this BOM adds

This BOM imports `maven-common-bom` (`uk.gov.justice:maven-common-bom`) so that all framework-tier versions are also available here. It then adds platform-specific versions:

**Workflow**
- Activiti 5.22.0

**Messaging**
- Apache ActiveMQ Classic client 5.16.8, RA 5.17.2 (legacy broker support)

**Additional Apache Commons**
- commons-dbutils 1.7, commons-pool2 2.13.0, commons-compress 1.26.0, commons-csv 1.4, commons-fileupload 1.6.0, commons-net 3.9.0, commons-text 1.10.0

**Web services**
- Apache CXF 3.4.4

**Document processing**
- Apache PDFBox 2.0.36
- Apache POI (OOXML) 5.4.1 — Excel/Word document generation

**MOJ interface JARs** — versioned dependencies on shared MOJ service API JARs (assignment, usersgroups, progression, hearing, SJP, referencedata). The `enforce-moj-latest-interfaces` enforcer rule requires these to be at their latest released versions.

## Usage

Import in your project's `<dependencyManagement>`:

```xml
<dependency>
    <groupId>uk.gov.moj.cpp.common</groupId>
    <artifactId>common-bom</artifactId>
    <version>${cpp.common-bom.version}</version>
    <type>pom</type>
    <scope>import</scope>
</dependency>
```

All projects that inherit from `cpp-platform-maven-service-parent-pom` get this import automatically.
