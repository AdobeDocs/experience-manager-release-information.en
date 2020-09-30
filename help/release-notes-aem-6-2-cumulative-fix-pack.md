---
title: AEM 6.2 Cumulative Fix Pack
description: null
seo-description: null
uuid: 767319ae-48be-417e-a777-6a5d7e4d03d2
discoiquuid: 334fd54d-2d62-4fb6-a1b1-6401fc6310f6
---

# AEM 6.2 Cumulative Fix Pack Release Notes{#release-notes-aem-cumulative-fix-pack}

## Release information {#release-information}

| **Product** |Adobe Experience Manager |
|---|---|
| **Version** |6.2 |
| **Release** | [Cumulative Fix Pack 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **Prerequisite** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **General availability** |06th June, 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe introduced a single-delivery model for releasing fixes. Instead of releasing hot fixes for individual issues, Adobe now releases a Cumulative Fix Pack (CFP) every month (subject to passing quality checks). A CFP is an aggregated content package for multiple fixes. CFPs primarily include bug fixes but might also include Feature Packs. They have the following advantages over individual hotfix releases:

* Cumulative in nature (for example, a CFP contains fixes delivered through previous CFPs)
* Increased quality assurance
* Simplified installation (User installs a CFP as a single package that has no dependencies, except for the latest service pack)

For more information on CFP and other types of releases, see [Maintenance Release Vehicle](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html).

## About the release {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20 is the last Cumulative Fix Pack for AEM 6.2 and is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

>[!CAUTION]
>
>Applying CFP without validating compatibility between installed feature packs may result in system failure or loss of custom configurations, which could require restoration from backup to resolve.

>[!NOTE]
>
>* A new Sling `discovery-  api` bundle  Johnzon  1.0.0 is included with AEM Cumulative Fix Pack 6.2 SP1-CFP10. In addition, a service user sling-discovery is added with  Read  and Write privileges for the node */var/discovery* in the CRX repository.
>
>* Email bundle of apache commons **org.apache.commons/commons-email/1.5** has been added replacing **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Adobe recommends  to deploy  CFP via the install folder for customers having a large number of users on AEM instance.
>

## Issues included {#issues-included}

This section lists all issues and hotfixes included in the current CFP.

In addition, this CFP includes hotfixes delivered in [previous cumulative fix packs](#previous).

### Integration {#integration}

* Backporting multiple Campaign Taregting personalization improvements. NPR-29163: Hotfix for CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler goes into an infinite loop and causes updates to nodes on publish instances. NPR-28561: Hotfix for CQ-4263096

### DAM - General {#dam-general}

* Unable to display/hide the replication button for non-admin users at specific dam folders. NPR-29026: Hotfix for CQ-4265361

### Vulnerability {#vulnerability}

* CSRF protection framework is not working with AEM foundation forms. NPR-28612: Hotfix for GRANITE-22231

### Forms {#forms}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package}

>[!NOTE]
>
>For AEM Forms customers, it is essential to install AEM Forms add-on package after installing any AEM Service Pack, Cumulative Fix Pack, or Feature Pack.

>[!NOTE]
>
>AEM Forms add-on packages help align forms functionality with AEM Service Packs and Cumulative Fix Packs. Therefore, it is imperative to install AEM forms add-on package after installing any AEM Service Pack, Cumulative Fix Pack, or Feature Pack.

#### Adaptive Forms {#adaptive-forms}

* Usability issues with scribble component for iOS 12.1 devices. NPR- 29082: Hotfix for CQ-4261765

#### Forms - Document Security {#forms-document-security}

* Verifying all the signatures in a PDF using PDF Advanced Electronic Signatures (PAdES) throws InvalidOperationException. NPR-27848: Hotfix for CQ-4244837

#### Forms - Correspondence {#forms-correspondence}

* On previewing the letter as PDF, text field placed at the master page does not honor the value entered from data tab or as per data linkage specified. NPR-29239: Hotfix for CQ-4266856.

#### Forms - Interactive Communication {#forms-interactive-communication}

* When an apostrophe character is added, the prefilled fields in the letter appear as ASCII characters instead of regular alphabets. NPR-28863: Hotfix for CQ-4262900

### Forms JEE Installer {#forms-jee-installer}

* No new AEM Forms fixes in Forms JEE installer.

## Hotfixes and Feature Packs included in previous Cumulative Fix Packs {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19 is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

The key highlights of this Cumulative Fix Pack are:

* Enabled support for MS Translator API v3.0 support to AEM 6.2
* Log message added after successful installation of the package for all SPs, CFPs, and HFs.

### Assets {#assets}

* Cannot rename DAM folder if permission Edit ACL is missing. NPR-27555: Hotfix for CQ-104652
* Image Preset editor tool non-responsive in 6.2.1 CFP 17 and later. NPR-28147: Hotfix for CQ-4261041

### Sites {#sites}

* The Link Checker doesn't complete the job, gets stuck with no-responding links. NPR-27373: Hotfix for CQ-4256030
* The segment file doesn't load properly due to an additional root path that breaks the path of the segment. NPR-28014: Hotfix for CQ-4260332

### Integration {#integration-1}

* LiveCopy inheritance cancellation does not work properly on targeted containers. NPR-28129: Hotfix for CQ-4259813
* The  cq  :actions  are not taken  in  consideration for a targeted component. NPR-27616: Hotfix for CQ-4257497

* Display of icon for breaking inheritance is not coherent. NPR-27671: Hotfix for CQ-4257779

### Felix {#felix}

* Web console component detail fails with 500 after CFP 18 installation on AEM 6.2 SP1 instance. NPR-28350: Hotfix for CQ-4261095

### Translation {#translation}

* Enable support for MS Translator service in AEM 6.3 after upgrade of MS Translator to API v3.0. NPR-28123: Hotfix for CQ-4259096

### UI - Foundation {#ui-foundation}

* OOTB Sites Calendar shows incorrect dates. NPR-28392

### Granite {#granite}

* Dictionary is not invalidated for resource bundles using sling :basename . NPR-27624

### Sustenance {#sustenance}

* Package manager activity logs should be extracted in a separate log file. NPR-27323: Hotfix for Granite-14866
* A Standardized phrase/wording/log-line(s) in the error.log to be displayed when installation is completed. NPR-27835
* Granite package plugin is picking dependency of a lower version of org.apache.sling.i18n. Hotfix for CQ-4263245
* com.adobe.cq.com.adobe.cq.ui.commons bundle gets deleted on installing the latest CFP after 6.2SP1-CFP15. Hotfix for CQ-4258808

### Forms {#forms-1}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-1}

#### Adaptive Forms {#adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27843: Hotfix for CQ-4257315

### Forms JEE Installer {#forms-jee-installer-1}

* No new AEM Forms fixes in Forms JEE installer.

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included}

The following text documents the list of OSGI bundles and content packages included in the CFP.

List of OSGi bundles included in AEM 6.2 SP1-CFP19

[Get File](assets/cfp19_osgi_bundles.txt)

List of Content Packages included in AEM 6.2SP1-CFP19

[Get File](assets/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18 is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

The key highlights of this Cumulative Fix Pack are:

* Added support in DAM CommandLineProcess to kill the long-running process.
* Fixed session leak in ReplicationEventListener.
* Added redirection support to core page component.

### Assets {#assets-1}

* Camera RAW processes get stuck during periods of massive ingestion eventually blocking all workflow processing. NPR-26990: Hotfix for NPR-23860
* The download functionality leverages AEM Assets via  assetdownload  servlet allowing anonymous users to download all assets. NPR-27054, Hotfix for CQ-4254732
* Special characters appear broken in the subject line of email templates in AEM. NPR-26470: Hotfix for CQ-4252368

### Sites {#sites-1}

* Due to incorrect behavior of ConfigPostProcessor class, suspending parent image removes  cq : LiveRelationship mixing type from the child page. NPR-26745: Hotfix for CQ-4254163
* Add redirection support to core page component. NPR-26576: Hotfix for CQ-110529
* Migrate context hub to jquery 3. NPR-26956: Hotfix for CQ-4255472
* Anchor input fields appear out of the browsers visible section on the dialog until maximized. NPR-26852: Hotfix for CQ-4255019
* Copy paste of text inserting unwanted &lt;br&gt; in the Content fragment. NPR-26660: Hotfix for CRTE-151
* Classic  siteadmin  does not render the list in the right pane for some pages. NPR-27247: Hotfix for CQ-4251621
* (Classic UI) Attempts to move/rename pages generates an error, “An error occurred while moving page.” NPR-27179: Hotfix for CQ-4235907

### Integration {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever walks the entire tree to gather the available brands. NPR-27060: Hotfix for CQ-4255790

### WCM - Foundation Components {#wcm-foundation-components}

* Search functionality issue with the Foundation list component. NPR-26817: Hotfix for CQ-4250324

### Platform {#platform}

* Due to special character em dash, the Publisher is having issue flushing the cache. NPR-27199: Hotfix for CQ-4242790

### Granite {#granite-1}

* Package Validator does not validate packages included in CFP/SP. NPR-26775: Hotfix for Granite-22825

### Replication {#replication}

* JCR Session leak in ReplicationListener. NPR-27063: Hotfix for CQ-4232088

### Forms {#forms-2}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-2}

* No new AEM Forms fixes in Forms add-on package.

### Forms JEE Installer {#forms-jee-installer-2}

* No new AEM Forms fixes in Forms JEE installer.

#### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-1}

List of OSGi bundles included in AEM 6.2 SP1-CFP18

[Get File](assets/62cfp18updated_bundles.txt)

List of content packages included in AEM 6.2 SP1-CFP18

[Get File](assets/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17 is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

The key highlights of this Cumulative Fix Pack are:

* Added support to site Extension-less URLs in at-integration.js
* Removed S7 polling importer from S7 cloud service configuration.
* Changes to the audiences view to support folder structure for multi-tenant implementation.
* Update to  jqueryui   clientlib  v1.12.1.

### Assets {#assets-2}

* Starting workflows from Asset UI requires the user to have write/delete/modify permissions. NPR-25688: Hotfix for CQ-4250140
* Publish and unpublish buttons remain visible even for the users with no "replicate" permissions. NPR-25094
* (Workflow) Smart Tag Asset workflow doesn't process through the AEM proxy configuration. NPR-25915: Hotfix for CQ-4248202
* Remove S7 polling importer from S7 cloud service configuration. NPR-25239: Hotfix for CQ-95236

### Sites {#sites-2}

* Workflows started from the Editor -&gt; Page Information contain the context path in the payload. NPR-26389: Hotfix for CQ-76804 
* (External Link Checker) Invalid https links are shown as valid links. NPR-25541: Hotfix for CQ-4201333
* (Classic UI) When creating a standalone page under a live copy, the page is created as a live copy. NPR-25610: Hotfix for CQ-4249801
* Issues with publishing resources associated with the Design Importer component when a page is activated. NPR-25638: Hotfix for CQ-102532
* RTE richtext toolbar covers select list. NPR-25165: Hotfix for CQ-4248948
* Migrate contexthub to jquery 3. NPR-25059: Hotfix for Granite-19902
* For a nested parsys components, always the first (with least nested path) satisfying design is applied from multiple available components. For more information, see [Design Path Resolution](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html). NPR-25250: Hotfix for CQ-4246276

### Integration {#integration-3}

* Using the OOTB target integration, targeting a component renders the whole page instead of an empty targeted component. NPR-25273: Hotfix for CQ-4248003
* Breaking the inheritance in targeting mode still shows the component as targeted with the inheritance not broken in edit mode. NPR-25324: Hotfix for CQ-4248162
* When a personnalisation is defined on a page and an audience is resolved, the corresponding experience is displayed in edit mode. NPR-25731: Hotfix for CQ-4249465
* Erroneous teaser URL when using AEM with a non-default context path. NPR-25971: Hotfix for CQ-4250953
* Blank rendering when using optout. NPR-25295: Hotfix for CQ-4246792
* Experiences deleted from the author environment are never removed from the publish site upon page activation. NPR-24869: Hotfix for CQ-4247832

### DAM - DM Client {#dam-dm-client}

* (Chrome, Firefox) VideoPlayer ignores mouse clicks on touch enabled devices. Hotfix for CQ-4247370

### Platform {#platform-1}

* Allow to configure the max number of retries when acquiring/releasing a package. NPR-25328: Hotfix for Granite-22376
* Incorrect logging in case of replication errors. NPR-25308: Hotfix for CQ-4249402
* Installing the Forms AEM 6.2 Forms CFP8 to CFP14 causes Apache POI to fail. NPR-25053: Hotfix for Granite-21771

### Granite {#granite-2}

* User sync process is failing with OakConstraint0022 exception. NPR-25729: Hotfix for Oak-7428

### Communities {#communities}

* cq -social-as-provider  bundle doesn't start with mongo driver 3.x versions. NPR-26271: Hotfix for CQ-4252710

### UI - Foundation {#ui-foundation-1}

* Update to  jqueryui   clientlib  v1.12.1. NPR-25090: Hotfix for Granite-21981, CQ-4248897

* (Omnisearch): 'Title' property is vulnerable to Cross-site (XSS) scripting in Sites. NPR-24994: Hotfix for Granite-19933

### Forms {#forms-3}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-3}

#### Adaptive forms {#adaptive-forms-2}

* Wrong encoding while submitting data from Adaptive Form. NPR-25539

#### Forms - Management {#forms-management}

* Unrelated form assets reported as references while publishing the page. NPR-26167: Hotfix for CQ-4251004

### Forms - JEE Installer {#forms-jee-installer-3}

#### Document Security {#document-security}

* Variable is populated as data type List, sub type is string, but we get a "cannot coerce object" error. NPR-26194: Hotfix for CQ-4252287
* Unable to access watermark configurations after installing 6.2-SP1-CFP15. NPR-26130: Hotfix for CQ-4250984

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-2}

List of OSGi bundles included in AEM 6.2 SP1-CFP17

[Get File](assets/62cfp17updated_bundles.txt)

List of Content Packages included in AEM 6.2SP1-CFP17

[Get File](assets/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16 is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

The key highlights of this Cumulative Fix Pack are:

* Added STARTTLS support in Day CQ Mail Service.
* Fixed ContextHub icons alignment in profile popover.
* Fixes in show/hide functionality of drop-down component.
* Upgrade to latest Jackson version 2.8.11

### Assets {#assets-3}

* Unable to initiate a workflow from a list view. NPR-24393: Hotfix for CQ-4245788
* (Firefox/Chrome) Unable to download assets in Asset Share page. NPR-24523: Hotfix for CQ-4224408
* Increased the default quality for video preview in AEM. NPR-24148: Hotfix for CQ-4244310

### Integration {#integration-4}

* When a component is targeted on publish instance, flickering appears showing the default experience before the targeted one. NPR-23992: Hotfix for CQ-4242038
* Experiences deleted from the author environment are never removed from the publish site upon page activation. NPR-24869: Hotfix for CQ-4247832

### Platform {#platform-2}

* Patch jQuery 1.12.4 from clientlib to include security fix. NPR-24129: Hotfix for Granite-20058
* Added STARTTLS support in Day CQ Mail Service. NPR-23941: Hotfix for CQ-4240397
* Remove default MERGE_PRESERVE aclHandling. NPR-24593: Hotfix for Granite-21889
* LineChecker fails to externalize links when request contains invalid query parameters. NPR-24127: Hotfix for CQ-4241893

### MSM {#msm}

* Proactive hotfixes to Cross-Site Scripting attacks (XSS). NPR-21893: Hotfix for CQ-4223385
* MSM LiveRelationship: effective RolloutConfig wrong if BlueprintConfig is on root. NPR-23999: Hotfix for CQ-4243000

### Sites {#sites-3}

* Creating a new experience in a live copy area requires the inheritance to be broken to be configured. NPR-24995, Hotfix for CQ-4248209
* (Touch UI) Several icons on the top toolbar disappear while locking or unlocking a page. NPR-23954: Hotfix for CQ-4243345
* The fields are not properly aligned in the contexthub. NPR-23958
* Publish action on locked page breaks authoring. NPR-23970: Hotfix for CQ-4243203
* OOTB reports in /etc/reports/ are not working properly and show no historical data graph. NPR-20035: Hotfix for CQ-4220180
* Launch creation fails while initiating 'Request launch' workflow on a Project. NPR-24255: Hotfix for CQ-4245030
* HTML tags and attributes ignored by emails post CFP10 installation. NPR-24287: Hotfix for CQ-4240028
* TagPicker: Tag suggestion in the tag metadata schema tag field queries taggable nodes, hence, taking a long time to load. NPR-24347: Hotfix for CQ-4244291
* Salesforce integration fails with proxy configurations. NPR-24418: Hotfix for CQ-4245300
* (WCM) PageManager leaves Page checked in on Exception during create Revision. NPR-24565: Hotfix for CQ-4246203
* Device Emulator button disappears from edit and preview mode after applying CFP14. NPR-24566: Hotfix for CQ-4247060
* (Classic UI) The entire tags show as empty once authored in dialog. NPR-24688, Hotfix for CQ-4246407
* Unable to create version on first attempt. NPR-24774: Hotfix for CQ-4232176
* OOTB reports in /etc/reports/ are not working properly and show no historical data graph. NPR-24138: Hotfix for CQ-4220180

### Vulnerability {#vulnerability-1}

* Salesforce integration is vulnerable to Server Side Request Forgery (SSRF). NPR-24289: Hotfix for CQ-4245277
* Server Side Request Forgery (SSRF) vulnerability in ReportingServicesProxyServlet. NPR-24657: Hotfix for CQ-4246880

### Granite {#granite-3}

* Metadata read operations are not getting terminated. NPR-24240: Hotfix for Granite-19866
* Update Jetty to 9.4.11.v20180605 to fix vulnerabilities. NPR-25033: Hotfix for Granite-22120

### WCM - Foundation Components {#wcm-foundation-components-1}

* PageComparator throwing ClassCastException while sorting pages. NPR-24123: Hotfix for CQ-4244048
* Show/Hide functionality of the form drop-down component is not working as expected. NPR-24562: Hotfix for CQ-4222853

### User Interface {#user-interface}

* High CPU utilization is observed due to lot of requests in Admin Search functionality. NPR-23588: Hotfix for Granite-21286
* (Classic UI) Component displays the default values even if the associated form data model service is set to empty field. NPR-21903: Hotfix for GRANITE-19744
* Multifield throwing NPE when no FormData present for request. NPR-24513: Hotfix for Granite-21055

## Forms {#forms-4}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-4}

#### Core {#core}

* (OSGI) AEM Forms OSGI impacted by Jackson data binding security alert. NPR-24274: Hotfix for CQ-4230245

#### Rights Management {#rights-management}

* Apache POI fails post installation AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Hotfix for CQ-4245898, CQ-4244778

#### HTML5 Forms {#html-forms}

* The data is not populated with prefilling of multi-line fields in HTML preview. NPR-23357: Hotfix for CQ-4244212
* When a letter is previewed via default preview, layout fragment mapping is not displayed while the same appears correctly when clicked on preview button. NPR-22993: Hotfix for CQ-4237745
* Issue with HTML preview of a text field when a Social Security Number pattern is applied to a template. NPR-23205

#### Adaptive Forms {#adaptive-forms-3}

* “Guidelib is not defiend” error while adding AEM form to parsys component. NPR-24269: Hotfix for CQ-4244546

### Forms JEE Installer {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Window line endings in Shell script files cause LCM not to run in UNIX. NPR-22958

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-3}

List of OSGi bundles included in AEM 6.2 SP1-CFP16

[Get File](assets/6_2cfp16_bundlecomparison-list.txt)

List of Content Packages included in AEM 6.2SP1-CFP16

[Get File](assets/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15 is an important update that includes key customer fixes released since the general availability of [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html).

The key highlights of this Cumulative Fix Pack are:

* Proactive security fix in Foundation table to maintain design consistency.
* Added support for typeHint to save values as string.
* Provides enhanced security for Forms prefill service
* Update to latest adobe-reader-extensions-dsc.jar file for fixes in Reader Extension.
* Adjusted validation hook to consider ":invalid" items for the boost number input.

### Assets {#assets-4}

* EmbedXMP data is always set to “active” for Ptiff generation process. NPR-22776: Hotfix for CQ-4234498
* Unable to set multiple default values in Multi-value fields. NPR-22900: Hotfix for CQ-4239000
* (Dynamic Media) On selecting Dynamic Renditions checkbox, downloaded zip file yields the original TIFF image with zero byte file. NPR-22410: Hotfix for CQ-4198471
* (Touch UI) Default upload location for assets in column view. NPR-23475: Hotfix for CQ-4237057

### Integration {#integration-5}

* In Target mode, authors can modify a component inherited from the blueprint without cancelling the inheritance. NPR-22751: Hotfix for CQ-4237907
* Path variable is not properly encoded leading to non-persistent Cross site scripting (XSS). NPR-22851

### MSM {#msm-1}

* During rollout of a LiveCopy with multiple roll-out configurations, if a ResourceNameConflict arises below the root, the roll-out flow terminates without including all branches. NPR-22842: Hotfix for CQ-4236188

### Platform {#platform-3}

* Implement a polling limit in one request for reverse application. NPR-23351: Hotfix for Granite-21135****
* Message pattern change is not reflected on custom loggers. NPR-23486: Hotfix for CQ-4241974

### Sites {#sites-4}

* Creating a link within a text of a Rich Text Editor to a document with spaces or other special characters does not work. NPR-22289: Hotfix for CQ-4224321
* Saving the segment with a huge value (10000000000) sets the boost to 0 causing error message. NPR-22524: Hotfix for CQ-4237006
* Unable to click on Add item in Multifield component. NPR-22552: Hotfix for CQ-4237404
* The horizontal scrollbar is not visible when segment has a long title. NPR-22615: Hotfix for CQ-4237001
* Loading of an empty audience generates an incorrect javascript code. NPR-22974: Hotfix for CQ-4238734
* When scheduling an activation or deactivation the workflow title is mandatory, hence, the custom workflow title is not translated in the timeline. NPR-23121: Hotfix for CQ-4237552
* Request for fixes to issues around Target segments in Sites. NPR-23128
* (Firefox) Checkbox for selected persona is not the correct one. NPR-23345
* Labels for the different modes are displayed along with icons. NPR-23275
* 'Invalid recursion selector value' error while migrating a component from AEM 6.0 to AEM 6.2. NPR-23503: Hotfix for CQ-4241258

### Communities {#communities-1}

* Web and mail notifications do not get triggered due to message failure to the groups. NPR-23447: Hotfix for CQ-4242880

### Translation {#translation-1}

* Asset language copies are getting created when “Do not translate” asset is set on the translation configuration. NPR-22540: Hotfix for CQ-4237962

### User Interface {#user-interface-1}

* Using Omnisearch with a hyphen query returns a server error. NPR-22999: Hotfix for Granite-19674
* DatePicker doesn’t support manually set external type hint set by hidden field. Changing the type hint gets a conversion error. NPR-23333: Hotfix for Granite-21194

### WCM - Foundation Components {#wcm-foundation-components-2}

* CAPTCHA Component has been deprecated for better security, if you are using CAPTCHA component, then message "Captcha component is deprecated and should no longer be used." will be displayed after installing 6.2 SP2-CFP15 or later release. AEM component can be customized to include reCAPTCHA for better security NPR-22151: Hotfix for CQ-4220052
* WCM Foundation component 'Table' is vulnerable to Stored Cross Site Scripting. NPR-23206: Hotfix for CQ-4240760

### Vulnerability {#vulnerability-2}

* Cross-site scripting (XSS) in Admin UI Project links. NPR-23272: Hotfix for CQ-4241795

## Forms {#forms-5}

### Forms add-on package {#forms-add-on-package-5}

#### Correspondence Management {#correspondence-management}

* When a letter is previewed via default preview, layout fragment mapping is not displayed while the same appears correctly when clicked on preview button. NPR-23335: Hotfix for CQ-4237745
* Data in the letter corresponding to bindings defined in XDP is not populated on using direct letter URL. NPR-24145: Hotfix for CQ-4244290

#### Mobile Forms {#mobile-forms}

* (Correspondence Management) Data misalignment while loading letter with target XML. NPR-22993: Hotfix for CQ-4237663

#### Reader Extensions Service {#reader-extensions-service}

* Unable to apply reader extension on Adobe PDF. NPR-23067

#### Forms Manager {#forms-manager}

* Forms embedded in Site are not published on republishing the Site Page. NPR-23014: Hotfix for CQ-4236566

#### Vulnerability {#vulnerability-3}

* Proactive hotfixes for Cross-Site scripting. NPR-20624: Hotfix for CQ-4206055
* Stored Cross-Site Scripting (XSS) vulnerability in the notes tab of the Forms Manager. NPR-27157: Hotfix for CQ-4255556

#### Encryption Service {#encryption-service}

* (OSGI) [JEE] Incorrect signature status for PDF with attachment while verifying using "Validate PDF process". NPR-23269, NPR-23737

### Forms JEE Installer {#forms-jee-installer-5}

#### Core {#core-1}

* The issues reported in the static code analysis of Core-ext should be fixed. NPR-13947

#### PDFG Service {#pdfg-service}

* HTML to PDF convertor is not working. NPR-21545

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-4}

The following text documents the list of OSGI bundles and content packages included in the CFP.

List of OSGi bundles included in AEM 6.2 SP1-CFP15

[Get File](assets/6_2cfp15updated_bundles.txt)

List of Content Packages included in AEM 6.2SP1-CFP15

[Get File](assets/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Improved editability of metadata properties of assets.
* Re-configured the Password Expiration Notification job for assets already in expired state.
* Customized Touch UI console to extend additional locales. 
* Updated cq-msm-core for efficient Livecopyindex synchronisation. 
* Streamlined replication functionality to various Rollouts.

### Assets {#assets-5}

* Users unable to download assets with disclaimer and long filenames. NPR-22163: Hotfix for CQ-4235274
* Single quote character prevents the metadata update in bulkview and the UI is completely broken when you open the properties of an asset using the quick toolbar actions. NPR-22317, NPR-22353: Hotfix for CQ-4236990, CQ-4236469
* Asset Expiry notification job does not deactivate the expired assets. NPR-22346: Hotfix for CQ-4237188
* Asset download fails when using Digital Rights Management in Assets on Safari. NPR-22378: Hotfix for CQ-4236460
* Web rendition for small image has inaccurate pixel size. NPR-22435: Hotfix for CQ-4236742

### Sites {#sites-5}

* (Touch UI) Moved tag appears in old and new location in page properties. NPR-21921, Hotfix for CQ-4238598
* (Touch UI) Rich Text Editor removes all attributes other than id from &lt;a&gt; tag. NPR-22045: Hotfix for CQ-4234133
* Pasting content directly in Rich Text Editor using CTRL+V skips the line breaks. NPR-22117: Hotfix for CUI-5881
* (Touch UI) Unable to show more than 40 tags under namespace. NPR-22290: Hotfix for CQ-99114
* RSS Feed issues, port -1 to AEM 6.2 NPR-22158: Hotfix for CQ-4233339
* (IE) When authoring any character in Rich Text field for the first time, a trailing space gets added to the character. NPR-22443: Hotfix for CQ-4235343
* When attempting to match the package name, Java Use object freezes the SightlyJavaCompilerService due to a trailing space character in the package declaration. NPR-22557: Hotfix for Granite-20836
* The Touch UI console does not pick up new languages for tagging. NPR-22250: Hotfix for CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Both Publication date and cover date were required fields to be set for folios before they are uploaded to DPS. NPR-22484

### Commerce {#commerce}

* Multiple cross-site scripting (XSS) vulnerabilities on commerce create catalog wizard. NPR-22344: Hotfix for CQ-4237017

### MSM {#msm-2}

* LiveCopyIndex synchronization leads to congestion of threads during long index updates. NPR-22214: Hotfix for CQ-90667
* cq:cugEnabled property is disabled when another field in a livecopy is edited, hence, making the page unprotected. NPR-22246: Hotfix for CQ-4236050
* The Page Roll-out action fails to update children when a page is suspended. NPR-22483: Hotfix for CQ-4236956
* Rollout of a structure which has been moved in a master leads to a wrong cq:moveTarget. NPR-22373: Hotfix for CQ-4232536

### Integration {#integration-6}

* Trying to sort offers in the offer selector library results in erratic behavior. NPR-22208: Hotfix for CQ-4235439 
* TargetContentImpl makes AEM sluggish during long running queries. NPR-22361: Hotfix for CQ-4236907
* Target engine (mbox.js, at.js) does not use mangled URLs and uses URLs containing colons which might fail with certain deployments. NPR-22366: Hotfix for CQ-4237854 
* Page personalization requires publication right on the brand node. NPR-22370: Hotfix for CQ-4236895

### Foundation {#foundation}

* Apache Sling Scripting Sightly Models use Provider bundle **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: Hotfix for Sling-5944, Sling-6866

### Projects {#projects}

* Workflow Starter not able to accept TypeHint value of String. NPR-22436: Hotfix for CQ-4237855

### Translation {#translation-2}

* Investigate issues with Preview functionality. NPR-22201: Hotfix for CQ-4223753

### User Interface {#user-interface-2}

* (Classic UI) Component displays the default values even if the associated form data model service is set to empty field. NPR-21903: Hotfix for GRANITE-19744

### WCM - Foundation Components  {#wcm-foundation-components-3}

* Error when publishing a Live Copy page that points to an Importer Page in Adobe Campaigns. NPR-22470: Hotfix for CQ-4237164
* JavaScript errors while opening the Experience Fragments Editor. NPR-22598: Hotfix for CQ-4238415

### Workflow {#workflow}

* The Day CQ Workflow Email Notification Service triggers one e-mail per Mongo node for WorkflowCompleted and WorkflowAborted notifications. NPR-22486: Hotfix for CQ-4238172

## Forms {#forms-6}

### Forms add-on package {#forms-add-on-package-6}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

#### Adaptive Forms {#adaptive-forms-4}

* Inconsistency in Drop-down placeholder value in Adaptive Form across IE11 and Chrome. NPR-22405: Hotfix for CQ-4227096

### Forms JEE installer {#forms-jee-installer-6}

#### Install LCM {#install-lcm}

* Update Jsafe Jars to Cryptoj 6.1.3.1 in installer & LCM. NPR-22744

### Feature Packs Included {#feature-packs-included}

#### Process Management {#process-management}

* (HTML Workspace) When a user claims a task, count of queue is refreshed for that particular user but not for other users unless the page is refreshed. NPR-19778: Hotfix for CQ-4233665

### OSGI bundles and content packages included in CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

List of OSGi bundles included in AEM 6.2 SP1-CFP14

[Get File](assets/6_2cfp14updated_bundles.txt)

List of Content Packages included in AEM 6.2SP1-CFP14

[Get File](assets/6_2_cfp14contentpackage-list.txt)
AEM Cumulative Fix Pack 6.2 SP1-CFP13 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Enabled Static Parameter field configuration inside Target Component Settings while using AT.js as Client library.
* Fixes in show/hide functionality of drop-down component. 
* Fixes for using target syncing audiences.
* Increased the versatility for Correspondence Management to accommodate special characters.

### Assets {#assets-6}

* Version Purge fails to remove old versions of assets. NPR-21682: Hotfix for CQ-4212996
* Reordering of folders under an re-orderable folder is not persisted. NPR-21964: Hotfix for CQ-4231761

### Sites {#sites-6}

* (TouchUI)(ClassicUI) Multiple cross-site scripting (XSS) vulnerabilities in HTL and core components. NPR-21532: Hotfix for CQ-4232305 and CQ-4232511
* Creating/Formatting content (e.g. assigning/removing new list styles) on a selected text does not work fine in Internet Explorer 11. NPR-21533: Hotfix for CQ-4230689
* (Safari) Users are unable to view all the assets in the asset finder panel. NPR-21981: Hotfix for CQ-4213720
* Time Warp returns "RecursionTooDeepException" error with garbled page and no new version is created even when the date is changed. NPR-21707: Hotfix for CQ-4199536
* When loading a page in the editor, the WorkflowStatusprovider (pageinfo.json) gets loaded three times causing AEM instance to perform slow. NPR-21778: Hotfix for CQ-59232

### Integration {#integration-7}

* Creation of audiences of Mobile Type & Browser in authoring Target mode is not working in AEM. NPR-21676, NPR-21681: Hotfix for CQ-4232100
* Under high latency during a refresh of a targeted component, it's possible to add another offer before the component is refreshed completely. NPR-21744: Hotfix for CQ-4233158/CQ-4234293
* Users are not able to see test Static Param values in the mbox call which can be seen when testing with AT.js as the client library in cloud configuration. NPR-21930: Hotfix for CQ-4234520

### Platform {#platform-4}

* Performance issues with user sychronisation when number of users or groups is large. NPR-20431: Hotfix for CQ-4223282
* Users not synced with User Synchronization using Sling Distribution. NPR-21911: Hotfix for Granite-20404
* Preventing stop words from being highlighted in search excerpts (on a Geometrixx page). NPR-21835: Hotfix for Granite-21067   
  Note: This fix requires the Oak CFP 1.4.20 or higher.

### Translation {#translation-3}

* jcr property is missing for Initiator user id while creating translation project. NPR-21715: Hotfix for CQ-4230713

### WCM - Foundation Components {#wcm-foundation-components-4}

* Show/Hide functionality of the form drop-down component is not working as expected. NPR-22164: Hotfix for CQ-4235288

## Forms {#forms-7}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-7}

#### Adaptive Forms {#adaptive-forms-5}

* XML External Entity Injection (XXE) injection in Adaptive Forms. NPR-21982: Hotfix for CQ-109878
* (iOS11) When clicked on file attachment component, file attachment opens up camera instead of device file browser. NPR-21926: Hotfix for CQ-4214348
* Missing title in theme creation UI is causing exception and failing rendering of the dialog. Hotfix for CQ-4236143

#### Correspondence Management {#correspondence-management-1}

* Rendering issues with xml data containing special characters. NPR-21712: Hotfix for CQ-4229137

### Forms JEE installer {#forms-jee-installer-7}

#### Assembler Service {#assembler-service}

* PDF file generated using 6.2.0-ASM-1017-003 is broken. NPR-21427: Hotfix for CQ-4228046

#### PDFG Service {#pdfg-service-1}

* OCR failure due to unexpected page size (PDF) from PNG, JPEG & TIFF files. NPR-19489: Hotfix for CQ-4209079

## OSGI bundles and content packages included in CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

List of OSGi bundles included in AEM 6.2 SP1-CFP13

[Get File](assets/cfp13_bundlecompare-list.txt)

List of Content Packages included in AEM 6.2SP1-CFP13

[Get File](assets/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Improved metadata handling for multivalue fields.
* Support for multicharacter (more than two) country codes in translation workflows.
* Improved rendering of pages with multiple nested components.
* Improved synchronization of publication dates for assets between AEM and Adobe Digital Publishing Suite.

### Assets {#assets-7}

* Too many characters in OmniSearch causes AEM server to crash. NPR-21083: Hotfix for CQ-4223602
* Values specified in the second option in a Multivalue Field in Metadata Schema are not appended to the previously-specified values in CRX-de. NPR-21220: Hotfix for CQ-4224526
* Asset download fails when using Digital Rights Management in Assets on Safari. NPR-21387: Hotfix for CQ-4230287

### Sites {#sites-7}

* (DAM) (ClassicUI) Multiple cross-site scripting (XSS) vulnerabilities in some SWF files in AEM CQ Author/Publish quickstart. NPR-21073, NPR-21074: Hotfix for NPR-20612
* The tag picker does not translate the tags that are available in multiple languages.NPR-21221: Hotfix for CQ-78855
* Rendering issues with AEM article console as using multiple nested components make it sluggish. NPR-21271: Hotfix for CQ-4224158

### Integration {#integration-8}

* When adding a Target framework, Targeting mode not available in the Select mode list in the editor. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) Publication dates for folios in AEM don't match with the dates that appear in Folio Producer. NPR-21145

### MSM {#msm-3}

* Live Copy reset process gets stopped after deleting the first local page in the LC. NPR-21276: Hotfix for CQ-4229743

### Platform {#platform-5}

* Custom taglib that reference tags implemented as a script are not found after upgrading to AEM 6.3. NPR-20149: Hotfix for Granite-18433

### Translation {#translation-4}

* Translation workflows fail with lang_country codes longer than 2 characters. NPR-21088: Hotfix for CQ-4197439
* Asset page should not be allowed to be submitted again to a translation project until the project completes. NPR-21219: Hotfix for CQ-4209908

### User Interface {#user-interface-3}

* Select component doesn't delete the target property during form submission. NPR-21163: Hotfix for GRANITE-14125
* HTTP.encodePathOfURI expand double encodes the plus sign '+'. NPR-21417: Hotfix for GRANITE-16340

### Vulnerability {#vulnerability-4}

* Cross-site scripting (XSS) in DAM metadata editor. NPR-21434: Hotfix for CQ-83472
* Multiple SWF files vulnerable to Cross-site scripting (XSS). NPR-20612: Hotfix for CQ-4213297

## Forms {#forms-8}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-8}

#### Correspondence Management {#correspondence-management-2}

* (IE11) Initial render of the HTML content occurs only on the left side while the right side loads intermittently after complete UI is loaded. NPR-21554
* Letter preview submit button gets disabled after installing AEM 6.2 SP1-CFP9. NPR-21547
* On selecting Asset linkage type, Asset Selector window does not open in Edit Letter Data Binding wizard. NPR-21164: Hotfix for CQ-4194567
* To edit an inline or editable text module, tap the relevant Edit icon or double-click the relevant text module in the letter preview. NPR-21402

#### Adaptive Forms {#adaptive-forms-6}

* The AEM Forms submit button component shows type="button" instead of type="submit". NPR-21007
* Data remains persistent on adding or deleting new panels for repeatable panels. NPR-21408

### Forms JEE installer {#forms-jee-installer-8}

#### Core {#core-2}

* Upgrading to the latest Java 8 Update 131 throws an exception: "JsafeJCE provider is disabled, a FIPS 140 required self-integrity check failed". NPR-21355  

  **Note:** This NPR requires additional settings, for details refer to [Latest Java 8 update](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr).

* Update jsafe jars to cryptoj 6.1.3.1 in Core, Encryption, Signature & Document Security. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Install LCM {#install-lcm-1}

* Update Jsafe Jars to Cryptoj 6.1.3.1 in installer & LCM. NPR-21362

#### PDFG Service {#pdfg-service-2}

* Update Jsafe Jars to Cryptoj 6.1.3.1 in PDFG. NPR-21359

#### Process Management {#process-management-1}

* (HTML Workspace) Enabling column resizing so that the name category does not appear truncated. NPR-19770: Hotfix for CQ-4233668

#### Reader Extensions Service {#reader-extensions-service-1}

* Update jsafe jars to cryptoj 6.1.3.1 in RE. NPR-21357

## OSGI bundles and content packages included in CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

List of OSGi bundles included in AEM 6.2 SP1-CFP12.1

[Get File](assets/cfp12_bundlecomparsion-list1.txt)

List of Content Packages included in AEM 6.2 SP1-CFP12.1

[Get File](assets/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Updated cq-msm-core for efficient Livecopyindex synchronisation.
* Improved editing efficiency for content fragments.
* Provides validation option in package manager for detecting ACL permissions.
* Introduced the ability of Campaign to include email id for customer correspondence.
* Improved video encoding abilities for Dynamic Media files.
* Fixes in Sightly Component and LiveCopies.

### Assets {#assets-8}

* Dynamic Media video encoding fails for files that include spaces in their names. NPR-20818: Hotfix for CQ-102469
* Multiple cross-site scripting (XSS) vulnerabilities in some SWF files in AEM CQ Author/Publish quickstart. NPR-21071, NPR-21072
* Users unable to download assets with disclaimer and long filenames. NPR-20255: Hotfix for CQ-4222139

### Sites {#sites-8}

* AEM and Campaign integration: Special links get rewritten in Adobe Campaign preventing the customers to send mailto: hyperlinks in their emails. NPR-20787: Hotfix for CQ-4225760
* (Touch UI) AEM usability concerns and performance issues when the language is set to French. NPR-20854: Hotfix for CQ-4227628
* Linking an encoded asset file using link plugin in RTE returns empty link. NPR-20626, NPR-21059: Hotfix for CQ-4223011
* Content Fragment metadata editor prevents content authors from saving changes to Content Fragments. NPR-20641: Hotfix for CQ-4224755
* Page Property Alias leads to Request Publication/Request Unpublication. NPR-20731: Hotfix for CQ-4226227
* Text component issues with encoding of link in RTE element. NPR-20755: Hotfix for CQ-4224321

### Platform {#platform-6}

* ResourceResolverImpl.map() does not invoke ResourceDecorator. NPR-20788: Hotfix for GRANITE-19718
* org.apache.sling.i18n.DefaultLocaleResolver not able to process requests via org.apache.sling.engine.SlingRequestProcessor. NPR-20706: Hotfix for CQ-94880
* Request to add a validation option in Package Manager to detect if any ACL permissions/privileges are changed on a particular package. Hotfix for CQ-4229196

### Integration {#integration-9}

* (Search&Promote) Ambiguous filter definition for the content package leads to overwritten paths on installation. NPR-20808: Hotfix for CQ-4227615

### Workflow {#workflow-1}

* Stability issues with AEM production server deployment. NPR-20979: Hotfix for Granite-19104

### Projects {#projects-1}

* (Touch UI) Unable to add team members to a project. NPR-20990: Hotfix for CQ-4205375

### WCM-Foundation Components {#wcm-foundation-components-5}

* Sightly Image Component 'link to' generates 403 error due to missing .html extension. NPR-20823: Hotfix for CQ-4195909
* On a blueprint site using LiveCopy, trying to delete a Form component throws a NullPointerException and adds back the Form component instead of deleting it. NPR-20855: Hotfix for CQ-4204628
* LiveCopyIndex synchronization leads to congestion of threads during long index updates. NPR-20634: Hotfix for CQ-90667

### Security {#security}

* Proactive XSS library update. NPR-21174
* Upgrade to Apache Commons Email 1.5 which presents a simplified API for sending e-mail. NPR-20509: Hotfix for Granite-18240
* Security patch applied to Apache Sling XSS Protection API to eliminate the possibility of XSS bypassing. NPR-21290: Hotfix for GRANITE-19924  
* XSS bypass in XSSAPI#getValidHref function. NPR-21174: Hotfix for Granite-19924

### Mobile Apps {#mobile-apps}

* Fixed issues with curl Head requests for OOTB assets in AEM. NPR-20511: Hotfix for CQ-4221520 and CQ-103024

## Forms {#forms-9}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

The key highlights for AEM Forms are:

* Enabled certificate authentication for Workbench users.
* Usability fixes for Correspondence Management, HTML5 forms, and AEM Forms workspace.

### Forms add-on package {#forms-add-on-package-9}

#### HTML5 Forms {#html-forms-1}

* Usability issues with scribble component on iOS 10 & 11 devices. NPR- 21092

#### Correspondence Management {#correspondence-management-3}

* (Correspondence UI) Disable submit button after one click. NPR-21078

### Forms JEE installer {#forms-jee-installer-9}

#### Assembler Service {#assembler-service-1}

* docConvertor fails to produce PDF/A with error "The prefix "stEvt" for element "stEvt:action" is not bound". NPR-21032: Hotfix for CQ-4222540
* An exception is thrown with name java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE while invoking service OMPFSubmission/PDFA/PDFtoPDFA. This prevents the short-lived signature verification process from completing until the server is restarted. NPR-20792

#### Workbench {#workbench}

* Enable certificate authentication for Workbench users. NPR-17548: Hotfix for CQ-4214486

#### Process Management {#process-management-2}

* Prepare data process invokes multiple times when mobile form is rendered with dataref parameters. NPR-19801: Hotfix for CQ-4230427: CQ-4230400

## OSGI bundles and content packages included in CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

List of OSGi bundles included in AEM 6.2 SP1-CFP11

[Get File](assets/cfp11_bundlecomparsion-list.txt)

List of Content Packages included in AEM 6.2 SP1-CFP11

[Get File](assets/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Added a new utility function onDialogLoaded for tests.
* Added frontend unit tests and configurations to ClientLibraryProxyServlet. 
* Performance fixes in Multiple image in-place editor component.
* Configuration updates in Apache Sling JCR ResourceBundleProvider.

### Assets {#assets-9}

* Asset preview does not work if asset update workflows are disabled. NPR-20543: Hotfix for CQ-4204986
* Rendering issues with class added in the granite: class property (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix for CQ-4219238
* Thumbnail assets having special characters in title show java object in alt attribute of NPR-20347: Hotfix for CQ-4223620
* Replace version comparison code with Adobe proprietary code due to licensing issues. NPR-20273: Hotfix for CQ-4223758
* Processing issues when uploading CMYK PSB files with multiple alpha layers. NPR-20251: Hotfix for CQ-4220869
* Internationalization dictionaries do not work unless server is restarted in org.apache.sling.i18n 2.5.6. NPR-20525: Hotfix for Granite - 19490
* No thread dumps are being generated according to the scheduler period with default Thread Dump Collector config (default AEM start-up). NPR-20288: Hotfix for GRANITE-19488 / GRANITE-12741 / CQ-90647.

### Sites {#sites-9}

* If the modified date filter is changed after opening the saved search, there is no effect on the results and the results displayed are same as the previous saved value of the modified date filter. NPR-19739: Hotfix for CQ-4219425
* Pages with nested components failed to load. NPR-20312 
* Request for Deletion workflow is triggered on deletion of workflow packages. NPR-20266: Hotfix for CQ-4221686
* (Touch UI) Issue with Copy/Paste with OS Clipboard and internal AEM Clipboard. NPR-20228: Hotfix for CQ-4220383
* AEM instance becomes sluggish with list view when multiple assets (more than 100) are being loaded. NPR-20034: Hotfix for CQ-4222695
* (Touch UI) Deletion of launches via Classic UI console make all pages uneditable. NPR-20520: Hotfix for CQ-4225074
* Target dropdown does not work with multiple RTEs components in a dialog. NPR-20345: Hotfix for CQ-4220981

### Platform {#platform-7}

* When accessed using anonymous session, the ClientLibraryProxyServlet does not proxy requests to client libraries on the publish instance and throws HTTP 404 not found error. NPR-20195: Hotfix for Granite-14409

### Integration {#integration-10}

* Selecting target engine as Adobe Target prevents the component from being loaded and throws an error in the server log. NPR-20058: Hotfix for CQ-88071,CQ-109698,CQ-4201600

### Commerce {#commerce-1}

* No confirmation or redirect popup message appears on creating products of the same page. NPR-20257: Hotfix for CQ-4223414

### User Interface {#user-interface-4}

* When Datepicker is a field in a multifield, the values saved in date fields are not persisted while editing the component. NPR-20077: Hotfix for GRANITE-19147
* Previous queries do not get aborted in case consecutive queries are triggered leading to incorrect results. NPR-20397: Hotfix for GRANITE-19306

### WCM - Foundation Components {#wcm-foundation-components-6}

* ImageMap property still exists even after removing the images from Multiple image in-place editor component. NPR-20142: Hotfix for CQ-4222982

## Forms {#forms-10}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-10}

#### Adaptive Forms {#adaptive-forms-7}

* valueCommit Script is executed twice for DropDownList when changed through UI. NPR-19989: Hotfix for CQ-110212

### Forms JEE Installer {#forms-jee-installer-10}

**Process Management**

* The CFP package contains AEM Forms HTML Workspace version 2.2.26. NPR-20099
* Pre-filled form does not work when mobile form is configured to view as PDF. NPR-20566

**Rights Management**

* CAC / Mutual Authentication Certificate Selection Dialog should display certificates with Enhanced Key Usage (EKU) as client-auth or smart card logon. NPR-20708
* Forms JEE Supports PKCS#11 Mutual Authentication. NPR-15001

## OSGI bundles and content packages included in CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

List of OSGi bundles included in AEM CFP 6.2 SP1-CFP10

[Get File](assets/bundle-list-cfp10.txt)

List of Content Packages included in AEM CFP 6.2 SP1-CFP10

[Get File](assets/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Adapted Analytics Classic UI configuration for secret input.
* Fixes for independent persistence cache for Contexthub.
* Accurate computation of Asset dimensions.
* Optimized AEM performance when publishing assets to Brand Portal.
* Fixes in Resourcetype value in canvas node.
* Enabled case-sensitive and special characters search functionality for document fragment content.
* Enhanced Adaptive Forms to attach PDF as attachments in Safari.  
  Provides a new Dynamic Media that connects to the new Dynamic Media Publishing Infrastructure for faster and more scalable replication.

### Assets {#assets-10}

* AEM Assets unable to extract subasset references for InDesign assets include duplicate links to the asset. NPR-19006: Hotfix for CQ-4204186
* Sort option is not working for assets inside the collection under Commerce. NPR-19508: Hotfix for CQ-4213622
* When an asset with the same name as a pre-existing asset is moved to the same location, the value of cq: lastReplicationAction for the assets is swapped between themselves, which causes the creation of wrong metadata. NPR-19531
* An error message is displayed when publishing a large number of assets despite all assets being published correctly. NPR-19629: Hotfix for CQ-4219611
* Static Renditions are listed with fixed dimensions and do not reflect the size of the actual rendition. NPR-20004
* AEM instance becomes sluggish when multiple assets (more than 4) are being published to Brand Portal. NPR-20009

### Sites {#sites-10}

* AEM displays unexpected behavior when a user tries to publish /unpublish/create version of a page locked by another user. NPR-19249; Hotfix for CQ-4215298 and CQ-4203856
* While promoting the nested launch manually, the child page is getting deleted. NPR-19704
* Persistence issues when ContextHub stores overwrite default persistence layer during initialization. NPR-19979: Hotfix for CQ-4218399
* Content fragments are overlapping with other buttons. NPR-19980: Hotfix for CQ-4221519
* Site page not displayed when viewed using alias in SiteAdmin. NPR-20053: Hotfix for CQ-4221478
* Error when publishing a Live Copy page that points to an Importer Page in Adobe Campaigns. NPR-20066: Hotfix for CQ-4220846

### Platform {#platform-8}

* Upgraded Apache POI to version 3.16 to support inclusion of background image of PPT slides in renditions. NPR-18286
* Rendering issues with Internet Browser 11 and Edge while uploading multiple assets in the same folder. NPR-20062

### Integration {#integration-11}

* Custom at.js file does not publish when accessed with the anonymous user. NPR-19542: Hotfix for CQ-4219592
* Migrating Analytics existing credentials to WSSE Authentication. NPR-19962

### Brand Portal {#brand-portal}

* Enabling publish tags from AEM to Brand Portal from tagadmin/tagging console. NPR-20271

## Forms {#forms-11}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-11}

#### Correspondence Management {#correspondence-management-4}

* Enabled functionality to search for actual text in document fragments when a letter is previewed. NPR-19712

#### Adaptive Forms {#adaptive-forms-8}

* Enhanced Adaptive Forms to attach PDF as attachments in Safari. To support same capability in existing forms, we need to make the change in configuration in attachment widget and in "Supported file types" update the value application/pdf instead of .pdf. NPR-19623

#### Forms Manager {#forms-manager-1}

* If validationState is undefined on a field of adaptive form and elementFocusChanged event occurs, then an error event (errorState) is returned to Adobe Analytics server. NPR-19513

### Forms JEE Installer {#forms-jee-installer-11}

#### Core {#core-3}

* Connection manager is not available during shutdown. Jboss cuts off the JDBC dependency prior to the author EAR being undeployed causing corruption issues. NPR-19703

## Feature Packs included {#feature-packs-included-1}

* Thumbnail correction and transparency improvements in Dynamic Media. NPR-15207

## OSGI bundles and content packages included in CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

List of content packages updated in AEM 6.2SP1-CFP9

[Get File](assets/content_package-list62sp1-cfp9.txt)

List of OSGi bundles updated in AEM 6.2SP1-CFP9

[Get File](assets/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Introducing tags to custom user templates on Adobe Email Template Service.
* TouchUI buttons enhancements to Desktop app.
* Disabled submit button on click to prevent multiple form submits on a translation page.
* Configured multiple RTE components in a dialog.
* Reinforced ReferenceUpdates in live copy.
* Enabled case-sensitive search functionality for document fragment content.
* Added list of Linux libraries to AEM Forms installation documentation.

### Assets {#assets-11}

* Issues with applying the Omnisearch Filter on smart collections on Safari browser. NPR-19511
* PDF keyword metadata is not properly extracted and modified incorrectly when there are multiple keywords associated with a PDF Asset. To resolve the issue, the Subject field metadata property has been removed for PDF Assets. However, you can edit the metadata schema to add a multi-value text field for the Subject field. NPR-19126
* The workflow notification service doesn't encode the links in email which prevents them to load after users click them. NPR-19490: Hotfix for CQ-4218055
* Unable to load complete list of pages/assets in Column view using Chrome. NPR-19458: Hotfix for CQ-4214248
* Incorrect Off time icon is displayed in AEM inbox when activating "Request for Activation" workflow. NPR-19365: CQ-4216174  
* Issues with sorting in list view. NPR-19217: CQ-95602
* When changing the title or thumbnail picture in Asset Folder settings, the original group and permissions of the folder are overridden. NPR-19283: Hotfix for CQ-4216080
* Windows 10 workstations automatically switch to Touch Mode disabling some of the buttons from functioning. NPR-19183

### Sites {#sites-11}

* Issues with having Multiple RTE components in a dialog. NPR-19311: NPR-19587
* Automatic version purge in vanilla AEM 6.2 only works once after the VersionManagerImpl is initialized. NPR-19315: Hotfix for CQ-4217175
* Workflow instance gets stuck on "Salesforce.com Export" workflow step. NPR-19222: Hotfix for CQ-4212976
* Language copies pages created from live copies are not editable. NPR-18967
* ReferencesUpdateAction fails to update Links into a nested LiveCopy with hierarchy change. NPR-18715: Hotfix for CQ-4214105

### Platform {#platform-9}

* The Adobe Email Template service adds tags to custom user templates. NPR-19190: Hotfix for CQ-4217113

### Projects {#projects-2}

* Project editors unable to copy/paste assets into the project asset folder. NPR-19619
* Unable to generate preview for Translation projects after installing 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integration {#integration-12}

* Access properties for articles getting incorrectly set in Adobe Digital Publishing Solution on Classic UI. NPR-19366
* Sluggish rendering of thumbnails due to full-size articles in AEM Article console. NPR-19086: CQ-4217148
* Incorrect behavior of auto-folding when personalizing offers through Campaign if users have access to multiple areas. NPR-19290: Hotfix for CQ-4218029
* Targeting dialog not displayed in targeting mode when a target module is edited and save more than once. NPR-19144: Hotfix for CQ-4216708

### Workflow {#workflow-2}

* Users unable to filter notifications in Inbox by user/group in Inbox Classic UI. NPR-19122: Hotfix for CQ-4215374
* Image Map does not retain selected coordinates in HTL image component. NPR-18911: CQ-4211584

## Forms {#forms-12}

* AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-12}

* When content is copied from Microsoft Word or a Web Browser to correspondence manager text editor, the style is lost. NPR-19530
* Content without line break-in Text Editor does not wrap. NPR-19481  
* Enabled functionality to search for actual text in document fragments when a letter is previewed. NPR-17792: Hotfix for CQ-4214501

#### Correspondence Management {#correspondence-management-5}

>[!NOTE]
>
>This search functionality for text fragments has some constraints:-
>
>* Document fragment content are case-sensitive and titles are not case-sensitive.  
>* Search results are not highlighted when part of the searched word is in different styling or contains special character like " or ' or \.
>* Search does not work for dynamic content(like Data dictionary element values or variable values) within the document fragment.

#### Forms Manager {#forms-manager-2}

* XML Schema properties of Adaptive Forms cannot be edited after applying CFP6 on AEM 6.2. Hotfix for CQ-4219684
* All services of AEM Forms Manager core bundle are not started on restarting the server. Hotfix for CQ-4217014

### Forms JEE Installer {#forms-jee-installer-12}

#### Install LCM {#install-lcm-2}

* Administrator screen on Microsoft windows displays version number 6.0 after installing CFP6. Hotfix for CQ-4217573

## Feature Packs included {#feature-packs-included-2}

* TouchUI buttons enhancements to Desktop app. NPR-18676

## OSGi bundles included in CFP8 {#osgi-bundles-included-in-cfp}

List of OSGi bundles updated in AEM 6.2SP1-CFP8

[Get File](assets/updated-bundles-list-cfp8.txt)

List of content packages updated in AEM 6.2SP1-CFP8

[Get File](assets/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Behavior change in displaying titles on Image card for Image having dc: title property set to String [] (multifield).
* Fixes in Performance Issue with Dynamic Media Cloud Services, Touch UI & Security UI interfaces.
* Fixes in Apache Felix Http Bridge 3.0.8
* Resolved Binaryless replication(BLR) b/w author & publish environment.
* Support for target Library file, AT.JS, an implementation library for client-side integration with Adobe Target designed for both typical web implementations and single-page applications.
* Improved AEM performance by introducing user configurable connection timeout period for Marketing Cloud solutions (Analytics, DTM, Target and S&P).

### Assets {#assets-12}

* While testing video ingestion with AEM 6.3 configured with Dynamic Media Cloud Services, "Too many open files" exception is caused. NPR-18734; Hotfix for CQ-4211407
* Vanity URL setting for assets on a page does not work after restarting the AEM instance. NPR-18634; Hotfix for Granite-18085
* In TouchUI, the Publish button is displayed for users without permission to publish assets. NPR-18620; Hotfix for CQ-4214042
* The dynamic rendition option is not present in the download dialog box for an asset once the license agreement is set for it. NPR-18607; Hotfix for CQ-4212342
* Dynamic rendition cannot be downloaded for assets that include spaces in their names. NPR-18571; Hotfix for CQ-4211738
* Unable to save more than one user when sharing the asset folder with creative cloud. NPR-18489; Hotfix for CQ-103297  
* dc: title & dc: description does not change to a multi-field value in crx/de. NPR-18474; Hotfix for CQ-4209086  
* Move assets operation causes performance degradation. NPR-18346  
* No items are displayed in the Timeline when it is opened with the default Show All option set. NPR-18302; Hotfix for CQ-4211957
* An error occurs when an ASCII/UTF-8 encoded text file is uploaded to AEM Assets and thumbnail generation fails. NPR-18006: CFP for CQ-4209345  
* Publish action buttons are visible even when user doesn't have the replicate access. NPR-17353; Hotfix for CQ-4209269  
* Both Siteadmin and Miscadmin do not work when minification is enabled using min:gcc;obfuscate=true. NPR-18593; Hotfix for CQ-4209220
* Custom menu items don’t appear until the screen is refreshed every time. NPR-18500; Hotfix for CQ-4213581
* Upgrade moment.js to 2.10.6. NPR-18596; Hotfix for Granite-11881  
* Applying permissions for DM macros breaks view for Admin user. NPR-18544; Hotfix for CQ-4211729
* Publish Later for assets is throwing Illegal ArgumentException. CQ-4214532

### Sites {#sites-12}

* On an active-active author cluster with MongoDB, both the authors attempt to trigger replication for the same content, when the time reaches On-time set for the content. NPR-18708; Hotfix for CQ-4210982
* NPE when moving a resource with a reference that has no jcr: content node. NPR-18664
* Placeholders are not visible in a page that contains multiple parsys components. NPR-18645; Hotfix for CQ-110253
* Concurrency Issues in AbstractCopyMoveCommand. NPR-18591  
* When copying text to a parsys component from another AEM instance, the parsys is created without any resourceType set. NPR-18511; Hotfix for CQ-4212306

### Platform {#platform-10}

* JCR Installer doesn't update bundle version after Package Installation. NPR-18728; Hotfix for NPR-15135
* Binaryless replication(BLR) fails with binaries b/w author & publish environment. NPR-18704
* Apache Felix Http Bridge resolution request in AEM environment. NPR-18297
* Replication fails when multiple pages having a similar structure are replicated simultaneously with Sling Content Distribution. NPR-18665; Hotfix for Granite-13712
* Sling distribution packages building up and not self-cleaned. NPR-18601; Hotfix for Granite-16183

### Integration {#integration-13}

* Viewing offers published from library folders result in NPE. NPR-18732; Hotfix for CQ-4214593
* The start/end date for an activity is not updated in JCR and Target when changed from a specific date to "When activated/deactivated." NPR-18612; Hotfix for CQ-104831
* The Analytics integration with AEM has no connect or socket timeouts set for the httpclient connections. NPR-18497
* The DTM integration with AEM has no connect or socket timeouts set for the httpclient connections. NPR-18495
* The Target integration with AEM has no connect or socket timeouts set for the httpclient connections. NPR-18494
* The Search & Promote integration with AEM has no connect or socket timeouts set for the httpclient connections. NPR-18493
* Target activity gets deactivated after adding an extra experience. NPR-18227; Hotfix for CQ-4201895

### WCM-Foundation Components {#wcm-foundation-components-7}

* Image maps do not retain selected co-ordinates in HTL image component. NPR-18530; Hotfix for CQ-4211584

### Translation {#translation-5}

* Translation search results doesn't include names of translation projects. NPR-18224; Hotfix for CQ-4210658

### Brand Portal {#brand-portal-1}

* Enabling publish tags from AEM to Brand Portal from tagadmin/tagging console. CQ-4212165

## Forms {#forms-13}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-13}

#### Correspondence Management {#correspondence-management-6}

* Correct data does not get displayed in the edit panel until the fragment is saved. NPR-19092
* Adding document fragment to a letter takes substantial time. NPR-18958
* If an XML declaration exists in a data xml file and letter rendition is initiated through a POST request, corresponding letter fails to display data. NPR-18870
* No audit logs are generated for actions taken on CM assets. NPR-16618

>[!NOTE]
>
>Do not install this CFP Add-on Package if you are impacted with the below two issues:
>
>* Copy Paste from Word / Web into CM Text Editor shows line break-in content. NPR-19530
>* Content without line break in CM Text Editor does not wrap. NPR-19449
>
>These would be addressed in future CFP.

#### Adaptive Forms {#adaptive-forms-9}

* On adding a new panel for repeatable panels, value of the drop-down field in the previous panel is deleted. NPR-18772
* Adaptive form fields marked to accept only integers also accept a few special characters from the numeric pad. NPR-18680
* Script to change the button title at initialize event of guideroot panel is not working. NPR-18476  
* Scroll bar is not seen in right panel for rules created under rule editor. NPR-18716

#### AEM Forms App {#aem-forms-app}

* Forms do not render properly in AEM Forms App when it is in offline mode or not connected to the network. CQ-4218368

### Forms JEE Installer  {#forms-jee-installer-13}

#### PDFG Service {#pdfg-service-3}

* PDF Generator fails to produce PDF documents with specified bookmarks levels. Hotfix for CQ-4211102

## OSGi bundles included in CFP7 {#osgi-bundles-included-in-cfp-1}

List of OSGi bundles updated in AEM 6.2SP1-CFP7

[Get File](assets/bundle-list-6_2sp1cfp7.txt)

List of content packages updated in AEM 6.2SP1-CFP7

[Get File](assets/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Efficient management of hidden components in layout mode in tablet.
* Introducing Quickactions on Hybrid Devices.
* Resolving component level synchronization issues with live copies.

### Assets {#assets-13}

* Customer gets blocked when user who does not have the required permission tries to move operation on an asset. NPR-18330; Hotfix for CQ-4212560
* Merging multiple smart content services configurations cause usability issue. NPR-18273; Hotfix for CQ-4201557
* Checkout action/Workflows are not available from Timeline console once approx. 80 fragments are added in Assets folder. NPR-18257; Hotfix for CQ-4211214 and NPR-18251; Hotfix for CQ-4211216. 
* System crashes in Out of Memory & lacks pagination during Assets reports. NPR-17865; Hotfix for CQ-4209759
* The published video fails to playback on encoded Video Asset. NPR-17849; Hotfix for CQ-4210739
* Thumbnail for PDF is not generated. NPR-17831, NPR-17750; Hotfix for CQ-4210547
* Expired assets are not deactivated by Adobe CQ DAM Expiry Notification job. NPR-17666; Hotfix for CQ-107766
* Assets expiration activities stop if an asset does not have an assigned owner. NPR-17665; Hotfix for CQ-4197946
* A null pointer exception is raised when an asset folder with more than 150 incoming references is moved. CQ-4200981

### Sites {#sites-13}

* Personalization works only for the first IP when segmentation rule is set for an IP range. NPR-18121; Hotfix for CQ-83767
* Login fails due to NumberFormatException when historyShow property is enabled. NPR-18073; Hotfix for CQ-101965
* Deleted pages marked are visible in Touch UI. NPR-18025; Hotfix for CQ-86694
* Performance issues when loading a page with large (2000+) audiences. NPR-17884; Hotfix for CQ-4209567
* Cannot select an image after removing another images on the page. NPR-17711; Hotfix for CQ-4201323

### Platform {#platform-11}

* Touch UI controls are not hidden for users who do not have the required permissions. NPR-17945; Hotfix for CQ-4211231
* Japanese tags missing on tagpicker field. NPR-17768; Hotfix for CQ-4210456
* The getsize() query returns incorrect results when FastQuerySize is enabled. NPR-18018
* Web console on the standby instance is not accessible. NPR-17861; Hotfix for Granite-14582

### Commerce {#commerce-2}

* Query traversal happens when catalog blueprint does not have any condition defined for a section. NPR-18229; Hotfix for CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. delays AEM shutdown. NPR-18298; Hotfix for CQ-96133

### Integrations {#integrations}

* Resolved AEM Search component errors that can occur when AEM Day HTTP Client 3.1 OSGI is configured with a Proxy that requires Digest Authentication. NPR 18128  
* Checkbox missing to revert inheritance. NPR-17753; Hotfix request for CQ-4210139
* Users are not able to set up the priority when targeting one component with multiple activities. NPR-18658; Hotfix for CQ-4210727
* Users are not able to browse the folder /etc/segmentation to select an audience created under the folder /etc/segmentation/group1. NPR-18522

### Security {#security-1}

* The Move Asset wizard hangs if the user does not have write permission on the target folder. NPR-18300
* Request to use an upgraded version of org.apache.sling.servlets.post servelet (2.3.22) in Apache Sling API to pre-empt an XSS vulnerability. NPR-18963

### Translation {#translation-6}

* Asset page should not be allowed to be submitted again to a translation project until the project completes. NPR-18249; Hotfix for CQ-4209908

### WCM-Foundation Components {#wcm-foundation-components-8}

* Unable to use WCM foundation iparsys component in editable templates. NPR-18223; Hotfix for CQ-4210384
* Image Map does not retain selected coordinates in HTL image component. NPR-18032; Hotfix for CQ-4211584
* When an HTL image component renders, the filename in the URL is renamed causing broken URL. NPR-17908; Hotfix for CQ-4211587
* Unable to exit from Page Properties after making changes. NPR-17832; Hotfix for CQ-96110

## Forms {#forms-14}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-14}

**Correspondence Management**

* Data Dictionary gets repeatedly read during letter render. NPR-18482, Hotfix for CQ-4210805
* Added JavaDocs for the com.adobe.livecycle.content class. NPR-18467  
* On creating a letter, description of the letter is not saved. NPR-18039  
* When a text module is saved and an expression in the text module does not contain opening or closing expression tags, no error message is displayed. The text module displays an error message and fails to render in the letter. NPR-17798  
* Unexpected errors seen in logs on installation of add-on package. NPR-18295

**Forms Manager**

* AEM Forms UI lists all the assets in the oldest first order. Users are not able to reorder the assets in newest first order. NPR-18451

### Forms JEE Installer  {#forms-jee-installer-14}

**Output Service**

* Improved performance issue of Output service for AEM forms 6.2. NPR-18033

**Signatures Service**

* Unable to sign a PDF document with remote Hardware Security Module. NPR-18017

## OSGi bundles included in CFP6 {#osgi-bundles-included-in-cfp-2}

List of OSGi bundles updated in AEM 6.2SP1-CFP6

[Get File](assets/6.2sp1-cfp6-bundlelist.txt)

List of content packages updated in AEM 6.2SP1-CFP6

[Get File](assets/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Resolved several UI issues with sharing, moving, publishing and downloading assets.
* Increased capacity of the Move dialog in displaying referenced assets.
* Resolved several issues around WCM components and workflows, such as Unpublish and Version Purge.
* Improved responsiveness of the action bar with respect to displaying toolbar actions and Coral components.

### Assets {#assets-14}

* Performance improvements in the publish to Brand Portal functionality. NPR-17189; Hotfix for CQ-4204150
* Sharing an asset using the Share Link option does not create a zip file with a flat folder structure for download. NPR-17513; Hotfix for CQ-4209381
* Selecting an asset in DAM and clicking Publish does not display the Publish to Brand Portal option in the Asset details page. NPR-17351; Hotfix for CQ-94905
* In DAM workflow steps, binary streams acquired from Session or ResourceResolver must be closed in a final block to ensure that resource leaks do not occur. NPR-17385; Hotfix for CQ-4209452
* Uploading a Word doc in DAM results in a null pointer exception and the workflow instance remains stuck in the Running state. NPR-17160; Hotfix for CQ-4207358
* The Share, Move, Publish, and Download buttons are visible for expired assets on the Metadata Editor page for non-admin users. NPR-16903; Hotfix for CQ-101440/CQ-104535
* Actions such as Share, Move, Publish, and Copy should be visible for administrative users in the Assets console. NPR-16902; Hotfix for CQ-4207111

### Sites {#sites-14}

* While moving a page using either Classic and Touch UI, the Move dialog does not show references beyond 150, making users unable to update these references and republish the page. This issue has been fixed by introducing a property for Classic UI: 'maxRefNo' which can be configured on the siteadmin node: '/libs/wcm/core/content/siteadmin'. This property specifies maximum number of references (default value 150) that is displayed before a heavy move operation and if a page has more number of references, they are not shown in the movePage dialog. This configuration also works for damadmin and miscadmin by applying configuration on the nodes: `'/libs/wcm/core/content/damadmin'` and `'/libs/wcm/core/content/miscadmin'` respectively. NPR-17222; Hotfix for CQ-85878

* While working with WCM components, hyperlinks with spaces are removed in the Touch UI Rich Text Editor. NPR-17698, NPR-17570; Hotfix for CQ-4206768
* While triggering the Request for Unpublication workflow from page properties, JavaScript errors appear for users without replication rights. NPR-17294; Hotfix for CQ-102064
* Rendering or exporting an HTL image component changes the URL to a number, renaming the file name, which causes broken links. NPR-17245; Hotfix for CQ-59616
* Deleting a launch in a nested launch causes sub-launches to become orphaned. NPR-17228; Hotfix for CQ-4202639
* Running Version Purge in AEM 6.2 with Oak 1.4.13 applied causes a constantly repeated warning in the logs. NPR-17391; Hotfix for CQ-4206870
* After installing a hotfix or an upgrade for the ContextHub component, the content package overwrites all segments in /etc/segmentation/contexthub, resulting in a loss of all custom ContextHub segments. NPR-17250; Hotfix for CQ-79958
* While running a workflow with nested groups as workflow users, the WorkflowStatusProvider (pageinfo.json) causes the workflow instance to lock up. NPR-17555; Hotfix for CQ-4202056
* While using the WCM-Page editor components, a huge amount of empty space exists at the end of the page in the Touch UI edit mode of the author instance. NPR-17510; Hotfix for CQ-4205441
* Rendering or exporting an HTL image component changes the URL to a number, which causes broken links. NPR-17245; Hotfix for CQ-59616

### UI {#ui}

* Selecting an asset and clicking Developer Tools does not always display the toolbar actions in the action bar in slow connections and the page has to be reloaded. NPR-17568; Hotfix for CQ-108365
* The action bar should be updated to use two containers: coral-actionbar-primary and coral-actionbar-secondary, instead of the coral-actionbar-container. NPR-17591; Hotfix for GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Users with 'Read Only' permissions to the AEM Mobile app cannot preview contents from AEM Mobile Content Management page. NPR-17390; Hotfix for CQ-4209690

### Security {#security-2}

* XSS vulnerability in the output generated by HTMLRendererServlet. NPR-17136
* Request to prevent AEM version disclosure in AEM Web Syndication Feeds page. NPR-16219

### Forms {#forms-15}

#### Forms add-on package {#forms-add-on-package-15}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

**Adaptive Forms**

* For an adaptive form with attachment, duplicate entries for the afSubmissionInfo tags are created in the submitted XML when the form is submitted for the second time. NPR-17364 
* While using the Google Chrome browser, after removing an attachment from a form, trying to re-attach the same attachment again throws an error. NPR-17297
* In case there are nested, repeatable lazy loaded panels in XSD-based or No-Form-model-based Adaptive Forms, values filled in the form are not retained in the Document of Record (DOR). NPR-17176
* Errors displayed in the error log for the Rule Editor should be added in the catch block of a try/catch block JavaScript code. NPR-16757 
* Clicking a file attachment in a form throws a browser console error and does not display the attachment preview. NPR-17174

**Correspondence Management**

* The Create Correspondence UI functionality breaks in case inline text or a blank line is added in the UI. NPR-17748 
* The browser flickers when a letter is opened for editing. NPR-17576 
* While adding remote functions in computed data dictionary elements, if the number of functions are more than the length of the tab showing remote functions, the scroll bar does not appear in the tab. NPR-17359 
* The API method, import com.adobe.icc.services.api.LetterInstanceService does not work. NPR-17922, NPR-16008
* A variable added in a text module is not visible in the Data Binding panel while editing a letter. NPR-17940
* The Correspondence Management UI does not launch when HTML submit action uses the POST method. NPR-17595

**Forms Manager**

* With an adaptive form configured for AB testing, clicking Start AB Testing does not start the test and throws a browser console error. NPR-17838

**Forms Service**

* The issues reported in the static code analysis of OSGI forms should be fixed. NPR-13951

#### Forms JEE Installer {#forms-jee-installer-15}

**Output Service**

* Using AEM forms 6.2 Output Service to merge a specific form with a data XML takes 20 times more time as compared to the time taken by LiveCycle ES4 SP1 server for the same operation. It is fixed on Windows and Linux environments. NPR-17501

**Install LCM**

* After installing AEM Forms 6.2 GM build and applying the AEM 6.2 CFP, running LiveCycle Configuration Manager displays an unwanted semicolon in the Version Information and the patch installation date is not updated. NPR-14322

**Process Management**

* The TaskContext variable is not populated for AEM Forms processes. CQ-4211857

#### AEM Forms JEE Bundles Package {#aem-forms-jee-bundles-package}

* The capabilities of forms users, whether using the JEE admin UI console or the OSGi console should be the same. NPR-17670

### Feature Packs included in CFP5 {#feature-packs-included-in-cfp}

**Forms JEE Package**

Process Management -HTML Workspace

* While assigning a workspace step, the workspace attachments tab should show a counter for the attachments or notes in case there is more than one attachment or note. NPR-17771 
* Request to support Office 365 in AEM JEE Forms for email capabilities in the form workflow. NPR-13866

**Forms Add-on Package**

Correspondence Management

* While editing fragments in the text editor during a letter preview, the processed text should be shown for editing instead of the inline conditions used in fragments. NPR-15748, NPR-17504

### OSGi bundles included in CFP5 {#osgi-bundles-included-in-cfp-3}

List of OSGi bundles updated between AEM6.2 SP1-CFP5

[Get File](assets/cfp5_osgi_bundles.txt)

List of content packages updated between AEM6.2 SP1-CFP5

[Get File](assets/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4 is an important update that includes key customer fixes released since the general availability of AEM 6.2 SP1.

The key highlights of this Cumulative Fix Pack are:

* Fixes in assets for Camera Raw file rendition, timeline view, and image orientation
* Improvement in

  * WCM launches for sites
  * Projects workflow
  * ContextHub components

* Fixes for Campaign, Mobile on-demand, and Translation
* Usability improvements in Adaptive forms Rule Editor
* Enhanced Inline Condition Editor for Correspondence Management in forms
* Process management and output service fixes for AEM forms on JEE 
* Forms Designer related fix for Script Editor

### Platform {#platform-12}

* The Search&Promote search form ignores the `environment` setting when the cloud service is configured, making it unusable on the author instance. NPR-16594: Hotfix for CQ-4206076
* Adding or customizing columns to the **Assets OmniSearch** results by overlaying in /apps does not work. NPR-16737: Hotfix for CQ-4206785
* The **Diagnosis tool **page does not work after an in-place upgrade from AEM 6.1 SP2 to AEM 6.2 SP1. NPR-17121; Hotfix for CQ-4196786
* HTL: While selecting a Forum, creating a Topic and a Post, the `Sightly SightlyCompiledScript` adds incorrect `addSelectors` property to `RequestDispatcherOption`. NPR-17008: Hotfix for GRANITE-16384

* Added support for `CRON expressions` in `ManagedPollConfigs` used by the `ReportImporter`. NPR-16608: Hotfix request for CQ-4206066  

* Uploading an avatar image for an LDAP user fails. NPR-16561; Hotfix for Granite-17013
* Number of results displayed on User Management screen is different in Card and List view. NPR-16241; Hotfix for GRANITE-16914  
* Workflow notifications fail to be lazy loaded while viewing in the Google Chrome browser in Full Screen mode. NPR-17013: Hotfix for CQ-4207567

### Assets {#assets-15}

* The image orientation is not correctly applied while importing an image with a defined orientation. NPR-16750: Hotfix for CQ-4204356 
* The Assets Timeline view does not display any asset even though 'Show All' is set by default. NPR-16957: Hotfix for CQ-98780
* Camera raw files (including ARW, CR2, NEF, DNG, and EPS) when added as rendition in assets, cannot be selected or deleted. Such files are automatically downloaded when user clicks them. NPR-16949: Hotfix for CQ-4206846
* Creating a pdf inside another pdf in Assets UI does not display the created pdfs in the DAM UI though these are visible in the crx repository. NPR-16833: Hotfix for CQ-4206501
* Uploading an asset as a direct child node of itself using the Touch UI causes an issue. The asset is uploaded as a direct child of the previously selected asset. NPR-16534: Hotfix for CQ-4204287
* In the DAM UI, commenting on an asset and tagging a user in the comment does not generate a mail notification. NPR-16589: Hotfix for CQ-102318

### Projects {#projects-3}

The Projects workflow console shows a NullPointerException on page when workflows are purged. NPR-17017: Hotfix for CQ-4194269

### Sites {#sites-15}

* Files in the `ContextHub` are not minimized on the author instance. NPR-17022: Hotfix for CQ-79456
* The WCM-Launches launch promotion takes long time for promoting a launch that consists of a large tree of a page. NPR-16480: Hotfix for CQ-82731
* `ClientContext` Segment Condition Renderer crashes when a segment (or audience) is created with a non-working or unfinished rule. NPR-16759: Hotfix for CQ-4205104
* In WCM Launches, pages associated with a Launch are not unpublished when the action is initiated from within the page properties in the Touch UI. NPR-16560: Hotfix for CQ-4204681
* Link Rewriter falsely rewrites href values containing a colon assuming that the colon ":"defines a JCR namespace. NPR-16753: Hotfix for CQ-4203762
* In WCM-Design Importer, opening a test importer page and trying to upload a zip file causes issues if it has been uploaded and deleted previously. NPR-16486: Hotfix for CQ-90962
* Navigating to the **[!UICONTROL Global Navigation]** pane using the Firefox Safari and Google Chrome browsers provides different user experience. The Firefox browser displays the **[!UICONTROL Tools]** menu whereas the Google Chrome browser shows the **[!UICONTROL Navigation]** menu. NPR-16770; Hotfix for CQ-4200456

### Campaign {#campaign}

* While testing AEM campaign templates and modifying seed addresses to include 'Additional Data', the Adobe Campaign drop-down disappears in the Touch UI Context Hub. NPR-16771: Hotfix for CQ-105748

### Mobile on-demand {#mobile-on-demand-3}

* When Preflighting a publication from the AEM author environment, a Preflight action taking longer than 5 seconds causes an unusual spike on the AEMM - AEM PECS Integration splunk dashboard with high number of status requests per second. NPR-16908: Hotfix for CQ-4207055
* The AEM Mobile configuration management fails after installing the AEM-6.2-SP1-CFP1-1.0 update. NPR-16909: Hotfix for CQ-4204892

### Translation {#translation-7}

* Previewing translation jobs does not work after installing 6.2 SP1 - CFP1. NPR-16481; Hotfix for CQ-4204655
* The language copy created using Translation points to the Root Master instead of the local country livecopy. NPR-17257; Hotfix for CQ-4208287

### Security {#security-3}

* No MIME type validation is performed when binaries of files are uploaded to AEM. NPR-16617
* Issues with uploading avatar images for LDAP users. NPR-16561

### Forms {#forms-16}

#### Forms add-on package {#forms-add-on-package-16}

**Adaptive Forms**

* In Adaptive Forms Editor, the Target Setting comment in head.jsp should be replaced with the new Context Hub statement. NPR-17173  
* In the Adaptive Forms Rule Editor, the **[!UICONTROL Choose an Item]** shows the event as 'null'. NPR-17139
* Submitted form gets resubmitted on navigating forward using the forward arrow (&gt;). NPR-17080  
* While submitting an Adaptive Form via AJAX, the 'error' callback function is never invoked in case of an error. NPR-17034
* Clicking the **[!UICONTROL Save Form]** button in Rule Editor at run time does not save the form. NPR-16905  
* Static text should be excluded from tabbing order in Adaptive form. NPR-16749  
* The calculated value of a decimal field appears incorrectly. NPR-16596  
* The icon for displaying Help content should be included in the tabbing order in Adaptive forms. NPR-16484
* Support for use of regular expression of type `dataRef=C:/Users/`in the ' **[!UICONTROL Default Prefill Service Configuration]**' for Prefill of data for Adaptive Forms. NPR-16425  

* Validations are not triggered correctly for all the panels if there is nested lazy loaded scenario. NPR-15821

**Correspondence Management**

* Letter rendition fails if a letter contains a blank text module (one with no text). NPR-17054  
* Line breaks and tab spaces get removed from content after being pasted in Text Editor. NPR-17039  
* The display of references of a text module takes much time if the text module is referenced in many letters. NPR-17035
* Editing, saving, deleting, and setting reference for document fragments takes much time. NPR-17033  
* Justified text is rendered in a different font when previewing the letter. NPR-16976
* Search functionality does not work properly if the searched text has multiple occurrences. NPR-16920  
* The Text Editor toolbar is displayed in the browser intermittently. NPR-16919  
* The **[!UICONTROL Save Form]** construct from Rule Editor does not work. NPR-16905
* The Font drop-down does not populate the Font family on creating a Text Module based on Data Dictionary using Internet Explorer. NPR-16944
* After creating a text fragment, the letter font changes on previewing the letter. NPR-16830  
* Letters with tab spaces in the beginning or in between expressions in the document fragment cannot be rendered or previewed. NPR-16769

**Mobile Forms**

* Mobile Form preview shows overlapped content, though the form is displayed correctly for PDF rendering. NPR-17105

**Forms Portal**

* Clicking the **[!UICONTROL Download]** link for a submitted form opens an HTML page instead of a PDF form. NPR-17082  

* `Upload Comments` for file attachment are not displayed in the UI for submitted instances, although they are present in the XML stored in the crx repository. NPR-17075

**Reader Extensions Service**

* A specific file is not Reader Extended on AEM forms OSGI installation. NPR-16625

#### Forms JEE Installer  {#forms-jee-installer-16}

**Core**

* During upgrade process, Configuration Manager fails with timeout. NPR-16774 (See [Configuring timeout for operations at component level](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Process Management - HTML Workspace**

* The startpoint from a Start Task does not begin with the data submitted at the time of startpoint submission. NPR- 16917
* Clicking the **[!UICONTROL Return]** button for a form in the HTML Workspace does not close the form, but returns it to its Group Queue.  
  NPR-16352

**Process Management**

* Allow users to set the display name of previous tasks to any of the next tasks in a process instance. NPR-15382

**Output Service**

* Output Service fails to process a PDF which is modified to include an additional 'milli-sec' field in the `date-time format` metadata. NPR-16838

#### Forms Designer {#forms-designer}

* AEM Designer Script Editor does not respect the Form Properties defaults for `Calculate Event`and `Validate Event`. NPR-15921

### Feature Packs included in CFP4 {#feature-packs-included-in-cfp-1}

**Forms Add-on Package**

* Enhancement in the Inline Condition Editor for Correspondence Management. NPR-10981

### OSGi bundles included in CFP4 {#osgi-bundles-included-in-cfp-4}

List of OSGi bundles updated between AEM 6.2 SP1 and CFP4

The key highlights of CFP3 are:

* More efficient search capability for Classic UI and for the AEM Search component using proxy with digest authentication
* Fixes problems while uploading assets and display of asset metadata
* Fixes issues while creating folders and moving pages in case the title has special characters.
* Fixes for using targeting- syncing audiences, publishing campaigns, and selecting Goal Metric in the Touch UI
* Resolves sync issues for translation jobs
* Provides enhanced security for Forms prefill service
* Improvements in forms portal draft and submissions component and in the Barcoded Forms Service
* Usability improvements for adaptive forms containing file attachment widgets or lazy loaded fragments. 
* Usability improvements in Correspondence Management including enhanced search capability, logging of deleted assets, and importing data dictionaries.

### Platform {#platform-13}

* A race condition in the **ModelAdapterFactory**, which is possible when two threads try to inject the same field, results in failure to construct the model. NPR-16443: Hotfix for SLING-6584
* Validation option in package manager to detect any conflicts between overlaid file (JSP or JavaScript file) under /apps and the one that contained in a Hotfix under /libs. Affected overlay can then be rebased to include changes from the file under /libs . NPR-16216: Hotfix for CQ-81729
* Logging in the error.log sometimes stops a few seconds after starting the publisher and needs to be cleared to run again. Request to update the logging framework and provide Sling logging. NPR-15913: Hotfix for Granite-15452
* Request to update the JavaScript " `use"` API to avoid failure in the HTL Javascript Use API implementation. NPR-16461: Hotfix for SLING-6780

### Sites {#sites-16}

* After upgrading from AEM 6.0 to AEM 6.2, the Classic UI shows slow performance while searching tags due to numerous queries. To resolve the issue, the steps mentioned under [Disable replication status in tagging console (classic UI)](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr) can be followed. NPR-15842: Hotfix for CQ-4201748.   

* While creating a page in the Touch UI, the Input check for 'name' field does not check the special character 'Apostrophe' (same as in the Classic UI). Therefore, the page cannot be moved. NPR-16404: Hotfix for CQ-4205321. 
* Applying different styles on two rows in Rich Text Editor and then merging them removes the style applied on the second row. NPR-16389: Hotfix for CQ-4203835.  
* In the Touch UI Sites screen, trying to paste a page inside a page having no subpages, does not work as the Paste button does not appear. NPR-15894: Hotfix for CQ-4201696.  
* While scrolling the Pages tab in Content Finder panel, a few sets of pages show indefinitely in the Classic UI whereas the Touch UI shows a limited set of few non-repeating pages. NPR-16271: Hotfix for CQ-4202371
* Opening the Page-Properties of a LiveCopy in Touch UI and clicking Save without any changes writes down any LiveCopy tab and creates a LiveSync Config node. NPR-16327: Hotfix for CQ-108562  
* Form constraint is not able to read the `ConstraintMessage` property. NPR-16388: Hotfix for CQ-101330
* The `wcm/foundation/components/parsys` component does not display the **[!UICONTROL 'Drag components here]**' placeholder. NPR: 16748: Hotfix for CQ-4205187

### Assets {#assets-16}

* The pdf rasterizer stops working and causes out of memory issues after installing 6.2 SP1 or Hotfix 12430. NPR-15991
* The metadata for a string property, `documentNumber` shows up as a date whereas it should be a number. NPR-16134: Hotfix for GRANITE-16916
* Text truncations in timeline event balloon. NPR-16226: Hotfix for CQ-85226
* On creating a folder under the content hierarchy with title having special characters, the encoded form of the special character is displayed. NPR-15935: Hotfix for CQ-4202987
* User cannot upload assets or create folders while navigating through assets due to inconsistent behavior displayed when using the 'Create' button. NPR-16410: Hotfix for CQ-4204793
* Unexpected errors are encountered while uploading shared HTML resources from the articles view in AEM Authoring. NPR-16133: Hotfix for AEMM-4155970

### Integration {#integration-14}

* When enabling proxy authentication with Digest authentication, the AEM Search component throws a ConcurrentModificationException. NPR-15309: Hotfix for CQ-4199191
* When creating a Target A/B Test Activity in AEM, the audience does not sync up to the Target and show 'no audiences'. NPR-16229: Hotfix for CQ-4204210
* After installing SP1+NPR-11577 v1.2, when choosing 'Use an Analytics Metric' for the Goal Metric while targeting in the TouchUI, the dropdown list of metrics never loads. NPR-16129: Hotfix for CQ-4204316
* When using targeting, publishing the campaign does not automatically publish the entire tree, including brand and the master. NPR-15855: Hotfix for CQ-94630

### Translation {#translation-8}

* The Sync Translation Job is not triggered automatically and AEM polling does not occur without poking the translation projects. NPR-15163: Hotfix for CQ-90856

### Forms {#forms-17}

#### Forms add-on package {#forms-add-on-package-17}

**Adaptive Forms**

* While saving an Adaptive Form with an attachment, the full path of the attachment is added in the `fileAttachment` tag of the generated XML, rather than the name of the attachment. NPR-16529
* In XDP-based adaptive forms, the `afData/afBoundData` wrapper is present in the submitted XML though even prefill XML does not have `afData/afBoundData` wrappers. NPR-16118

* Exponential notation in Number field: While using adaptive forms, if a number with a decimal fraction that exceeds ten characters in total is entered, the number turns into exponential notation in the submitted XML. NPR-16106
* For forms that contain both a file attachment component and a lazy loaded fragment, the submitted data xml does not contain the information for the file attachment component. NPR-16022
* For a lazy loaded repeatable panel that does not have a repeatable ancestor, repeatable children inside a second instance of the panel fail to repeat. NPR-15944
* When trying to save a fragment inside a fragment in form editor--the fragment model root does not populate the value of child fragment. NPR-15943
* While creating a checkbox with only one item and trying to show the checkbox title keeping the item title hidden, the create dictionary action throws an `ArrayIndexOutOfBoundException` if the item text is empty. The dictionary is not created and no error response is generated on the screen. NPR-15816
* For adaptive forms with file attachment widgets, some parts of the form get disabled after the attached file is previewed.  
  NPR: 16611  

* For file attachment widgets where multiple attachments are allowed, if a new form instance with an attachment is submitted on a widget having a previous attachment, an error code is displayed on opening the added attachment instead of the actual content. NPR-16258  
* Securing forms prefill service from unauthorized access through protocols such as `file://`, `http://`, and `ftp://`. Refer " [Configuring Prefill service using Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)." NPR-15414 

* Request to render the adaptive form in PDF format instead of HTML in the Verify step and append all attachments to the PDF, so that the printout displays the complete form. NPR-9011

**Correspondence Management**

* While working with text fragment in a letter in Preview/Edit mode, if text is converted to list, the whole letter functionality breaks and a JavaScript error is generated. NPR-16460
* Importing an XSD file to create a Data Dictionary in the Correspondence Management node fails as the browser becomes unresponsive every time the XSD is uploaded and the root node is selected. This issue is browser independent and does not appear in server logs. NPR-16452
* While previewing a letter using the Internet Explorer browser and trying to edit the font size of content, duplicate values are seen from 8 to 72 in the font size dropdown. NPR-16387
* In case a floating field appears as an input field from an XDP fragment, the field does not expand in the letter preview while using Internet Explorer browser. NPR-16367
* When trying to submit a letter directly from preview, the popup for the letter name is not displayed properly due to being hidden. NPR-16353
* Line spaces added while editing a letter are not reflected in the Preview window. For lists in text fragments, the PDF output does not show the correct spacing. NPR-16267
* While working on a text document fragment using Internet Explorer browser, trying to provide indentation to the text fails as the cursor does not allow text indentation. NPR-16128
* Adding or modifying a data dictionary to an existing text document fragment takes much time and user is not notified always. NPR-16102
* While previewing a letter which has scrollable content using the Internet Explorer browser, the browser scroll bar overlaps with the letter's scroll bar and the entire content cannot be viewed for fragments on the right side. NPR-16068
* While creating or editing text document fragments using Google Chrome browser, the color selection drop-down automatically pops up and cannot be removed. User needs to select list as type of data entry to be able to edit the fragment. NPR-16067
* While using Letterinstance API, the method `import com.adobe.icc.services.api.LetterInstanceService` does not work. NPR-16008
* Changing the date display formats to `locale=en_US; dateFormat=MMM dd,yyyy;` in the Asset Composer Configuration does not work as expected and the date format is displayed as junk characters. NPR-16007
* Data Linkage type in letters while re-authoring is shown as 'User' even if set differently earlier. NPR-16619

**Forms Portal**

* Upgrade scenarios for draft and submissions components do not work with database sample implementation. NPR: 16752

**Barcoded Forms Service (BCF)**

* The static code analysis of Barcoded Forms Service (BCF) reports issues. NPR-13855

#### Forms JEE Installer  {#forms-jee-installer-17}

**Process Management - HTML Workspace**

* Securing forms prefill service from unauthorized access through protocols such as "file://", "http://", and ftp://. For details, refer [Configuring Prefill Service using Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754). NPR-15434

**User Management **

* The SAML login screen shows improper version (6.1.0) on the AEM 6.2 server. NPR-13825
* With AEM Forms configured for Single Sign On (Kerberos) authentication, if user authentication fails while trying to log in, an error code '404' is returned. The user is redirected to the login site only after refreshing the page. NPR-15015

#### Forms Designer {#forms-designer-1}

* Changing the Form Locale to French (Canada) in the Dictionary Spell Check does not work in AEM Forms Designer.   
  NPR-15896

### Feature Packs included in CFP3 {#feature-packs-included-in-cfp-2}

**Forms Add-on Package**

* On deleting any asset in correspondence management, a warning message should be logged in the error.log file. NPR-13225
* Enhance the search functionality while previewing a letter in correspondence management, to enable searching text in the text fragment content, instead of searching only the letter title or label. NPR-16103

### OSGi bundles included in CFP3 {#osgi-bundles-included-in-cfp-5}

List of OSGi bundles updated between AEM 6.2 SP1 and CFP3

[Get File](assets/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
The key highlights of Cumulative Fix Pack 2 are:

* Stability fixes and performance improvements in AEM platform, including Sling framework and operations
* Improved assets management with several fixes for accessing, moving, searching, uploading, and publishing of assets
* Improved authoring and management of Sites with fixes in Content Fragments, Anchor plugin, Slideshow, and Context Hub components
* Several fixes in Touch UI including text editor, Omnisearch, and variant creation process
* Improved translation workflows; enhanced Microsoft connector for using new translation APIs for the Azure portal  
* Fixes in Projects and Campaign
* Improved authoring and management with fixes in adaptive forms, correspondence management, and form portal features
* Fixes in Forms JEE core, XTG, and HTML workspace components

### Platform {#platform-14}

* The `SlingPostProcessor` is triggered if the page directly referencing the Sling framework is edited. NPR-15754: Hotfix for CQ-104153  

* The value for tags with `tagBasePath` property are not fetched in the classic UI dialog while navigating to a page component. NPR-15543: Hotfix for CQ-4199950  

* While performing Sling operations, when you have a chunk named 'chunk_n_n-1' `SlingFileUpload handler.getLastChunk` runs into an endless loop with empty chunks. NPR-15455: Hotfix for SLING-5701  

* When an interface extends another interface, the injectable methods on the super interface are not injected correctly. NPR-15202: Hotfix for SLING- 5710  
* A potential null pointer exception is not prevented when making use of the `com.adobe.granite.infocollector.impl.FilesTraversal`function call. NPR-15169 Hotfix for CQ-4197640
* The workflow state is inconsistent for some secondary nodes and error is displayed while dispatching observation events for that node. NPR-15701: Hotfix for GRANITE-13786
* When user selects a node in CRXDE (for example, /content/dam/) and then the 'Access control' tab, making sure that an Access Control List exists, dragging and dropping some elements moves the elements other than the one selected. NPR-15696 Hotfix for GRANITE-16300
* Selecting a user from the drop-down list when trying to impersonate makes the entire user pop-up disappear. NPR-15774: HotFix for CQ-4201738/GRANITE-11895
* In Omnisearch, searching by tags with auto-populated suggestions does not work. NPR-15088: Hotfix for GRANITE-14426.  
  Note: This fix requires the Oak CFP 1.4.11 or higher.

### Mobile AEM Author {#mobile-aem-author}

* When using AEM Mobile and ContentSync packages with a hybrid application, AEM responds to a fetch request (with timestamps) made by the application with the oldest package, instead of the one requested by the application. NPR-15749: Hotfix for CQ-104153

### Sites {#sites-17}

* Modification status for Workflow Inbox in the WCM core does not change if user modifies a page after activating a workflow. NPR-15684: Hot fix for CQ-4196974  
* The Anchor plugin in Rich Text Editor for Touch UI generates non-compliant HTML5 when user clicks anchor icon and adds a name. It should add an 'id' attribute instead of 'name' attribute in the HTML5 tag for the anchor element. NPR-15650: Hotfix for CQ-89782  
* When a metadata schema with numerous fields is created and applied to the content fragment metadata, no scroll bar is created at the content Fragment metadata screen making the fields uneditable. NPR-15478: Hotfix for CQ-4202622  
* Editing `TagInput` field component does not show the previously configured values against the dialog fields. NPR-15464: HotFix for CQ-4200360  

* In Content Fragment editor UI, in case many variations of a Content Fragment are created, the side panel does not show the scroll bar to navigate all the variations. NPR-15445: HotFix for CQ-4199444
* When users are removed from direct groups, they get added to inherited groups. NPR-15400: Hotfix for CQ-98758  
* WCM-authoring: Touch UI author does not allow editing of pages that have commas in the name. NPR-15396: Hotfix for CQ-4199723
* While using the Touch UI for authoring, the function `Granite.author.editableHelper.doSelectParent` passes arguments in the wrong order leading to a JavaScript error. NPR-15349: Hotfix for CQ-4198594
* ContextHub segment displays the experience even if the opt-out cookie is present. NPR-15293: Hotfix for CQ-4198024
* The Slideshow component in the Classic UI cannot create slides or drag and drop images to create new slides. NPR-15281: Hotfix for CQ-4194164
* Users, regardless of permission, are shown the 'Create' options such as Create Page, Create Site, Create Live Copy, Create Launch, and Create Catalog menu items in the Site Admin console. NPR-15278: Hotfix for CQ-94436
* After installing AEM 6.2 Service Pack 1, the 'Include Subpages' slider stops working for page launches. NPR-15230: Hotfix for CQ-4198449
* Request to enhance Version Purge to fetch and process versions in blocks and also be able to use a specified path into a XPath query. NPR-15186: Hotfix for CQ-109205
* The Clear button is missing on the Page Properties thumbnail tab in Sites component. NPR-15143 Hotfix for CQ-4196997
* For a site that uses Live Copies, selecting the 'Live Copy' checkbox in the Columns pane in the siteadmin console does not display Live Copy status correctly and only HTML markup is shown. NPR-15108: Hotfix for CQ-97086  
* When editing Content Fragments, if the user clicks done ('√') for editing before getting the response of the Post, the edited content is not saved correctly. NPR-15014: Hotfix for CQ-4194095  
* Closing the Edit page during Timewarp mode and trying to reopen it from Siteadmin results in an error with status '500' instead of reopening the page. NPR-14965: Hotfix for CQ-109647:
* In the Digital Asset Manager (DAM) UI, the User Picker Find Authorizables search causes an 'Out of Memory' exception. NPR: 15307: HotFix for CQ-98542

### Assets {#assets-17}

* After searching an asset in Omnisearch, selecting an asset and trying to edit properties by clicking 'View Properties' and then the 'Save' button redirects users to a blank page. NPR-15900: Hotfix for CQ-4202372  
* Assets User interface does not respond to events. Selecting an asset and clicking 'Publish' or 'Renditions' does not result in any activity. NPR-15828: Hotfix for CQ-4202247  
* When publishing an asset from the Card view, the Card is not updated to reflect a published state unless the page is refreshed. NPR-15826: HotFix for CQ-102732  
* Cumulative Hotfix containing Assets Hotfixes. NPR-15225  
* If ampersand ('&') character is included in the name of an asset folder, the folder name is not correctly displayed when navigating to the asset. NPR-15775: Hotfix for CQ-4201735  
* Using ampersand ('&') character in the name of an asset file causes issues when accessing to its properties. NPR-15770: Hotfix for CQ-4201737  
* While navigating Assets and using the 'Column view' display mode, if user refreshes the page after selecting and clicking an asset, the asset details are displayed instead of the refreshed content. NPR-15768: Hotfix for CQ-4201727  
* PDS ingestion takes up 100% CPU utilization with a heap of libraries for pdf services. NPR-15606 HotFix for GRANITE-12929  
* Accessing the 'My Link Shares' UI using Firefox browser does not display the shared items or users and the screen is unusable. NPR-15539: HotFix for CQ-4200992  
* While using the Digital Asset Manager, if a page is associated to a set of images, moving the images to a new folder breaks page association and the associated page misses some of the images. NPR-15538: Hotfix for CQ-111479  
* In the Dam Viewer component, using the 'nosamplecontent' run mode causes errors with dynamic media. NPR-15449: Hotfix for CQ-4195425  
* While creating video profiles, if both a high quality and a medium quality video encoding preset is chosen, the changes made are not saved. NPR-15447: Hotfix for CQ-4195482
* Even though upload of an asset to Brand Portal fails due to server error response, the status is updated to 'Published' on the Brand portal UI making it hard to track the missed file. NPR-15442: Hotfix for CQ-4197968  
* When publishing an asset folder to the Brand Portal, where publish takes more than an hour, some files fail to publish. NPR-15441: Hotfix for CQ-4199493  
* When using Asset Finder console in column view, trying to create a folder fails once though it succeeds on retrying. NPR-15370: Hotfix for CQ-4199448  
* In case an asset or folder selected in the DAM UI has a comma in the name, the References tab is not available and shows a message "List of references is not available for multiple selections". NPR-15362: Hotfix for CQ-4199721  
* Publishing a folder to Brand Portal does not change the folder's published state, even though the assets under the folder are published successfully. NPR-15292: Hotfix for CQ-4197667
* While navigating to the Assets console in Touch UI, an exception in shown while activating certain assets. NPR-15217: HotFix for CQ-108779  
* Publishing a video to Youtube when the connection is through a proxy server. NPR-15109: HotFix for CQ-110332  
* Using an asset with a name containing a dot or period (.) in data-sly-resource does not resolve to the same asset and the output path is terminated at the dot. NPR-15069: Hotfix for CQ-4195914  
* After upgrading AEM 6.2 to Service Pack1, the synchronization of assets into Scene7 fails. The dam:Scene7FileStatus property displays ' `UploadFailed`' status even for published assets. NPR-15269: Hotfix for CQ-4197708

### User Interface {#user-interface-5}

* In **[!UICONTROL Touch UI]**, the saved date is not shown for date fields that do not have type='datetime' while using Internet Chrome browser version 56.0.2924.87. NPR-15383: Hotfix for GRANITE-16481
* In **[!UICONTROL Touch UI]**, the Rich Text Editor removes the thread and the caption elements from HTML tables while rendering them. NPR-15267: Hotfix for CRTE-41
* `FileUpload Validator` does not handle cases when autostart is true or when `uploadFile()` is called manually and generates invalid validation report in these cases. NPR-15295: Hotfix for GRANITE-13499  

* Omnisearch does not allow customers using /apps to add a column data source since it assumes that the location configuration is listed under */libs/granite/omnisearch/content/metadata/*. NPR-13188 Hotfix for GRANITE-16479
* When using the **[!UICONTROL Touch UI]**, product variants are not created at the same level as the product. The user is not informed about the status of the variant creation process. NPR-15345: HotFix for CQ-4198948

**Scene 7**

* Running Scene7 workflow results in open files that do not close. Request to improve AEM-S7 service so that it maintains and reuse a single HttpClient instance with shared pooling configuration. NPR-15357: HotFix for CQ-109958

### Translation {#translation-9}

* When using translation projects, updating language copies from the English master, produces 11 separate launches all with the same name and source root, but with slightly different launch roots, in case the page name follows a set pattern. NPR-15605: Hotfix for CQ-4200699  
* Translation projects are not created for pages when the language roots have hyphens and dashes in the name. NPR-15171: HotFix for CQ-96286
* Request to update the Microsoft connector to be able to use the Microsoft Translator APIs, which Microsoft makes available in the Azure portal. NPR-15320: Hotfix for CQ-101010

### Projects {#projects-4}

* Only 20 inactive projects are visible in the Projects Screen though more than 20 inactive projects exist in the repository. NPR-15656: Hotfix for CQ-4200903

### Campaign {#campaign-1}

* While using the Campaign - Targeting and MAC - Test and Target Integration components, de-publication of activities does not update the activity status in the Master UI. NPR-15401: HotFix for CQ-4199839  
* While moving a product in AEM Commerce, the Product Move Wizard misses the pre-filled values for the product name, title, referenced pages, create author, and created date. NPR-15228: Hotfix for CQ-98617

### Security {#security-4}

* CSRF token parameter added to forms with a GET method. NPR-15229

### Forms {#forms-18}

#### Forms add-on package {#forms-add-on-package-18}

`**Adaptive Forms**`

* Default values get overridden by empty values in xml on pre-populating the Adaptive form with input XML. NPR-15721
* The `afData/afBoundData` wrapper is present in submitted XML, though even prefill XML does not have `afData/afBoundData` wrapper in XML schema-based adaptive forms. NPR-15541

* The titles in the Accordion bar should be editable HTML 'h2' headings instead of 'a' tag. NPR-15475
* The accordion layout of a form panel is not accessible to screen reader users. Users cannot navigate to the accordion tab by keyboard alone using screen reader software such as JAWS or NVDA. NPR-15474

`**Correspondence Management**`

* Saving, deleting, and setting reference for a document fragment takes substantial time. NPR-15939
* Tab alignment set in Manage Assets on text containing multiple Headers breaks in CCR UI. NPR-15818
* Thumbnails of Text modules do not show aligned content although the text contains aligned content created using Tabs in Google Chrome. NPR-15819

`**Forms Portal**`

* The Prefill Service does not work for XDP Forms. NPR-15466
* When storing Adaptive forms drafts and submissions to database, the state of the adaptive form gets corrupted when the database connectivity fails for any reason (for example, after a long time of inactivity). NPR-15297

#### Forms JEE Installer  {#forms-jee-installer-18}

`**Core**`

* After upgrading to the latest version of Java 1.8.0_121-b13, the Admin user interface is not accessible in AEM Forms. NPR-15330

`**XTG**`

* While using Output service to merge a specific form with a dataxml, the response time is 20 times as compared to the time taken by ES4 SP1 server for the same operation. NPR-15283

#### AEM Forms App {#aem-forms-app-1}

* When recovering unsaved tasks, the message shown on recovery of unsaved tasks needs to be made clearer to reduce user error. NPR-15377
* AEM Forms app does not render forms created from custom templates. NPR-15892
* Users are not able to log in the AEM Forms app. NPR-15891

The key highlights of AEM 6.2 SP2-CFP1 are:

* Streamlines replication functionality in Sites:

  * Fixes to various Rollout, LiveCopy, and faulty writing issues

* Enhances Touch UI responsiveness during:

  * Asset searches
  * size-based sorting

* Enhances Tag management in smart collections
* Tighter access controls during CRUD operations on folders

### Platform {#previous}

* Request for removal of `ReplicationQueue#forceRetry` API calls during startup of replication agents because such calls significantly slow down the instance, especially when it has many replication agents. NPR-14032: Hotfix for GRANITE-13095
* Request for `DurboImportConfigurationProviderService` OSGi configuration to support fields that can store an array of values. NPR-14570: Hotfix for CQ-108684
* Using the Sightly component in a page after migrating to AEM 6.2 causes the Properties dialog of the page to stop working. NPR-14328: Hotfix for CQ-108355
* Unscheduling a previously scheduled job does not remove the corresponding node below */var/eventing/scheduled-jobs*. NPR-14253: Hotfix for SLING-5666
* When an administrator tries to impersonate as a deleted user, the user interface fails to refresh. NPR-14247: Hotfix for CQ-107446
* XSS protection check causing incorrect encoding in Sightly component. NPR-14004: Hotfix for CQ-93821
* Request to upgrade Jackrabbit Filevault to 3.1.30 to resolve multiple issues. NPR-13454
* Cache error occurs when Sling distribution synchronizes the distribution packages from author to publish. NPR-13034: Hotfix for GRANITE-13970

### Sites {#sites-18}

* Issues with VersionManagerImpl purging incorrect versions from version history. NPR-14372 
* The WCM Sightly Foundation parsys component ignores the component declaration tag names, `cq:htmlTag / cq:tagName`. NPR-14225
* When Sightly Parsys is used to render components inserted via JavaScript in Touch UI, the custom decoration is ignored after the page is refreshed. NPR-14122
* Target dropdown lists do not work in Touch UI dialog when multiple Richtext fields, such as links are created. NPR-13911
* When editing a text field with multiple Rich Text Editor (RTE) properties in a dialog (Touch UI), the focus randomly shifts to a specific RTE property. NPR-13703
* Default out of the box video component does not render the video thumbnail. NPR-14976
* Information slowly loaded in the Live Usages tab in Template Editor. NPR-14880: Hotfix for CQ-83417
* Installing Hotfix-10936 on an AEM 6.2 instance disables the iparsys component. NPR-14330: Hotfix for CQ-106982  
* Multiple Rollout component issues and a Live Copy issue after migration to AEM 6.1 SP1. NPR-15256
* The Page Roll-out action fails to create children beyond the first level even for multiple Roll-out configurations. NPR-15055
* When submitting the PageProperties dialog from the Editor, unchanged data in LiveCopy tabs is rewritten. NPR-14693
* When the PageProperties Dialog is submitted from the Editor, MSM Post Processor writes some parameters from the request instead of the `msm:writeLiveCopyConfig` parameter. NPR-14434
* Multiple issues pertaining to Rollout component, Live Copies, and other aspects of MSM. NPR-12235

### Assets {#assets-18}

* UnPack Workflow unable to handle images with special characters in the image file name. NPR-15227: Hotfix for CQ-103887
* Assets having Repeat with Condition expression are not displayed properly. When the user previews the `*CDN3835RLCEN*` letter template, no assets that are located in the Body target area are displayed. When the asset `*VIPReassement*`, which is an optional asset, that is preselect is unselected, then the other assets that are preselected are displayed in the letter. NPR-14844

* While creating a smart collection, the style tag is not preserved when the smart collection is saved. NPR-15081: Hotfix for CQ-4195494
* Asset search queries running slowly in touch UI during concurrent searches by multiple users. NPR-15019: Hotifx for CQ-4195405
* Metadata extracted for a property of type `Long[]` converts to type `String[]` when the original asset is reuploaded to a different location. NPR-15016: Hotfix of CQ-4195005

* Users unable to delete a saved search or a smart collection. NPR-14924: Hotfix for CQ-108494
* Editing metadata for assets in bulk (append mode) while using a Boolean value for TypeHint in a drop down field in the underlying metadata schema produces an error. NPR-14529: Hotfix for CQ-106876
* Users without Replication rights can't delete Asset folders. NPR-14321: Hotfix for CQ-88271
* When trying to edit the video profiles for a video in Channel Editor, the design dialog does not open and raises a Null Pointer Exception in the error log. NPR-14144: Hotfix for CQ-81101
* The system-generated 'Created' timestamp property displayed in properties page for an asset is incorrect. NPR-13992: Hotfix for CQ-95029
* Request to enable detection of duplicate assets for users without Read access in AEM Assets NPR-13851: Hotfix for CQ-102281
* Users unable to edit metadata for assets in bulk from the properties page. NPR-13721: Hotfix for CQ-100703
* Incorrect error message in Classic UI when a duplicate asset is uploaded. The error message does not indicate why the upload failed. NPR-13691: Hotfix for CQ-99272
* AEM Assets unable to sort more than 50 assets by size at a time in List view when the folder contains numerous assets. CQ-100588
* Selecting multiple assets raises an error with Response Code - 414 (Request-URI Too Long) if the asset/folder URI is too long. NPR-13516: Hotfix for CQ-76076
* The Assets Report page becomes unresponsive when the user selects all choices in the Configure Columns dialog. NPR-13187: Hotfix for CQ-95589
* Unexpected behavior of Tag Picker in Safari and Internet Explorer. NPR-13134
* Editing saved search from the Assets Admin Search rail allows for saving them as nested smart selections, which cause environment stability issues. NPR-13119: Hotfix for CQ-99460
* After moving a file (or folder) and then renaming it, the 'cq:name' metadata does not reflect the new file name (folder name). NPR-13036: Hotfix for CQ-99141
* Asset with names that include special characters cannot be downloaded from the download link shared via email. NPR-12872: Hotfix for CQ-95795
* Out-of-the-box Asset reports generated when there are substantial number of assets cause heavy traversals where the search does not hit any index and CPU usage spikes. NPR-12811: Hotfix for CQ-84409
* Users on AMS AEM Assets author instance access from disparate networks unable to upload assets using chunk upload without delete privileges on folders. NPR-12768: Hotfix for CQ-82715
* In tag-based searches for assets using the Asset Search rail, the Type Ahead feature does not limit itself to the root path and displays tags from all namespaces. NPR-12666
* The StaticRenditions component raises a null pointer exception. NPR-12665
* Request to disable MissingMetadataNotificationJob because it causes the Badge Notification UI to break the page with a runtime exception "Unable to scan input." NPR-12500: Hotfix for CQ-93573
* The 'Disable Edit' option for a tag field does not work in asset properties pages on TouchUI. NPR-12429: Hotfix for CQ-88835
* API fixes in AEM Assets 6.2 for Companion App SMB implementation. NPR-11099
* Since the Jquery update, users unable to select an asset collection and confirm the selection in the Associate Content panel of a content fragment. NPR-14847: Backport for CQ-4194209
* Despite invoking infinite sorting at the client side, only articles/banners/collections currently displayed in the UI are sorted. NPR-14493: Hotfix for CQ-109926
* Request to implement omnisearch feature for AEM mobile-on-demand service. Keyword search for any article, collection, or banner does not return any matches. NPR-14093: Hotfix for CQ-101394
* When using the Coral-select component (*granite/ui/components/coral/foundation/form/select*) in a dialog, value initialization does not work correctly on Internet Explorer (IE11 or Edge browsers) when the selected value contains a single item. NPR-13395: Hotfix for CQ-101013

### Projects {#projects-5}

* When exporting a translation project created with Translation Method as 'human' and Translation Provider as 'none', no translation_export_summary.xml file is generated because the GUID mapping file is missing. NPR-13137: Hotfix for CQ-91976
* In the AEM projects, when creating a project with the due-date property set, the date conversion sets the time incorrectly due to difference in timezone between server and client. NPR-13003: Hotfix for CQ-98288
* The 'Reveal in Sites' option is missed from the translation job when a translation project is updated. NPR-12966: Hotfix for CQ-93740
* When a translation project is created for an exported site page, it does not render correctly in preview. NPR-12964: Hotfix for CQ-84627

### Workflow {#workflow-3}

* Payload link in the Archive tab of the Workflow console returns an error with response code '404' on clicking it. NPR-14993: Hotfix for CQ-4194977
* When using AEM default workflows, the CQ Mailer fails to send an email notification to the group that misses the e-mail address of a single member. NPR-14804: Hotfix request for CQ-91499
* Performance improvements for inbox and notification badge in Touch UI. NPR-14145: Hotfix for CQ-101125
* Users unable to preview the payload from the workflow Inbox console while initiating workflows. NPR-13226: Hotfix for CQ-100275
* The 'saml_request_path' cookie configured using the SAML Authentication Handler displays cookie set with an extra '?' character. In addition, when a SAML response is posted back to AEM, the AEM 'saml_request_path' cookie returns an invalid value because of already encoded characters. NPR-13517: Proactive Hotfix for GRANITE-11722 and GRANITE-14414

### Solution Integration {#solution-integration}

* After integrating AEM 6.2 with Search&Promote, if a user searches a term that returns a banner, the search functionality becomes unresponsive. NPR-14549: CFP for CQ-109631

### Dynamic Media {#dynamic-media}

* Numerous AEM-Scene7 sling jobs that were created and cancelled when during AEM activation is logged as archive jobs during replication. NPR-12835: Hotfix for CQ-86115

### Security {#security-5}

* Request for resolving input validation issue in WCMDebug filter. NPR-12444: Hotfix request for CQ-94890
* Proactive request for correcting XSS behavior while using Create Launch Wizard.  
  NPR-13062: Hotfix request for CQ-99577

#### Forms add-on package {#forms-add-on-package-19}

`Adaptive Forms`

* When creating a repeatable panel using adaptive forms, the panel title cannot be updated at run time. NPR-15325
* When the default value of a radio button is set and a value other than default is selected while saving or submission, the value is not shown on prefill. NPR-15304
* Google Chrome shows incorrect behavior on using the options event for dynamically populating the drop-down list and submitting the selected item's value. NPR-15198
* When creating a repeatable panel using adaptive forms, the panel title cannot be updated at run time. NPR-15181
* When using edit mode for adaptive forms, JavaScript errors such as - 'Handler of component is invalid' and 'guidelib is undefined', are encountered. NPR-15112
* Lazy Loading fragment inside a repeating panel does not work as expected. NPR-13916, NPR-14785

`Correspondence Management`

* Correspondence Management assets with `'Repeat with condition'`expression set are not displayed properly. NPR-14844
* When searching for a Correspondence Management asset (such as a letter, document fragment, or any other type), the Queue for Download icon goes missing from the toolbar. NPR-14745
* On creating a List module, toggling of the asset-specific properties (such as editable, mandatory) does not work. NPR-14689
* Data Elements panel in the Expression Builder utility keeps loading in case a condition module is created without selecting a data dictionary. NPR-14688
* On previewing a letter, users cannot use tab spaces to align content in tabular format. NPR-14481
* When exporting Correspondence Management assets in bulk from the user interface, AEM Forms server generates unnecessary logs. NPR-15226
* When a letter is previewed, justified text appears in a different font. NPR-15468

`**Forms Portal**`

* Attachments from submitted forms in the Forms portal are not visible when a new draft from portal submission is submitted. NPR-13515

`**Forms Manager**`

* While navigating in the *FormsandDocuments* directory, the Paste button is not displayed when user copies any asset and then navigates to a different folder. CQ-111327

#### Forms JEE Installer {#forms-jee-installer-19}

`Rights Management`

* The user login related audit event is logged with invalid time. The correct time for audit event is not traceable. NPR-13107
* Adobe Acrobat Reader and Microsoft Office fail to open documents protected with extended authentication. NPR-14482

`Process Management`

* When a forwarded draft task in HTML workspace is returned to the initial user, the task does not appear in the initial user's queue. NPR-15178

`Assembler Service`

* AEM Forms fail to validate a PDF/A-2b with more than two signatures. NPR-14101

`XTG`

* While printing a document using a printer bypass tray, the `GeneratePrintedOutput` function does not enable fetching paper from the right bypass tray. NPR-14079

#### Forms Designer {#forms-designer-2}

* Forms Designer crashes when user runs the Spell Check utility with the selected Form Locale as French (Canada). NPR-13740
* Forms Designer crashes when user selects calculate event or validate event for a form field and changes the language to JavaScript and enters `this.` in the **[!UICONTROL Script Editor]** window. NPR-12974

### Feature Packs included in CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Forms Add-on Package):

* When an adaptive form is created from an XDP file, tabbing for accessibility does not follow set pattern. NPR-12562

`Adaptive forms` (Forms Add-on Package):

* Rule Builder for adaptive forms does not provide role based access. Changes made by an author are not trackable. NPR-12840

`Core` (Forms JEE Installer):

* CoreCross Origin Resource Sharing (CORS) functionality as a servlet filter is not enabled for Jboss+. NPR-13050

## Download Instructions for CFP via Package Share {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>For AEM Forms customers, it is essential to install AEM forms add-on package after installing any AEM Service Pack, Cumulative Service Pack or Feature Pack.

You can download the CFP package directly from Adobe Package Share or perform the following steps:

1. On your AEM instance, click **Tools &gt; Package Share**. 
1. Log in using your Adobe ID credentials.
1. Search for **AEM6.2 SP1-CFP20** and click the appropriate package in the search results to open the CFP details page.
1. On the CFP details page, click **Download** and accept the license agreement. Click **OK** to confirm the download.

## Installation instructions for CFP {#installation-instructions-for-cfp}

This section walks you through the requirements and steps to install the CFP.

### Before you install {#before-you-install}

>[!NOTE]
>
>Optional Feature Packs provided by Adobe have dependencies on the release version and Cumulative Fix Pack. If you have any Feature Pack installed, please contact the [AEM Customer Care team](https://helpx.adobe.com/marketing-cloud/contact-support.html) to validate the compatibility with this Cumulative Fix Pack for AEM 6.2.

>[!NOTE]
>
>It is recommended that you run validation on every new installation package before attempting to install the package. Pre-validation analyzes and reports any errors found before installation and warn the users about such errors, overlays, permissions proactively.
>
>You can access documentation for Validate option at [https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 is a prerequisite for the CFP. For installation instructions, see [AEM 6.2 Service Pack 1 release notes](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html).  

* The Cumulative Fix Pack download is available on [Adobe Package Share](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20), which you can access directly from the AEM instance.
* For a cluster deployment using ( RDBMK  or MongoDB), the CFP package can be installed on any of the Author instances that  uses  Package Manager.

* Before installing the cumulative fix pack, ensure to take a snapshot or make a backup of your AEM instance.
* Uninstalling the CFP is not supported.

### Install the CFP via Package Share {#install-the-cfp-via-package-share}

Perform the following steps to install the Cumulative Fix Pack on an existing AEM 6.2 SP1 instance:

1. On your AEM instance, click **Tools &gt; Packages.** 

1. Find the downloaded CFP package and click Install.

### Automatic installation {#automatic-installation}

The CFP can be automatically installed into a running instance in the following ways:

* Place the package into ../crx-quickstart/install while the server is running. The package gets installed automatically.
* Use the [HTTP API from Package Manager](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) - make sure that you use `cmd=install&recursive=true` - so the nested package is installed.

### Validate installation {#validate-installation}

1. The Product Information page (/system/console/  productinfo  ) should now show the updated version string "Adobe Experience Manager, Version 6.2.0.SP1-CFP20" under Installed Products.
1. All OSGI bundles are either ACTIVE or FRAGMENT in the OSGI Console (Use Web Console: /system/console/bundles).

>[!NOTE]
>
>On successful installation of the package, an informational message appears indicating that the content package has installed successfully, such as "Content Package AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 installed successfully."

>[!NOTE]
>
>Since AEM 6.2 SP1-CFP1, the log level in Jackrabbit FileVault has changed from INFO to DEBUG for most of the messages. To obtain installation logs for a content package installed on AEM 6.2 SP1-CFP1 or higher, enable DEBUG log level for `org.apache.jackrabbit.vault.packaging.impl`.

### Install AEM Forms {#install-forms}

>[!NOTE]
>
>Skip this section if you are not using AEM Forms.

#### Install AEM Forms add-on {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms on JEE only**) The procedure to install a CFP on AEM Forms on JEE is described in [Installing CFP on AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Ensure that you have installed the AEM 6.2 SP1 CFP package. 
1. Download the corresponding Forms add-on package listed at [AEM Forms releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html) for your operating system.
1. Install the Forms add-on package as described in [Installing AEM forms add-on packages](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html).

#### Install AEM Forms JEE bundles package {#install-aem-forms-jee-bundles-package}

Fixes in AEM Forms JEE are delivered through a separate installer. For information about installing a CFP on AEM Forms on JEE, see [Installing CFP on AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Forms Designer installer {#designer-installer}

1. To install the update, run the Designer6.2.0_&lt;Language&gt;_Cumulative_QF.msp file.
1. On the welcome screen, click **update**. The installation starts.
1. After the installation completes, click **finish**.

## User Configurable timeout parameters for DTM, Analytics, Target, Search & Promote Connections {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

With AEM Cumulative Fix Pack 6.2 SP1-CFP7 and later releases, connection timeout periods have been made configurable on all above connections as per the details below:

| **Connections** |**Connection timeout&#42;** |**Socket timeout&#42;&#42;** |
|---|---|---|
| DTM |30000ms |30000ms |
| Analytics |30000ms |30000ms |
| Target |60000ms |30000ms |
| Search & Promote |30000ms |30000ms |

* **Connection timeout&#42;**- Timeout in milliseconds until a connection is established. A timeout value of zero is interpreted as an infinite timeout. 
* **Socket Timeout&#42;&#42;**- Timeout in milliseconds for waiting for data or a maximum period of inactivity between two consecutive data packets.

>[!NOTE]
>
>With AEM Cumulative Fix Pack 6.2 SP1-CFP6 and later releases, the OSGi configuration used for Search & Promote Integration is Apache HTTP Components Proxy Configuration. The Proxy configuration from Day Commons HTTP Client 3.1 is no longer used.

## Disable replication status in tagging console (Classic UI) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

In case you are using CFP3 or later, follow these instructions to disable Replication Status in the Tagging console in the Classic UI:

* Overlay *"/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js"* in */apps* 

* Add `replicationStateRequired`: "false" after Line #416.

  ```js
  415    baseParams: {
  416                    count: "false",
  417                    "replicationStateRequired": "false"
  418                },
  ```

## Latest Java 8 Update 131 throws an exception (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>These configuration settings are specific for AEM Forms customers using Document security.

NPR-21355 is included in CFP12.1. If you are installing CFP12.1 or later, then perform the below procedure to configure NPR-21355 on JBoss application server. If you are installing CFP12.1 on AEM Forms server running on Oracle WebLogic or IBM WebSpehere application servers, no additional configuration is required:

1. Backup, delete, and create new module.xml file. The default location of the file is [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/  

1. Open the newly created module.xml file for editing. Add the following code to the file:

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. Create a backup of the jsafeFIPS.jar, jsafeJCEFIPS.jar, and certjFIPS.jar files located at [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ and delete the files from the aforementioned directory.

   Contact [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to get new JAR files. Place the JAR files obtained from [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) at [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Windows only) Modify the `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` or `domain.conf.bat` configuration files:

    * For JBoss server in standalone configuration, open the standalone.conf.bat for editing.
    * For JBoss server in cluster configuration, open the domain.conf.bat for editing.

   Add the following lines at the end and save the file:

   set "JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true"

   set "JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"

1. (Linux-based OS only) Modify the [AEM_Forms_Installation_directory]/jboss/standalone.conf or domain.conf configuration files:

    * For JBoss server in standalone configuration, open the standalone.conf for editing.
    * For JBoss server in cluster configuration, open the domain.conf for editing.

   Add the following lines at the end and save the file:

   JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"

   JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"

## Configuration settings required for NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>The NPR-19778 is a part of CFP14.

The count for shared Queue doesnot refresh, by default, for other users when a user claims a task . For this, we have introduced a new property. Follow the steps below to configure this property on your AEM instance:

1. Go to Admin UI -&gt; Services -&gt; Workspace -&gt; Global administration.
1. Export Global settings.
1. In the downloaded XML file, add the tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>` Here, 10 is the example value in seconds. You can modify it accordingly.
1. Save the file.
1. Go back to Admin UI -&gt; Services -&gt; Workspace -&gt; Global administration.
1. Import the xml file in the Import Global Settings section.
1. You can now logout of the system and log in again.
1. The count for shared queue starts refreshing for other users in the workspace.
1. To turn off the polling, change the value to 0 and import the XML file again.

## UI Changes {#ui-changes}

* Behavior change in displaying titles on Image card for Image having dc: title property set to String [] ( multifield ): only latest changed title will be displayed on Image card in UI, although all titles will be saved in CRX. Hotfix for CQ-4217165

## Known issues {#known-issues}

* Updating AEM 6.2SP1-CFP19 and AEM 6.2SP1-CFP20 from CFP18 changes the root redirect to the Classic UI welcome page instead of /sites.html/content. You may have to correct sling: target property from /welcome.html to /index.html with CRX Explorer. This issue is not observed on updating from CFP17 or older version.

The following transient errors may occur when you install AEM 6.2 SP1-CFPx. However, no resolution is required for these errors because they do not impact your AEM instance and go away after CFP is installed:

* On upgrading AEM 6.2SP1-CFP20 instance to AEM 6.5, some vanity URLs may not work like:  

  * */projects.html*
  * */sites.html*

However, the workaround is to restart the AEM instance after an upgrade.

* HTTP 500 Internal Server Error is received when the Webconsole component detail page is opened.
* Errors as **create component instance** and **Service factory returned null** occurs due to repository restart:

  * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
  * org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Component: com.day.cq.tagging.impl.TagGarbageCollector (1687)))

* Error observed in CFP installation in Mongo and DB2: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException**. This error will not occur after installing a CFP over CFP8. 
* (Adobe Granite Maintenance Scheduler Update Task) com.adobe.granite.maintenance.impl.TaskScheduler: No maintenance task found with name WorkflowPurgeTask for window granite:weekly
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* When you install CFPx on AEM 6.2 SP1 that includes the Smart Tags feature pack, the previously-added workflow step for Smart Tag Assets gets deleted from the DAM Update Asset workflow.

See list of [Known Issues in AEM 6.2 SP1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Issues).

## Uber Jar {#uber-jar}

The Uber Jar for 6.2 SP1-CFP20 is available at [Adobe Public Maven repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/).

To use Uber Jar in a Maven project, include the following dependency in your project POM:

```
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-5}

The following text documents the list of OSGI bundles and content packages included in the CFP.

List of OSGi bundles included in AEM 6.2 SP1-CFP20

[Get File](assets/updated.txt)

List of Content Packages included in AEM 6.2SP1-CFP20

[Get File](assets/content_package_comparison_result.txt)

## Helpful resources {#helpful-resources}

* [AEM 6.2 hotfixes page](https://helpx.adobe.com/experience-manager/kb/aem62-available-hotfixes.html)
* [AEM 6.2 SP1 release notes](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)  
* [AEM 6.2 release notes](https://docs.adobe.com/docs/en/aem/6-2/release-notes.html)
* [AEM product page](http://www.adobe.com/solutions/web-experience-management.html)
* [AEM 6.2 documentation](https://docs.adobe.com/content/docs/en/aem/6-2.html)
* [Subscribe](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) to [Adobe Priority Product Updates](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)
