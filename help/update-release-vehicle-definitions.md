---
title: Update Release Vehicle Definitions
description: This article details the various types of AEM releases, including full releases, feature packs, and services packs.
contentOwner: AK
---

# AEM update release vehicle definitions {#update-release-vehicle-definitions}

This document includes details about the various types of [!DNL Adobe Experience Manager] (AEM) releases, including full releases, feature packs, and services packs that [!DNL Adobe] delivers to its customers.

>[!NOTE]
>
>For release schedule of AEM update releases, refer to [AEM update releases roadmap](update-releases-roadmap.md)

## Full Release {#full-release}

| Items | Description|
|-------|------|
| Definition  | <ul> <li> Scheduled release </li> <li> Supports upgrade paths for specific versions, which is defined in the release notes </li> </ul> |
| Naming | <ul> <li> Version numbers for major releases increase based on the formula X+1.Y.Z. </li> <li> Version numbers for minor releases increase based on the formula X.Y+1.Z </li> </ul> Where X is the primary version number, Y is the secondary version number, and Z the patch number. |
| Inclusions  | <ul> <li> New features </li> <li>  Improvements </li> <li>  Bug fixes </li> </ul> |
| Documentation | <ul> <li> Release notes are available on the documentation portal </li> <li> Documentation on features, improvements, and bug fixes are available on the documentation portal </li> </ul> |
| Cadence  | Yearly |
| Availability and Installation | <ul> <li> Delivered as a standalone product installer </li> <li>  Available from Licensing Website and Managed Services </li> <li> Licensing Website May require content repository migration </li> </ul> |
| Level of Testing | Fully validated by QA |

## Service Pack {#service-pack}

|Item | Description |
|-----|-----|
| Definition  | <ul> <li> Scheduled release </li> <li> Currently, cannot be rolled back </li> </ul>|
| Naming | <ul> <li> Patch release number is a single digit number </li> <li> After installation, will increase the installed release number patch digit, based on the formula X.Y.Z.SPx </li> </ul> Where X is the primary version number, Y is the secondary version number, and Z the patch number. x is the service pack number. |
| Inclusions | <ul> <li> New features</li> <li>  Improvements </li> <li> Bug fixes </li> <li> Common Interest feature packs (if any) </li> </ul> |
| Documentation |<ul> <li> Release notes available on the documentation portal </li> <li> Documentation on features, improvements, bug fixes on the documentation portal </li> </ul> |
| Cadence   | Quarterly |
| Availability and Installation | <ul> <li> Delivered as a package </li> <li> Available on Software Distribution</li> <li>  Requires existing functional installation </li> </ul> |
| Level of Testing  | <ul> <li> All fixes QA validated </li> <li>  Overall package sanity with automation runs </li> </ul>|

## Cumulative Fix Pack  {#cumulative-fix-pack-aem}

|Item | Description |
|-----|-----|
| Definition | <ul> <li> Single delivery model of releasing fixes </li> <li> Aggregator content package containing content package of individual components </li> <li>  CFPs are rollover of hot fixes and no improvements are part of it.  </li> </ul> |
| Naming | X.Y.Z.CFPx  <br> Where X is the primary version number, Y is the secondary version number, and Z the patch number. x is the cumulative service pack number. |
| Inclusions | CFP is cumulative fix pack containing fixes of all components through specified dates. For example, if a customer applies CFP3, then CFP3 = CFP1 + CFP2. |
| Documentation | Release notes available on the documentation portal |
| Cadence  | Quarterly  |
| Availability and Installation | <ul> <li> Delivered as a package </li> <li>  Available on Software Distribution </li> <li>  Dependent on the latest service pack released </li> <li>  CFP is self-dependent. Customers need not worry about finding/resolving dependencies. CFP should be installed on latest released Service Pack. </li> <li>  CFP can be installed as a single package, which improves customer experience.  </li> </ul> |
| Level of Testing  | QA validated at Integration level and regression testing |

## Overlay {#overlay}

<table>
 <tbody>
  <tr>
   <td><strong>Definition</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td><strong>Naming</strong></td>
   <td>overlay-&lt;ticket ID&gt;</td>
  </tr>
  <tr>
   <td><strong>Inclusions</strong></td>
   <td>Bug fix for a JS or JSP file</td>
  </tr>
  <tr>
   <td><strong>Documentation</strong></td>
   <td>None</td>
  </tr>
  <tr>
   <td><strong>Cadence</strong></td>
   <td>As necessary</td>
  </tr>
  <tr>
   <td><strong>Availability and Installation</strong></td>
   <td>
    <ul>
     <li>Delivered as package by AEM Customer Care</li>
     <li>Not necessarily included in service packs or full releases</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Level of Testing</strong></td>
   <td>Validated by Customer Care</td>
  </tr>
 </tbody>
</table>

## Feature Pack {#feature-pack}

<table>
 <tbody>
  <tr>
   <td><strong>Definition</strong></td>
   <td>
    <ul>
     <li>Feature Packs are add-on functionalities and are delivered via Service Packs. If an AEM version has released its last service pack, Adobe will not deliver any feature pack for it in future.</li>
     <li>FPs contain product enhancements, scheduled for a subsequent product release, but delivered early based on the decision of [!DNL Adobe's] Product Management.</li>
     <li>Features are always merged with the next major release and then ported to the AEM version required by the customer</li>
     <li>Common Interest and GA feature packs are merged into the next service pack</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Naming</strong></td>
   <td>cq-&lt;Release Version&gt;-featurepack-&lt;feature pack ID&gt;-&lt;feature pack version&gt;</td>
  </tr>
  <tr>
   <td><strong>Inclusions</strong></td>
   <td>
    <ul>
     <li>New features</li>
     <li>Improvements</li>
     <li>Bug fixes (incremental product updates)</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Documentation</strong></td>
   <td>Documentation is available on helpx.adobe.com.</td>
  </tr>
  <tr>
   <td><strong>Cadence</strong></td>
   <td>Varies with Product area</td>
  </tr>
  <tr>
   <td><strong>Availability and Installation</strong></td>
   <td>
    <ul>
     <li>Delivered via Service Packs</li>
     <li>Available on Software Distribution. Customers accept [!DNL Adobe's] Terms and Conditions through Software Distribution.</li>
    </ul> </td>
  </tr>
  <tr>
   <td><strong>Level of Testing</strong></td>
   <td>General Availability feature packs are QA validated</td>
  </tr>
 </tbody>
</table>

* 1: OAK fixes are not delivered as individual hot fixes. However, they are included in the subsequent Cumulative Oak hot fix. If necessary, a diagnostic build on top of the latest COFP can be made available. The precondition is that the customer has the latest COFP running. Diagnostic builds only provide the same level quality assurance as a hot fix. Therefore, they don't provide the same level of quality assurance as a cumulative fix pack, service pack, or product release. The final fix is delivered with the next CFP.
