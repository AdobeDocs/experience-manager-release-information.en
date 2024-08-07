---
title: Update Release Vehicle Definitions
description: This article details the various types of [!DNL Experience Manager] releases, including full releases, feature packs, and service packs.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
---
# [!DNL Experience Manager] update release vehicle definitions {#update-release-vehicle-definitions}

This document includes details about the various types of [!DNL Adobe Experience Manager] releases, including full releases, feature packs, and services packs that [!DNL Adobe] delivers to its customers.

>[!NOTE]
>
>For release schedule of [!DNL Experience Manager] update releases, refer to [[!DNL Experience Manager] update releases roadmap](update-releases-roadmap.md)

## Full Release {#full-release}

| Items | Description|
|-------|------|
| Definition  | <ul> <li> Scheduled release </li> <li> Supports upgrade paths for specific versions that are defined in the release notes </li> </ul> |
| Naming | <ul> <li> Version numbers for major releases increase based on the formula X+1.Y.Z. </li> <li> Version numbers for minor releases increase based on the formula X.Y+1.Z </li> </ul> Where X is the primary version number, Y is the secondary version number, and Z the patch number. |
| Inclusions  | <ul> <li> New features </li> <li>  Improvements </li> <li>  Bug fixes </li> </ul> |
| Documentation | <ul> <li> Release notes are available on the documentation portal </li> <li> Documentation on features, improvements, and bug fixes are available on the documentation portal </li> </ul> |
| Cadence  | Yearly |
| Availability and Installation | <ul> <li> Delivered as a standalone product installer </li> <li>  Available from Licensing Website and Managed Services </li> <li> Licensing Website May require content repository migration </li> </ul> |
| Level of Testing | Fully validated by QA |

## Service Pack {#service-pack}

|Item | Description |
|-----|-----|
| Definition  | <ul> <li> Scheduled release </li> <li> Currently, it cannot be rolled back </li> </ul>|
| Naming | <ul> <li> Patch release number is a single digit number </li> <li> After installation, will increase the installed release number patch digit, based on the formula X.Y.Z.SPx </li> </ul> Where X is the primary version number, Y is the secondary version number, and Z the patch number. x is the service pack number. |
| Inclusions | <ul> <li> New features</li> <li>  Improvements </li> <li> Bug fixes </li> <li> Common Interest feature packs (if any) </li> </ul> |
| Documentation |<ul> <li> Release notes are available on the documentation portal </li> <li> Documentation on features, improvements, bug fixes on the documentation portal </li> </ul> |
| Cadence   | Quarterly |
| Availability and Installation | <ul> <li> Delivered as a package </li> <li> Available on Software Distribution</li> <li>  Requires existing functional installation </li> </ul> |
| Level of Testing  | <ul> <li> All fixes QA validated </li> <li>  Overall package sanity with automation runs </li> </ul>|

## Cumulative Fix Pack {#cumulative-fix-pack-aem}

|Item | Description |
|-----|-----|
| Definition | <ul> <li> Single delivery model of releasing fixes </li> <li> Aggregator content package containing content package of individual components </li> <li>  CFPs are rollover of hot fixes and no improvements are part of it.  </li> </ul> |
| Naming | X.Y.Z.CFPx  <br> Where X is the primary version number, Y is the secondary version number, and Z the patch number. x is the cumulative service pack number. |
| Inclusions | CFP is a cumulative fix pack containing fixes of all components through specified dates. For example, if a customer applies CFP3, then CFP3 = CFP1 + CFP2. |
| Documentation | Release notes are available on the documentation portal |
| Cadence  | Quarterly  |
| Availability and Installation | <ul> <li> Delivered as a package </li> <li>  Available on Software Distribution </li> <li>  Dependent on the latest service pack released </li> <li>  CFP is self-dependent. Customers do not need to worry about finding/resolving dependencies. CFP should be installed on the latest released service pack. </li> <li>  CFP can be installed as a single package, which improves customer experience.  </li> </ul> |
| Level of Testing  | QA validated at Integration level and regression testing |

## Overlay {#overlay}

| Item   | Details |
|-------|--------|
| Naming  | overlay-&lt;ticket ID&gt; |
| Inclusions | Bug fix for a JS or JSP file |
| Documentation  | None |
| Cadence   | As necessary  |
| Availability and Installation | <ul> <li> Delivered as package by [!DNL Experience Manager] Customer Care  </li> <li> Not necessarily included in service packs or full releases </li> </ul> |
| Level of Testing  | Validated by Customer Care |

## Feature Pack {#feature-pack}

|Items | Details |
|--------|-----|
| Definition | <ul> <li>Feature Packs are add-on functionalities and are delivered through a service packs. If an [!DNL Experience Manager] version has released its last service pack, Adobe will not deliver any feature pack for it in the future. </li> <li> FPs contain product enhancements, scheduled for a subsequent product release, but delivered early based on the decision of [!DNL Adobe's] Product Management.</li> <li>  Features are always merged with the next major release. They are then ported to the [!DNL Experience Manager] version required by the customer </li> <li>  Common Interest and GA feature packs are merged into the next service pack  </li> </ul> |
| Naming | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusions | <ul> <li> New features </li> <li> Improvements </li> <li> Bug fixes (incremental product updates) </li> </ul>|
| Documentation | Documentation is available on adobe.com. |
| Cadence | Varies with Product area |
| Availability and Installation | <ul> <li>Delivered via Service Packs </li> <li> Available on Software Distribution. Customers accept [!DNL Adobe's] Terms and Conditions through Software Distribution. </li> </ul> |
| Level of Testing | General Availability feature packs are QA validated. |

* 1: Oak fixes are not delivered as individual hot fixes. However, they are included in the subsequent Cumulative Oak hot fix. If necessary, a diagnostic built on top of the latest COFP can be made available. The precondition is that the customer has the latest COFP running. Diagnostic builds only provide the same level of quality assurance as a hot fix. Therefore, they don't provide as much quality assurance as a cumulative fix pack, service pack, or product release. The final fix is delivered with the next CFP.
