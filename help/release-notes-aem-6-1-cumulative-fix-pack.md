---
title: Release Notes: AEM 6.1 Cumulative Fix Pack
description: AEM 6.1 Cumulative Fix Pack
uuid: 7bee5414-01fc-486f-a6e2-0d3dd9c4a4d1
contentOwner: cmajumda
discoiquuid: 8d5a5d18-094b-486b-a921-474617f1a7b6
---

# Release Notes - AEM 6.1 Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Release information {#release-information}

| **Product** |Adobe Experience Manager |
|---|---|
| **Version** |6.1 |
| **Release** | [Cumulative Fix Pack 6.1 SP2-CFP18](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/cumulativefixpack/AEM-6.1-SP2-CFP18) |
| **Prerequisite** | [AEM 6.1 Service Pack 2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html) |
| **General availability** |January 11, 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Starting with AEM 6.1 Service Pack 2, Adobe has introduced a single delivery model for releasing fixes. Instead of releasing hot fixes for single issues, Adobe will release a Cumulative Fix Pack (CFP) every month (subject to passing quality checks), which is an aggregator content package for multiple fixes. CFPs primarily include bug fixes but might also include Feature Packs. They have the following advantages over single hotfix releases:

* Cumulative in nature (for example, CFP3 contains fixes for CFP2 and CFP1)
* Increased quality assurance
* Simplified installation (User installs a CFP as a single package that has no dependencies, except for the latest service pack)

For more information on CFP and other types of releases, see [Maintenance Release Vehicle](https://docs.adobe.com/content/docs/en/aem/6-1/deploy/maintenance-release-vehicle-definitions.html).

## About the release {#about-the-release}

AEM Cumulative Fix Pack 6.1SP2-CFP18, released on January 11, 2019, includes the most recent key customer fixes and is the last Cumulative Fix Pack for AEM 6.1.

>[!CAUTION]
>
>* Applying CFP without validating compatibility between installed feature packs may result in system failure or loss of custom configurations, which could require restoration from backup to resolve.
>* If your instance is running a higher version of Oak compared to the Oak version of the CFP package, the latter will not impact your current Oak version.

>[!NOTE]
>
>* Email bundle of apache commons **org.apache.commons/commons-email/1.5** has been added replacing **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* Apache Sling Scripting Sightly Models use Provider bundle **org.apache.sling.scripting.sightly.models.provider/1.0.0** has been added.
>
>* This CFP includes **jQuery 1.12.4** that can potentially impact your javascript application code. Ensure that you use appropriate JAVA APIs or library updates.

## Issues included {#issues-included}

This section lists all issues and hotfixes included in the current CFP. In addition, this CFP includes hotfixes delivered in [previous cumulative fix packs](#previous).

### Sites {#sites}

* cq:actions editannotate is not compatible with Touch UI mode. NPR-27160: Hotfix for CQ-4256192

### Forms {#forms}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

#### Forms add-on package {#forms-add-on-package}

>[!NOTE]
>
>AEM forms add-on packages help align forms functionality with AEM Service Packs and Cumulative Fix Packs. Therefore, it is imperative to install AEM forms add-on package after installing any AEM Service Pack, Cumulative Service Pack or Feature Pack.

* No new AEM Forms fixes in Forms add-on package.

#### Forms JEE installer {#forms-jee-installer}

* No new AEM Forms fixes in Forms JEE installer.

## Hotfixes and Feature Packs included in previous Cumulative Fix Packs {#previous}

### Cumulative Fix Pack 17 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.1 SP2-CFP17 is an important update that includes key customer fixes released since the general availability of [AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html) in August 2016.

Here are the key highlights of AEM 6.1 SP2-CFP17:

* Removed S7 polling importer from S7 cloud service configuration.
* Fixed adding of inline-styles to the hyperlink
* Fixed the scaling down when initial height is a multiple of the new height and vice-versa for scaling up.

#### Assets {#assets}

* (Firefox/Chrome) Unable to download assets in Asset Share page. NPR-25636: Hotfix for CQ-4244391
* Remove S7 polling importer from S7 cloud service configuration. NPR-25239: Hotfix for CQ-95236
* Publishing video generates DynamicMediaPreprocessor error. NPR-24981: Hotfix for CQ-4247072

#### Sites {#sites-1}

* "Live copy suspended" option of live-copy site is unchecked when field is modified in source site. NPR-25696: Hotfix for CQ-4250680
* WCM Foundation component 'Table' is vulnerable to Stored Cross Site Scripting. NPR-25185: Hotfix for CQ-4240760
* (Touch UI) NPE in datasource provider when trying to edit the embedded component dialog. NPR-25914: Hotfix for CQ-4250845
* Adaptive Image rescaling produces artifacts at the bottom of the image. NPR-26269: Hotfix for CQ-44156
* Rich Text Editor adds inline css "background-color" to links when using backspace/delete. NPR-26251: Hotfix for CQ-4251200

#### UI - Foundation {#ui-foundation}

* Upgrade to momentjs 2.18.1 to fix vulnerabilities in client library. NPR-25110: Hotfix for Granite - 21885

### Forms {#forms-1}

#### Forms add-on package {#forms-add-on-package-1}

#### Adaptive forms {#adaptive-forms}

* Unable to render XFA-based forms. NPR-25010: Hotfix for CQ-4248345

#### Forms - XMLFM {#forms-xmlfm}

* Using AEM forms 6.2 Output Service to merge a specific form with a data XML takes 20 times more time as compared to the time taken by LiveCycle ES4 SP1 server for the same operation. It is fixed on Windows and Linux environments. NPR-24137: Hotfix for CQ-108190

#### Document Services {#document-services}

* AssemblerService to PDFA produces pdf/a violating pdfs when multithreading. NPR-26329: Hotfix for CQ-4248656
* The PDF/A returned by Acrobat DC is non-compliant. NPR-26270: Hotfix for CQ-4248823

#### Forms - JEE Installer {#forms-jee-installer-1}

#### Forms - Foundation JEE {#forms-foundation-jee}

* The .sh files in LCM have been submitted with windows line endings causing the LCM not to run on unix platforms. NPR-22957
* (SOAP interface) Unable to open workspace after applying axis.jar 1.4 file. NPR-24529: Hotfix for CQ-4241833

* Changing the Form Locale to French (Canada) in the Dictionary Spell Check does not work in AEM Forms Designer. NPR-20765

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included}

List of OSGi bundles included in AEM 6.1 SP2-CFP17

[Get File](assets/61cfp17updated_bundles.txt)

List of Content Packages included in AEM 6.1SP2-CFP17

[Get File](assets/content_packages61sp2-cfp17.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.1 SP2-CFP16 is an important update that includes key customer fixes released since the general availability of [AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html) in August 2016. It includes version 1.2.18 of the built-in repository (Apache Jackrabbit Oak).

Here are the key highlights of AEM 6.1 SP2-CFP16:

* Fixed replication permission check for deleted nodes
* Fixes in the Apache Sling Scripting HTL Sling Models Use Provider bundle.
* Update to com.adobe.granite.sling/org.apache.sling.scripting.jsp/2.1.6-B001.
* Updated version of cq-platform-content.

#### Sites {#sites-2}

* Java Use object with underscores and trailing whitespace in the package declaration freezes the SightlyJavaCompilerService. NPR-22557: Hotfix for Granite-20836
* Display context option cannot be overridden in data-sly-text HTL block elements. NPR-22625

#### Platform {#platform}

* (Classic UI) Slow performance in tag console due to numerous queries. NPR-23349: Hotfix for CQ-4201748
* Patch jQuery 1.12.4 from clientlib to include security fix. NPR-24130: Hotfix for Granite-20058
* Apache Sling Scripting Sightly Models use Provider bundle org.apache.sling.scripting.sightly.models.provider/1.0.18. NPR-22614: Hotfix for Sling-5944, Sling-6866
* Replication of delete event doesn't check for rights. NPR-23382: Hotfix for CQ-4241234
* Publisher having error when flushing cache due to malformed URI. NPR-23551: Hotfix for CQ-4242790
* StackOverflowError when configuring the ootb dispatcher flush agent to update aliases. NPR-23635: Hotfix for CQ-4242928
* High CPU utilization is observed multiple times due to infinite loops. NPR-24414: Hotfix for NPR-21177

#### Granite {#granite}

* AEM instance crashes due to high heap utilization of Apache Http Client. NPR-22866: Hotfix for Granite-21056

#### Integration {#integration}

* Target engine (mbox.js, at.js) does not use mangled URLs and uses URLs containing colons which might fail with certain deployments. NPR-22366: Hotfix for CQ-4237854 
* Create activity Path variable not properly encoded leading to reflected cross-site scripting (XSS). NPR-22851

#### Vulnerability {#vulnerability}

* Salesforce integration is vulnerable to Server Side Request Forgery (SSRF). NPR-24289: Hotfix for CQ-4245277
* Cross-site scripting (XSS) in Admin UI Project links. NPR-23272: Hotfix for CQ-4241795

#### Campaign {#campaign}

* When trying to preview or publish a page, a string is displayed on teaser targeted component. NPR-23469: Hotfix for CQ-4242635

#### User Interface {#user-interface}

* (Classic UI) Performance issues with selectionchanged listener in case of multiple dropdowns. NPR-22724: Hotfix for CQ-4237215

#### WCM - Foundation Components {#wcm-foundation-components}

* CAPTCHA Component has been deprecated for better security, if you are using CAPTCHA component, then message "Captcha component is deprecated and should no longer be used." will be displayed after installing 6.1SP2-CFP16 or later releases. AEM component can be customized to include reCAPTCHA for better security NPR-22151: Hotfix for CQ-4220052

## Forms {#forms-2}

### Forms add-on package {#forms-add-on-package-2}

#### Forms-XTG {#forms-xtg}

* Output performance issues compared to ES4 SP1. NPR-24137, NPR-23987: Hotfix for CQ-108190

#### Output Service {#output-service}

* OutOfMemory due to “com/adobe/internal/pdftoolkit/services/xmp/XMPMetaFactoryMonitor”. NPR-24564: Hotfix for CQ-4244379

#### Assembler Service {#assembler-service}

* Discrepancy between Acrobat DC and AEM reports about PDF/A-1b compliance check error. NPR-24283: Hotfix for CQ-4227539
* Flattening a PDF with XFA version 3.0 does not retain the PDF form state. NPR-23131: Hotfix for CQ-4239155

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-1}

List of OSGi bundles included in AEM 6.1 SP2-CFP16

[Get File](assets/6_1_bundle-list.txt)

List of Content Packages included in AEM 6.1SP2-CFP16

[Get File](assets/6_1_content-package-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.1 SP2-CFP15 is an important update that includes key customer fixes released since the general availability of [AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html) in August 2016. It includes version 1.2.18 of the built-in repository (Apache Jackrabbit Oak).

Here are the key highlights of AEM 6.1 SP2-CFP15:

* Improved video encoding abilities for Dynamic Media files.
* Added delete collection modal on search result page.
* Fixed errors in the product page template missing product component.
* Updated cq-msm-core for efficient Livecopyindex synchronisation.
* OSGI configuration updates in serviceUser.target service.

### Assets {#assets-1}

* Dynamic Viewer fails to create certain size video renditions. NPR-22460: Hotfix for CQ-4237143
* Unable to delete the collections from the search results page. NPR-21055: Hotfix for CQ-4220922
* AOD-AEM asset synchronization stops working. NPR-22149: Hotfix for CQ-4207118
* Creation/Deletion of the asset doesn’t delete the create audit of the previous asset. NPR-21557: Hotfix for CQ-4231831
* Text extraction gets stuck for a corrupt PDF making AEM instance sluggish. NPR-21527: Hotfix for CTG-4150375
* (Classic UI) Damadmin stops loading when rep:policy (access control privileges) are applied under wcm/core/content/damadmin/tabs/searchpanel. NPR-21525: Hotfix for CQ-4229590
* AEM instance crashes while extracting image from doc file. NPR-21521: Hotfix for CQ-4231143
* (DAM) Multiple cross-site scripting (XSS) in DAM metadata editor. NPR-21434: Hotfix for CQ-83472
* (DM) [Classic UI] Multiple cross-site scripting (XSS) vulnerabilities in some SWF files in AEM CQ Author/Publish quickstart. NPR-21379, NPR-21073: Hotfix for NPR-20612
* Hash code collision causes wrong size of displayed image. NPR-21674: Hotfix for CQ-4223363

### Sites {#sites-3}

* Version Manager retrieves different results with and without recursive flag on/off. Version Purge can attempt to load version history on a non-versionable node causing exception. NPR-21662: Hotfix for CQ-4229696 & CQ-4211271

### Commerce {#commerce}

* Rollout of catalog fails if no product component is associated to the product page. NPR-22017: Hotfix for CQ-4232276

### MSM {#msm}

* LiveCopyIndex synchronization leads to congestion of threads during long index updates. NPR-21734: Hotfix for CQ-90667

### Foundation {#foundation}

* HTL: Uri manipulator breaks query parameter encoding. NPR-22372: Hotfix for SLING-6761
* Unable to sync groups between two publish instances. NPR-21943: Hotfix for Granite-19564

### Dynamic Video {#dynamic-video}

* High CPU utilization is observed frequently due to Scene7 content search requests. NPR-22140: Hotfix for CQ-4235872

### Vulnerability {#vulnerability-1}

* Cross-site scripting (XSS) in DAM metadata editor. NPR-21434: Hotfix for CQ-83472
* Multiple SWF files vulnerable to Cross-site scripting (XSS). NPR-20612: Hotfix for CQ-4213297

## Forms {#forms-3}

### Forms add-on package {#forms-add-on-package-3}

#### HTML5 Forms {#html-forms}

* Cannot use 'in' operator to search for '0' in 0,00" error using Belgium Locale on decimal field. NPR-22225: Hotfix for NPR-21510

#### Reader Extensions Service {#reader-extensions-service}

* Update jsafe jars to cryptoj 6.1.3.1 in Reader Extensions. NPR-21349

### Forms JEE installer {#forms-jee-installer-2}

#### Core {#core}

* Update jsafe jars to cryptoj 6.1.3.1 in Core, Signature, Encryption & Document Security. NPR-21353, NPR-21350, NPR-21348, NPR-21352
* Upgrading to the latest Java 8 Update 131 throws an exception: "JsafeJCE provider is disabled, a FIPS 140 required self-integrity check failed". NPR-21347: Hotfix for CQ-4208922

#### Install LCM {#install-lcm}

* Update Jsafe Jars to Cryptoj 6.1.3.1 in installer & LCM. NPR-21354

#### PDFG Service {#pdfg-service}

* Update jsafe jars to Cryptoj 6.1.3.1 in PDF Generator. NPR-21351

### OSGI bundles and content packages included {#osgi-bundles-and-content-packages-included-2}

List of OSGi bundles included in AEM 6.1 SP2-CFP15

[Get File](assets/6_1cfp15updated_bundles.txt)

List of Content Packages included in AEM 6.1SP2-CFP15

[Get File](assets/6_1cfp15content_packagelist1.txt)

AEM Cumulative Fix Pack 6.1 SP2-CFP14 is an important update that includes key customer fixes released since the general availability of [AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html) in August 2016. It includes version 1.2.18 of the built-in repository (Apache Jackrabbit Oak).

Here are the key highlights of AEM 6.1 SP2-CFP14:

* Improved rendering of Parsys components in Classic UI.
* Resolved out of memory issues using Sightly classes.
* Proactive security fix to remove flash dependency.
* Improved folder handling for Campaigns and Communities sites.

### Assets {#assets-2}

* TIFF images get auto-downloaded on clicking Original under Rendition. NPR-20466: Hotfix for CQ-4224679
* (Classic UI) Dam Admin fails to load tags when the referencing tag is deleted. NPR-20629: Hotfix for CQ-4224004
* (Chrome) Unable to open "detailed asset view" or "User preferences" while viewing a video asset on any tablet service. NPR-20863: Hotfix for CQ-4226516
* (DAM) (ClassicUI) Multiple cross-site scripting (XSS) vulnerabilities in some SWF files in AEM CQ Author/Publish quickstart. NPR-21071, NPR-21074: Hotfix for NPR-20612

### Sites {#sites-4}

* Copied components breaks/removes the parsys and removes sling:resourceType property. NPR-20146; Hotfix for CQ-4212306
* Text fields losing properties when using the property edit dialogue. NPR-20595, NPR-20997: Hotfix for CQ-4221537
* Export option to csv from a search page is fetching only first 10 records. NPR-20832: Hotfix for CQ-44157
* The value does not reset even when users try to cancel the inheritance on page properties. NPR-20931: Hotfix for CQ-83261
* When using the move page wizard, the destination step makes the system unresponsive. NPR-21011: Hotfix for CQ-4228909
* (Classic UI) Move tags cannot be removed. NPR-21149: Hotfix for CQ-4229164

### Platform {#platform-1}

* Package Manager "session time out" due to large number of dependencies. NPR-20574: Hotfix for Granite-19569
* Performance issues with TWC on publish instances. Threads are blocked by org.mozilla.javascript.ImporterTopLevel.getPackageProperty(..) NPR-21190: Hotfix for Granite-19524

### Integration {#integration-1}

* (Classic UI) Inconsistent behavior with Parsys components while targeting in Classic UI. NPR-20645: Hotfix for CQ-4219983

### Commerce {#commerce-1}

* Internal server error on selecting a time filer and cancel on the catalog product page. NPR-21056: Hotfix for CQ-4227580

### WCM - Foundation Components {#wcm-foundation-components-1}

* OutOfMemory:Metaspace errors due to lot of duplicate sightly classes in heapdump. NPR-21120: Hotfix for SLING-4787 and SLING-4783

### Security {#security}

* Security patch applied to Apache Sling XSS Protection API to eliminate the possibility of XSS bypassing. NPR-21290: Hotfix for GRANITE-19924
* XSS bypass in XSSAPI#getValidHref function. NPR-21172: Hotfix for Granite-19924

## Forms {#forms-4}

>[!NOTE]
>
>Due to no change in Forms add-on packages released for AEM 6.1 SP2-CFP13, we are currently not releasing any new add-on packages for AEM 6.1 SP2-CFP14. Therfore, you must re-install AEM 6.1 SP2-CFP13 add-on packages after installation of AEM 6.1 SP2-CFP14 to incorporate Forms enhancements and bug fixes from previous CFPs.

### OSGI bundles and content package included in CFP14 {#osgi-bundles-and-content-package-included-in-cfp}

List of OSGi bundles included in AEM 6.1 SP2-CFP14

[Get File](assets/6_1cfp14updated_bundles.txt)

List of Content Packages included in AEM 6.1SP2-CFP14

AEM Cumulative Fix Pack 6.1 SP2-CFP13 is an important update that includes key customer fixes released since the general availability of AEM 6.1 SP2 in August 2016.

Here are the key highlights of AEM 6.1 SP2-CFP13:

* Increased the versatility of the offloading workflow to accommodate folder names with special characters.
* Improves the functionality of the create folder dialog for the sites console.
* Enhanced Adaptive Forms to attach PDF as attachments in Safari.
* Fixes in show/hide functionality of drop-down component.

### Assets {#assets-3}

* Static renditions not displayed in the Rendition rail when original/rendition is selected. NPR-19390: HF for CQ-4217839
* Assets expiration activities stop if an asset does not have an assigned owner. NPR-18986; Hotfix for CQ-4197946  
* (TouchUI) the "View Properties" and Annotate buttons not displayed when subassets are selected, which prevents bulk metadata editing with subassets. NPR-20246: Hotfix for CQ-4220346  
* The time-based asset expiration scheduler job unable to expire more than 10 assets at a time even if there are more assets scheduled for expiration. NPR-20287: Hotfix for CQ-4218193  
* When an asset with a Chinese file name is detected as duplicate through "Asset Duplicate Detection" functionality, the Duplicate Detection dialog displays a corrupted name for the asset. NPR-19620: Hotfix for CQ-4220427
* When the original rendition of a PDF file is overwritten, the title gets appended instead of being replaced. NPR-19665; Hotfix for CQ-4220595  
* Expired assets can be downloaded only from the Card View, but not from the asset details page. NPR-19710: Hotfix for CQ-4218432  
* Asset PDF rendition is not generated correctly and takes long to generate thumbnails. NPR-19244: Hotfix for CQ-4215791
* Create asset request with JSON format returns a combined JSON and HTML. NPR-19603: Hotfix for CQ-4219606
* Editing metadata for assets in bulk (append mode) while using a Boolean value for TypeHint in a drop down field in the underlying metadata scheme produces an error. NPR-19109: Hotfix for CQ-106876

### Sites {#sites-5}

* Folder name containing hyphen(-) converts to underscore(_) in URL. NPR-19326: Hotfix for CQ-4215273
* ContextHub files do not minimize on the author instance and get downloaded by some browsers on every request. NPR-19142  
* Mobile Emulator Not Loading from /content/launches/jcr:content node. NPR-19728: Hotfix for CQ-4218109  
* OOTB reports in /etc/reports/ are not working properly and show no historical data graph. NPR-20035: Hotfix for CQ-4220180  
* (Safari) Users are unable to view all the assets in the asset finder panel. NPR-18595: Hotfix for CQ-4213720
* (Touch UI) After adding mappings under etc/map, the page is not refreshing and JS console error is getting generated. NPR-18965  
* Version Purge task does not remove old versions of assets. NPR-18990: Hotfix for CQ-4214996  
* When using the move page wizard, the destination step makes the system unresponsive. NPR-18985: Hotfix for CQ-4216827

### Platform {#platform-2}

* Fixed issues with curl Head requests for OOTB assets in AEM. NPR-20048: Hotfix for CQ-4221520 and CQ-103024
* Search in package manager result in traversal slowing the AEM production instance. NPR-19719

### Integration {#integration-2}

* Target activity gets deactivated after adding an extra experience. NPR-18227; Hotfix for CQ-4201895

### MSM {#msm-1}

* Using pushOnModify roll-out method to restore a version of blueprint page sometimes deletes the livecopy. NPR-19554: Hotfix for CQ-76741
* The text disappears when users try to cancel the inheritance on page propoerties when cq-msm-locable property is absolute path. NPR-20321: NPR-18909: Hotfix for CQ-4214354

### Projects {#projects}

* Unable to add or remove users from a project using Edge browser. NPR-19327: CQ-4218500 
* Project editors unable to copy/paste assets into the project asset folder. NPR-19619: Hotfix for CQ-4215321

### Translation {#translation}

* Unable to create translation project from asset UI. NPR-19321: Hotfix for CQ-4216968

### WCM - Foundation Components {#wcm-foundation-components-2}

* Show/hide functionality of the form drop-down component is not working as expected. NPR-20219: Hotfix for CQ-4222853

## Forms {#forms-5}

### Forms add-on package {#forms-add-on-package-4}

#### Adaptive Forms {#adaptive-forms-1}

* Enhanced Adaptive Forms to attach PDF as attachments in Safari. NPR-19624

#### Assembler Service {#assembler-service-1}

* XMP Metadata pdfaid:amd should be kept empty and not filled with a value. NPR-19646: Hotfix for CQ-4216597

### OSGI bundles and content package included in CFP13 {#osgi-bundles-and-content-package-included-in-cfp-1}

List of OSGi bundles included in AEM 6.1 SP2-CFP13

[Get File](assets/osgibundles6_1_sp2cfp13.txt)

List of Content Packages included in AEM 6.1SP2-CFP13

[Get File](assets/contentpackages61sp2cfp13.txt)
AEM Cumulative Fix Pack 6.1 SP2-CFP12 is an important update that includes key customer fixes released since the general availability of AEM 6.1 SP2 in August 2016.

Here are the key highlights of AEM 6.1 SP2-CFP12:

* Improved Export URL resolution of CSV reports for Sites.
* Improvement in re-ordering local ACL policies in CRXDE.
* Optimized Asset offloading by making OAKResource Listener queue length user configurable.
* Enhanced Query optimization during XPath to SQL2 query conversion.
* Upgraded version of org.apache.sling.servlets.post servelet (2.3.22) in Apache Sling API pages. 
* Enabled support for EMC Documentum 7.3 and preSubmit event for HTML5 forms.

### Integration {#integration-3}

* Connections to Target from AEM through HTTPClient do not have user-configurable timeout periods. NPR-18494
* Connections to Search & Promote from AEM through HTTPClient do not have user-configurable timeout periods. NPR-18493  
* Connections to Analytics from AEM through HTTPClient do not have user-configurable timeout periods. NPR-18497  
* Connections to DTM from AEM through HTTPClient do not have user-configurable timeout periods. NPR-18495  
* Viewing Campaign offers published from library folders result in NPE. NPR-18732; Hotfix for CQ-4214593

### Assets {#assets-4}

* For specific AI files, the web enabled JPEG rendition generated is blank. NPR-18518
* Metadata Asset Manager throws an error while saving metadata: XML namespace required for all elements and attributes. NPR-18652; HF for CQ-109960  
* Users unable to download assets from AEM protected by licence agreement using Safari browser. NPR-19288; Hotfix for CQ-4214358
* Video aggregation by Dynamic Video returns only top 100 items in result set. NPR-18340; Hotfix for CQ-4213561

### Sites {#sites-6}

* When editing a page in Classic UI, the Pages tab of Content Finder does not show the actual page that is modified. NPR-18332  
* Pressing the Backspace key after editing the hyperlink text in RTE changes its background color to grey. NPR-18212  
* Using the paramformat option to change text format in a page while inline editing on TouchUI automatically submits the page without saving the changes. NPR-18762  
* Unable to drag images from the content finder to replace images in the Thumbnail tab under Page properties on TouchUI. NPR-19123

### Platform {#platform-3}

* User unable to configure the OakResourceListener queue to optimize asset offloading. NPR-18185  
* Vulnerable CSRF token getting attached to the URL to download the CSV report for a page. NPR-15229

### Projects {#projects-1}

* When a project task is created, Upload Asset does not work. NPR-19121

### User Interface {#user-interface-1}

* Queries get stuck in the Query optimization phase during XPath to SQL2 query conversion. NPR-18616; Hotfix for Granite-18026  
* Request to use an updated version of the moment.js plugin (2.10.6) for CoralUI. NPR-18611, Hotfix for Granite-11881

### Granite {#granite-1}

* Sling resource resolver mapping "exposes" the internal URL for AEM if the URL in incoming publish requests includes special characters/query parameters. NPR-18527; GRANITE-18012  
* Issues with re-ordering local ACL policies in CRXDE. NPR-18797; Granite - 16300

### Commerce {#commerce-2}

* Catalog creation fails when Product master page provided in catalog is a live copy of another page. NPR-18649; Hotfix for CQ-420978

### Security {#security-1}

* Request to use an upgraded version of org.apache.sling.servlets.post servelet (2.3.22) in Apache Sling API to pre-empt an XSS vulnerability. NPR-18963

### WCM - Foundation Components {#wcm-foundation-components-3}

* Unexpected behavior of the Cancel Inheritence functionality in Multi Site Manager (MSM). NPR-18560; CQ-4214025

## Forms {#forms-6}

### Forms add-on package {#forms-add-on-package-5}

#### HTML5 Forms {#html-forms-1}

* While previewing letter in HTML mode, an error is displayed: this._xfa is not a function. NPR-17797

### JEE Installer {#jee-installer}

#### ECM Connectors {#ecm-connectors}

* Support for EMC Documentum 7.3 is added to AEM 6.1 Forms on JEE. NPR-16571

#### XTG {#xtg}

* AEM Forms fails to post data on SSL protected webservices. NPR-18681

#### Installation {#installation}

* Administrator screen on Microsoft windows displays version number 6.0 after installing 6.1SP2-CFP10. (CQ-4217575)

### Feature Packs included in CFP12 {#feature-packs-included-in-cfp}

* Added support for preSubmit event. NPR-14388; CQ-4214505

### OSGI bundles and content package included in CFP12 {#osgi-bundles-and-content-package-included-in-cfp-2}

List of OSGi bundles updated in AEM 6.1SP2-CFP12

[Get File](assets/aem_6_1sp2-cfp12osgibundles.txt)

List of content packages updated in AEM 6.1SP2-CFP12

[Get File](assets/list_of_content_packagesupdatedinaem61sp2-cfp12.txt)

AEM Cumulative Fix Pack 6.1 SP2-CFP11 is an important update that includes key customer fixes released since the general availability of AEM 6.1 SP2.

The key highlights of this Cumulative Fix Pack are:

* Efficient management of hidden components in layout mode in tablet.
* Introducing Quickactions on Hybrid Devices.
* Resolving component level synchronization issues with live copies.

### Integration {#integration-4}

* Resolved AEM Search component errors that can occur when AEM Day HTTP Client 3.1 OSGI is configured with a Proxy that requires Digest Authentication. NPR-18128: Hotfix for NPR-18029
* On refreshing a page, Targeting Experiences are not correctly updated. NPR-18656; CFP for CQ-4209422

### Assets {#assets-5}

* An error occurs when an ASCII/UTF-8 encoded text file is uploaded to AEM Assets and thumbnail generation fails. NPR-18006: CFP for CQ-4209345

### Sites {#sites-7}

* The text component toolbar I TouchUI is partially obscured when a large amount of text is entered. NPR-17933: Hotfix for CQ-4194816
* The option to unhide hidden components is not displayed for tablet/phone devices in Layout mode. NPR-17860: CFP for CQ-4207011
* Issues with ContextHub ProfileStore for anonymous users. NPR-17823: CFP for GRANITE-10171
* Normal users can activate page locked by admin. NPR-17508: Hotfix for CFP CQ-4206140
* Blocked queues for replication agent because rep:policy nodes are replicated when folders are moved via the site admin pane. NPR-17806: Hotfix for CFP CQ-4206140

### User Interface {#user-interface-2}

* Request to display quick actions on Hybrid devices. NPR-17754: Hotfix for GRANITE-17566

### MSM {#msm-2}

* Modified localized components not restored to their original form when inheritance is reapplied in a LiveCopy. NPR-18119: Hotfix for CQ-4211379

### WCM-Foundation Components {#wcm-foundation-components-4}

* Search component being used in OOTB geometrixx becomes slow when it hits a large number of pages/content in the repository. NPR-17671

### Security {#security-2}

* Issues with uploading avatar images for LDAP users. NPR-16561: Hotfix for GRANITE-17013

## Forms {#forms-7}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).

### Forms add-on package {#forms-add-on-package-6}

#### Mobile Forms {#mobile-forms}

* Fixed the issue where users are not able to set focus on a group using the setFocus Form Bridge API. NPR-17775

### JEE Installer {#jee-installer-1}

#### Process Management {#process-management}

* The TaskContext variable is not populated for AEM Forms processes. NPR-18198
* After upgrading to AEM 6.1 Forms, HTML Workspace freezes on accessing Task List for specific users. NPR-18166
* JBOSS error logs show a misleading error message. NPR-17804

#### XTG {#xtg-1}

* AEM Forms fail to post data on SSL protected webservices. NPR-17930

### OSGI bundles and content package included in CFP11 {#osgi-bundles-and-content-package-included-in-cfp-3}

List of OSGi bundles updated in AEM 6.1SP2-CFP11

[Get File](assets/list_of_osgi_bundlesincludedinaem61sp2-cfp11.txt)

List of content packages updated in AEM 6.1SP2-CFP11

[Get File](assets/list_of_content_packagesupdatedinaem61sp2-cfp11.txt)

### Platform {#platform-4}

* Localized title for a tag cannot be deleted from the UI. NPR-17154; Hotfix for CQ-4208157

### Sites {#sites-8}

* A page locked by a user in the first session can be modified by another user in another session. NPR-17557; Hotfix for CQ-4199017

* The Show/Hide option in the Rules Editor does not display fields in the select dropdown, due to which rules cannot be created. The Show/Hide functionality should work irrespective of the parent component. NPR-17379; hotfix for CQ-4209418

### Assets {#assets-6}

* Uploading images in the Touch UI admin console does not show all renditions, though all of them are successfully uploaded in the crx repository. NPR-17417; hotfix for CQ-4209348
* In **[!UICONTROL Asset Reports]**, the ' **[!UICONTROL Customize Columns]**' dialog allows **[!UICONTROL Submit]** action with nothing checked under a certain condition, causing screen collapse and heavy load in case a report is generated. NPR-17401; CQ-4208482

### Security {#security-3}

This section lists all hotfixes included in the current CFP. In addition, this CFP includes hotfixes delivered in [previous cumulative fix packs](release-notes-aem-6-1-cumulative-fix-pack.md#main-pars-header-331345443).

* Dispatcher IP exposed via SurferInfoMgr. NPR-16005

### Forms {#forms-8}

#### Forms add-on package {#forms-add-on-package-7}

**Adaptive Forms**

* For an adaptive form with attachment, duplicate entries for the `afSubmissionInfo` tags are created in the submitted XML when the form is submitted for the second time. NPR-17349
* While using the Google Chrome browser, after removing an attachment from a form, trying to re-attach the same attachment again throws an error. NPR-17946, NPR-17947
* Events that require a true or false response should be wrapped in a `try/catch` block JavaScript to avoid errors in the log. NPR-16756
* While using the Google Chrome browser, after removing an attachment from a form, trying to re-attach the same attachment again throws an error. NPR-17296
* The attachment browsing windows opens in submitted forms on clicking the **[!UICONTROL Attachment]** button. NPR-17723

**Mobile Forms**

* Events on fields inside inactive subforms get executed. NPR-17212
* Trying to set the default display value for a dropdown does not work and the raw value is displayed instead of the display text. NPR-17285  
* The FormBridge `setFocus API` does not allow set focus to the parent exclusion group from an OnClick event. NPR-17289

#### Forms JEE installer {#forms-jee-installer-3}

* The Configuration Manager can fail during the upgrade process due to timeout issues. NPR-16773
* AEM forms 6.1 ears fail to get deployed with Java 1.7u131. NPR-17011

#### Forms Designer {#forms-designer}

A row set as 'Keep with next', moves to the top of other pages instead of the top of next page on Designer. NPR-17242

### OSGI bundles and content package included in CFP10 {#osgi-bundles-and-content-package-included-in-cfp-4}

List of OSGi bundles included in AEM 6.1SP2-CFP10

[Get File](assets/list-of-osgi-bundles-updated-in-aem-6.1sp2cfp10.txt)

List of content packages included in AEM 6.1SP2-CFP10

[Get File](assets/list-of-content-packages-included-in--aem-6.1sp2cfp10.txt)
Here are the key highlights of AEM 6.1 SP2-CFP9:

* Fixes for tagging while using the Touch UI
* Improvements in Asset Management and Translation
* Fixes in the following components:

  * CUG widget and LiveCopy in Sites
  * Adaptive Forms Rule Editor
  * Form Analytics and Forms Portal
  * Forms Designer, Output Service, and Workbench

### Platform {#platform-5}

* Unusual build up of sling distribution packages observed after upgrading from AEM 6.1 SP1 to 6.1 SP2 and installing CFP3 and Communities FP6. NPR-15154; Hotfix for GRANITE-16183
* Request to consider removing the `ReplicationQueue#forceRetry` called during agent startup, as it causes a significant slowdown in instance startup when there are lots of agents. NPR-14130; Hotfix for GRANITE-13095
* Rendering a page as a PDF in production ready mode (by changing the extension .html to .pdf using Pdf Rewriter) displays a blank page with an error. NPR-16777; Hotfix for CQ-4206337
* A sync issue occurs while updating a node value from a set of associated nodes in a publish instance, while it is being automatically synced to another publish instance. NPR-12928; Hotfix for CQ-4201878
* The Touch UI console does not pick up new languages for tagging. NPR-16517; HF for CQ-4205649  
* After upgrading to AEM 6.1, high CPU utilization is observed frequently when searching Scene7 cloud configuration in production Author environment. NPR-15838; Hotfix for CQ-4202360
* Replacement of loginAdministrative leads to regression in upgrade mergeback logic. NPR-12929; Hotfix for CQ97552
* Users cannot set a profile photo if the photo structure does not yet exist. NPR-16793; Hotfix for GRANITE-17135
* With Authentication Requirement for a page enabled, siblings of nodes with ‘AuthRequired’ string starting with the same name result in a 302 error. NPR-17009; Hotfix for CQ-4199691 
* LDAP users cannot impersonate another user using the Classic UI. NPR-17041; Hotfix for CQ-4207155 (See [Configuration settings required for NPR-17041](release-notes-aem-6-1-cumulative-fix-pack.md#main-pars-header-1635597902))

### Assets {#assets-7}

* The 'Replace' and 'Create Versions' functionality in asset management do not work as expected. NPR-16928; Hotfix for CQ-4205651
* While uploading assets, the asset metadata property is imported as type 'Date', when it should be of type 'String'. NPR-16742; Hotfix for CQ-4206262
* The Assets UI does not work properly for Touchscreen Laptops connected to an external monitor and a mouse. Users are not able to publish and un-publish assets or use some of the other asset-related functions. NPR-16514; HF for CQ-4204624

### Sites {#sites-9}

* The Sites UI shows a performance issue in the CUG widget when the user belongs to a large number of groups. NPR-16609; HF request for CQ-4206064
* After installing AEM 6.1 SP2 CFP7, a newly created user who does not have the 'Preferences' node cannot update user properties such as 'Language' in the Classic UI. NPR-17066; HF for CQ-4206604
* On a blueprint site using LiveCopy, trying to delete a Form component throws a NullPointerException and adds back the Form component instead of deleting it. NPR-16437; Hotfix for CQ-4204628

### Translation {#translation-1}

* The path of images or assets changes to respective localized sites after pages are added to a translation job, even though asset translation is disabled via Cloud Service Configuration. NPR-16815; Hotfix for CQ-4206007

### Security {#security-4}

* Request to prevent AEM version disclosure in AEM Web Syndication Feeds page. NPR-16219
* XSS vulnerability in the output generated by HTMLRendererServlet. NPR-17136

### Forms {#forms-9}

#### Forms add-on package {#forms-add-on-package-8}

**Adaptive Forms**

* Opening Adaptive Forms Script Editor and not selecting any event using the ' **[!UICONTROL Choose an Item]**' option results in the summary for the current event being shown as 'null'. NPR-17138
* When writing a script using the Rule Editor, saving a script in some cases sets the event type as 'undefined' resulting in the script not being able to work. NPR-16825
* The **[!UICONTROL Save Form]** functionality in Rule Editor does not work at runtime. NPR-16904
* An error is encountered during anonymous submission of XSD-based forms with the Submit action `Store Content`. NPR-17020

**Mobile Forms**

* The `Calculate Event` method fails for fields in repeatable panel, if they are present inside another sub form. NPR-17111
* The `Clear Items` method does not work in HTML5 forms. NPR-16764
* Submission of mobile forms containing a subform with 'inactive', or 'hidden' mandatory fields fails with an error. NPR-16814
* While previewing forms in the Forms Manager, tabbing does not work after installation of SP1 CFP4. NPR-16638

**Forms Manager**

* Port the Form Analytics fixes provided in the AEM 6.3 Forms Manager to AEM Forms 6.1. NPR-16337
* The Forms Analytics report does not display abort data. CQ-4208249
* In **[!UICONTROL AEM Forms Analytics Configuration]**, the description of the **[!UICONTROL Load App Measurement library]** is not clear. NPR-17217

**Forms Portal**

* Comments added while uploading file attachments are not displayed in a submitted instance though they are present in the XML file stored in the content repository. NPR-16843
* The link to download a submitted form opens an HTML page instead of a PDF. NPR-16906

#### Forms JEE installer {#forms-jee-installer-4}

**Core**

* Running an index scan against EDC tables containing a large number of rows, causes CPU starvation. NPR-16821

**Output Service**

* While using the Forms Output Service to preview an XDP form as PDF, a row set as Keep with next, moves to the top of other pages instead of the top of the next page. NPR-16819

#### Forms Designer {#forms-designer-1}

* While using the Forms Designer to preview an XDP form as pdf, a row set as **Keep with next**, moves to the top of other pages instead of the top of the next page. NPR-16913

#### Forms Workbench {#forms-workbench}

* A Workbench process in AEM Forms 6.1 cannot be renamed. NPR-16792

### OSGi bundles included in CFP9 {#osgi-bundles-included-in-cfp}

List of OSGi bundles updated between AEM 6.1 SP2 and CFP9

[Get File](assets/list_of_osgi_bundles_updated_between_sp2_and_cfp9.txt)

List of Content Packages included in AEM 6.1 SP2 CFP10

Here are the key highlights of AEM 6.1 SP2-CFP8:

* Provides validation option in package manager for detecting conflicts between overlay and hotfix 
* Facilitates more efficient building and running of queries using JSON Querybuilder
* Secures Forms prefill service
* Fixes issues encountered while:

  * Uploading duplicate assets and watermarking of assets
  * Updating LiveCopy components and page properties
  * Saving inline libraries using Campaign
  * Creating and submitting XSD-based adaptive forms
  * Previewing and submitting adaptive forms with file attachment widgets
  * Accessing the AEM Forms app

### Platform {#platform-6}

* The `PageManagerImpl.createRevision` leaves a node in checked-in state when an Oak Exception occurs. NPR-16220: Hotfix for CQ-99567
* After upgrading to AEM 6.1 SP2-CFP3, the dropdown values for multifield components that support drag and drop or custom xtypes do not get re-populated. NPR-15869: Hotfix for CQ-4194771 
* Multiple rich text fields in the Touch UI dialog cause the select drop-down link to not work properly. Other select dropdowns in the rich text editor too are disabled. NPR-15837: Hotfix for CRTE-65
* When using Google Chrome browser to edit text components on site pages, copying and pasting text starting with a new line does not work correctly. NPR-15698: Hotfix for CRTE-108
* While submitting the PageProperties dialog from the editor, the `msm:writeLiveCopyConfig parameter` is set, but not all required values are sent. Instead, the MultiSiteManager (MSM) post processor writes parameters from the request. NPR-15831: Hotfix for CQ-100479

### Sites {#sites-10}

* HTL: uri manipulator breaks query parameter encoding. NPR-16222: Hotfix for SLING-6761
* Request to add a validation option in package manager to detect any conflicts between overlaid file (JSP or JavaScript file) under /apps and the one contained in a Hotfix under /libs. Affected overlay can then be rebased to include changes from the file under /libs. NPR-16217: Hotfix for CQ-81729
* Running a query when using the JSON Querybuilder results in a Querybuilder stackoverflow exception. NPR-16099
* CodeUpgradeTasks are not executed when Services are registered too late. NPR-12123: Hotfix for CQ-96964

### Assets {#assets-8}

* Updating asset metadata does not update the value of the `dam:sha1` metadata attribute causing problems with duplicate asset detection. NPR-15949: Hotfix for CQ-101949, CQ-103432.
* On updating asset metadata, the last modified date is not updated. The properties xmpNodeType and xmpArraySizeLast Modified Date are missing for the XMP:History node. NPR-16448  
* Debug code enabled by default in the `WatermarkUtil` causes watermark to fail. NPR-15923: Hotfix for CQ-4203158

### Integration {#integration-5}

* During A/B Test Activity in AEM Target, the audience does not sync up to the Target and shows 'no audiences'. NPR-16229: Hotfix for CQ-4204210
* When configuring AEM Day HTTP Client 3.1 OSGI configuration with a Proxy that requires Digest authentication, the AEM Search component throws a `ConcurrentModificationException`. NPR-15309: Hotfix for CQ-4199191
* Saving an inline offer to an offer library fails due to an extra slash added before the offer library path. NPR-16598: Hotfix for CQ-4203286

### Forms {#forms-10}

#### Forms add-on package {#forms-add-on-package-9}

**Adaptive Forms**

* After an adaptive form with attachment widget is previewed, some parts of the form get disabled. NPR-16610   
* For forms with date fields, validation messages for date fields do not work in the HTML5 preview mode. NPR-16451  
* For XSD-based adaptive forms, additional tags present in the prefill XML are lost on form submission. NPR-16409
* For XSD-based adaptive forms, in case a new form instance is created from previously submitted form data, the file attachment node details are lost in the submitted XML. NPR-16275
* For adaptive forms containing the file attachment component, the submitted XML data does not contain the information for the file attachment component, when the form has any lazy loaded fragment. NPR-16273
* While saving an Adaptive Form with an attachment, the full path of the attachment is added in the `fileAttachment` tag of the generated XML, rather than the name of the attachment. NPR-16272
* In case of a file attachment widget where multiple attachments are allowed, if a new form instance with an attachment is submitted on a widget where a previous attachment was already attached, an error code appears on opening the added attachment instead of the actual content. NPR-16339
* Securing forms prefill service from unauthorized access through protocols such as `file://`, `http://`, and `ftp://`. For details, refer [Configuring Prefill Service using Configuration Manager](https://helpx.adobe.com/aem-forms/6-1/prepopulate-adaptive-form-fields.html#main-pars_header_601884624). NPR-15435.

#### Forms JEE installer {#forms-jee-installer-5}

**Process Management - HTML Workspace**

* Securing forms prefill service from unauthorized access through protocols such as `file://`, `http`://, and `ftp://`. For details, refer [Configuring Prefill Service using Configuration Manager](https://helpx.adobe.com/aem-forms/6-1/prepopulate-adaptive-form-fields.html#main-pars_header_601884624). NPR-15437

#### AEM Forms App / Mobile Workspace {#aem-forms-app-mobile-workspace}

* Users are not able to access the AEM 6.1 Forms via AEM Form mobile apps. NPR-15999

### OSGi bundles included in CFP8 {#osgi-bundles-included-in-cfp-1}

The following text document lists the OSGi bundles included in AEM 6.1 Cumulative Fix Pack SP2-CFP8.

List of OSGi Bundles updated between AEM 6.1 SP2 and CFP8

[Get File](assets/aem_6.1_sp2_cfp8_updated_osgi_bundle_list.txt)

Here are the key highlights of AEM 6.1 SP2-CFP7:

* Fixed issues while using Site components such as:

Version Purge

Descendent Pages

Column Control

* Fixed issues encountered during uploading, deleting, and bulk editing of assets
* Updated Microsoft connector for translation to be able to use new APIs for the Azure portal
* Enhanced HTML5 forms capability for handling Calculate Events, aligning with PDF forms

### Sites {#sites-11}

* Using the Version Purge feature when one of the candidate versions is older than the Max Version Age makes the `VersionManagerImpl` purge the incorrect version and log an error. NPR-15833: HotFix for CQ-104193  

* While configuring a text field with multiple Rich Text Editor properties using the Touch UI, the focus randomly ends up within one of the Rich Text Editors in the dialog every time the component is 'edited' on a page. NPR-15544: HotFix for CQ-101793  
* Deleting a column control component placed into a form component does not delete all the nodes in the repository.  
  NPR-15412: HotFix for CQ-4199945  

* The out of the box List component option, 'Descendent Pages', does not work. NPR-15410: HotFix for CQ-60791

### Assets {#assets-9}

* On deleting an EPS file in AEM, the Scene7 synchronization purges not only the EPS file but also all its related assets, instead of deleting only the EPS file. NPR-15700: HotFix for CQ-4200226
* After uploading a PDF to AEM Assets, the PDF thumbnail shows corrupt images if large images are contained in the PDF.  
  NPR-15342: HotFix for CTG-4150272
* After enabling dynamic media, video reports are not visible to users with read access to them. NPR-15979: 
  HotFix for CQ-4202019

### Integration {#integration-6}

* The `SlingPostProcessor` is triggered if the page directly referencing the framework is edited. NPR-15754: HotFix for CQ-104153
* In Campaign, the targeting framework does not get updated with Client Context changes after reconfiguring the Client Context Store properties. NPR-15076: HotFix for CQ-4194842

### User Interface {#user-interface-3}

* When using the Touch UI with Google Chrome browser version 56.0.2924.87, the Date fields that do not have the `type="datetime"` fail to show the saved date value. NPR-15384: HotFix for GRANITE-16481
* While accessing the Manuscript Console through Apache webserver, the **[!UICONTROL Save]**, **[!UICONTROL Help]**, and other icons are not visible on top of the console. NPR-11129: HotFix Request for CQ-87728

* The Asset Bulk Editor for tags does not work if only one item is selected for bulk editing. NPR-15327: HotFix for CQ-4196649
* In the Touch UI, searching for a User/Group by entering special characters in the search field does not work. NPR-15977: HotFix for GRANITE-16518

### Platform {#platform-7}

* After installation of AEM 6.1 Cumulative Fix Pack SP2-CFP4, installing a package of size 480 MB consumes more than 50 GB of temporary space. NPR-15685: HotFix for CQ-4202159

### Translation {#translation-2}

* Request to update the Microsoft connector to be able to use the Microsoft Translator APIs, which Microsoft will make available in the Azure portal. NPR-15322: HotFix for CQ-101010

### Localization {#localization}

In the Classic UI, the user language is ignored in most dialogs after installation of the AEM 6.1 Cumulative Fix Package SP2-CFP4. NPR-15981: HotFix for CQ-4199208

### Forms {#forms-11}

#### Forms JEE Installer {#forms-jee-installer-6}

`HTML workspace`

* While using Forms JEE Workspace, when there are more than 10 items in the tracking panel, the scroll bar does not appear and user cannot scroll down to the first item. NPR-15651: HotFix for CQ-4200988

### Feature Packs included in CFP7 {#feature-packs-included-in-cfp-1}

`HTML forms` (Forms add-on package)

* Request to update the functionality of HTML forms to handle Calculate Events same as that handled by PDF Forms. Presently, 'Calculate event' on all fields is triggered any time the Instance Manager is invoked. NPR-14835

Here are the key highlights of AEM 6.1 SP2-CFP6:

* Improved editing experience in Sites:

  * Removed glitches in Bulk editor Inline editors
  * Resolved issues with restoring the inheritance functionality in Live Copy

* Better targeting experience:

  * Resolved non-pointer exceptions by TargetedContentManager
  * ReconfiguredTarget Framework to ensure it is responsive to client context changes

* Increased the versatility of the offloading workflow to accommodate folder names with special characters
* Fixed issues with creating adaptive forms using XSD templates and Assembler service.
* Resolved issues with Sling utilities post upgrade

### Platform {#platform-8}

* Synchronization issue in `LinkCheckerSettingsProviderImpl` causes the production server to be inaccessible to users. NPR-14742: Hotfix for CQ-74439

### Sling {#sling}

* While streaming video to IE 11, Sling `StreamRendererServlet` does not use Partial Content Response. NPR-14877: Hotfix for GRANITE-15945

### Sites {#sites-12}

* Users cannot re-enable the 'Revert Inheritance' functionality for a live copy. NPR-15050: Hotfix for CQ-112828
* Bulk editor ignores escape characters in a String array property. NPR-14984: Hotfix for CQ-4194729  
* Version Purge fails to fetch and process versions in blocks. NPR-14968: Hotfix for CQ-109205  
* Clicking the 'Clear' button in the Thumbnail tab of the Properties page (Touch UI) doesn't remove image from the dialog. NPR-14967: Hotfix CQ-4194526  
* Issues with editing multiple image fields inline in Touch UI. NPR-14934: Hotfix for CQ-4194514  
* Promoting a launch to production doesn't push changes to pre-existing launches. NPR-14926: Hotfix for CQ-4194588

### Assets {#assets-10}

* Offloading workflow fails when asset path contains folders with special characters. NPR-15193: Hotfix for GRANITE-16280
* User can't view an asset's timeline, when the asset is moved from a folder for which the user doesn't have read permissions. NPR-15155: Backport for - CQ-4196689

### Projects {#projects-2}

* After upgrading the system from AEM 6.1 to SP1, the `Sync Translation` job which synchronizes data for translation does not run automatically. NPR-15082: Backport for CQ-90856

### Integration with Adobe Marketing Cloud {#integration-with-adobe-marketing-cloud}

* Character encoding issue when transferring data from AEM to Campaign. NPR-15234: Hotfix for CQ-4198256  
* If a user publishes a page after adding a targeting experience to it, `TargetedContentManager` returns a non-pointer exception. NPR-15187: Hotfix for CQ-4194740  

* `Target Framework` does not get updated with `ClientContext` changes. NPR-15076: Hotfix for CQ-4194842

### Forms {#forms-12}

>[!NOTE]
>
>In addition to the hotfixes listed below, the cumulative AEM 6.1 SP2-CFP9 release includes hotfixes delivered in [previous cumulative fix packs](#previous). For a list of packages, see [AEM Forms releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html).
>
>AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using separate Forms add-on package. For details, see [Install AEM Forms add-on](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms).

#### Forms add-on package {#forms-add-on-package-10}

* When creating an Adaptive Form and uploading an XSD file, AEM Forms does not save the correct XSD reference path, leading to an error. NPR: 15003
* While using Assembler service, file attachments of type 'ods' to a form, are not converted to PDF. NPR: 14892

### Feature Packs included in CFP6 {#feature-packs-included-in-cfp-2}

* `HTML5 forms` (available in Forms add-on package): Request to enhance tabbing support in HTML forms so that it follows the precedence of subforms in the hierarchy instead of the geographical hierarchy. NPR-12990

### Known issues for Cumulative Fix Pack 6 {#known-issues-for-cumulative-fix-pack}

* The ZIP file downloaded by administrator from the link in the email notification for downloading assets is invalid. CQ-4200974  
* `HEAD` request to Apache Sling default GET servlet returns a 403 error due to incorrect configuration of index files (CQ-4201682). To resolve the issue, perform these steps:

1. Access Web Console from *http://localhost:4502/system/console/configMgr*.
1. Edit the configuration `Apache Sling GET Servlets`.
1. Remove the entry `[index,index.html]` from Index Resources by clicking the (-) button.
1. Click the (+) sign to add the following entries:

    * index
    * index.html

1. Click Save.

For a complete list of issues, see [Known Issues in AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html).

**Sites**

* Component inheritance with AEM6.1 SP2 doesn't pull from source. NPR-14729: Hotfix for CQ-108507

**Assets**

* All icons appearing at the wrong position after user installs AEM 6.1 CFP3. NPR-14866: Hotfix for GRANITE-15920
* A broken link is sent in email notification when an asset is downloaded. NPR-14523: Hotfix for CQ-105429
* Links sent by CQ Workflow Email Notifications are encoded twice over. NPR-14494

**Projects**

* Expression language injection vulnerability. NPR-14781: Hotfix for CQ-110692

**Forms**

>[!NOTE]
>
>In addition to the hotfixes listed below, the cumulative AEM 6.1 SP2-CFP5 release includes hotfixes delivered in [previous cumulative fix packs](release-notes-aem-6-1-cumulative-fix-pack.md#previous).
>
>AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using separate Forms add-on package and Forms Workbench Hotfix. For details, see [Install AEM Forms add-on](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms) or [Forms Workbench installer](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms).

**Forms add-on package**

* On submitting a form set, the submission service encodes Chinese language characters in an incorrect format. (NPR-14778)
* On validating a PDF/A-1b compliant PDF document, AEM Forms return “`PDFA_METADATA_020_MISMATCHED_TYPE_FOR_PROPERTY`” error. The PDF document validates successfully with Adobe Preflight and third-party validator tools. (NPR-14758)
* When a user tabs back and forth in a calculated decimal field, it causes the value to be displayed incorrectly. The issue occurs only for non-English locales. (NPR-14735)
* When a PDF document is converted to PDF/A-1b with AEM Forms, an error message is displayed. (NPR-14801)

**Forms Workbench HotFix**

* The server log viewer feature of AEM Forms Workbench does not work correctly. Developers are not able to view the server log from within workbench. (NPR-14738) (HotFix# 1067-002)

### Feature Packs included in Cumulative Fix Pack 5 {#feature-packs-included-in-cumulative-fix-pack}

* Feature pack NPR-6576: Adobe Campaign provisions improvements for the Parsys placeholder, Context Hub components, and additional Seed Data.

### Adding ACLs {#adding-acls}

If you install AEM 6.1 CFP5 without first installing AEM 6.1 CFP4 or NPR-6985 with AEM 6.1 SP2, you must manually add ACLs for three principals (two `targetservice` principals and an `everyone` principal) to the */content* node for the feature pack for AEM target integration with AEM 6.1 (NPR-6985) to work properly.

1. Open Crx-de from *http://&lt;host-name&gt;:&lt;port&gt;/crx/de*.
1. From the tree listing, expand the **content** node.
1. On the right pane, switch to the **Access Control** tab.
1. By default, the **Current Path** option is selected and the access control list is displayed.
1. Click/tap **+** to add an entry.
1. From the dialog, click/tap the Principal icon, search for **targetservice**, and select it.
1. Ensure that the entry type **Allow** is selected. Then, select the privileges `jcr:read` and `rep:write`.
1. Open the **Advanced** section, and add */&#42;/jcr:content/cq:ActivitySettings* in the field `rep:glob` under **Restrictions**. Click/tap **Ok** to save the permissions.
1. Repeat steps 5-7 to add another set of ACLs for **targetservice** principal.
1. Open the Advanced section, and add */&#42;/jcr:content/cq:ActivitySettings/&#42; *in the field `rep:glob` under Restrictions. Click/tap **Ok** to save the permissions.
1. Repeat step 5. From the dialog, click/tap the Principal icon, search for **everyone**, and select it.
1. Select the entry type **Deny** and then select the `jcr:all` privilege.
1. Open the **Advanced** section, and add "*/&#42;/jcr:content/cq:ActivitySettings*" in the field `rep:glob`. under **Restrictions**. Click/tap **Ok** to save the permissions.

### Platform {#platform-9}

* Proxy exceptions ignored in Apache HTTP Components Proxy Configuration (Linkchecker fails). NPR-14527: Hotfix for CQ-104212
* Calls to the tag search widget are very slow for large replication queue. NPR-14507: Hotfix for CQ-108343
* The Sightly parsys component wraps itself into a div tag in preview and publish modes. NPR-14273: Hotfix for CQ-97269 
* If a user is deleted from the rep:impersonators list, the useradmin UI breaks. NPR-14247: Hotfix for CQ-107446
* ContentDispositionFilter can suppress content type when a setContentType request is forwarded to a new servlet for further handling. NPR-14092: Hotfix for GRANITE-14999

### Sites {#sites-13}

* Resolves incorrect behavior when comparing LiveRealtionships to detect configuration changes. NPR-14582: Hotfix for CQ-89664, CQ-96323
* SiteAdmin: Incorrect page reference when user tries to delete a page. NPR-14421
* After the publish later operation, the page moves to Projects page forcibly. NPR-14412: Hotfix CQ-108675
* Single Page Launch automatically activates all images under a tree. NPR-14401: Hotfix for CQ-106218
* Inherited Hide option in the Navigation checkboxPage properties from source is unchecked in live copy when it is saved. NPR-14366: Hotfix for CQ-107579
* Issues with overlays when page has 100% height. NPR-14117: Hotfix for CQ-81860

### Forms {#forms-13}

>[!NOTE]
>
>In addition to the hotfixes listed below, the cumulative AEM 6.1 SP2-CFP4 release includes hotfixes delivered in [previous cumulative fix packs](#previous).
>
>AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using separate Forms add-on package and JEE installer. For details, see [Install AEM Forms add-on](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms) and [Install AEM Forms JEE installer](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms).

#### Forms add-on package {#forms-add-on-package-11}

* Cannot sort columns in the search results in HTML Workspace on Microsoft Edge browser. (Ref# CQ-109497)
* Expression builder does not open in Microsoft Edge browser while creating a Condition module. (Ref# CQ-109094)
* Horizontal lines appear between form components in the Survey adaptive form template on Microsoft Edge browser. (Ref# CQ-108382)  
* HTML5 form elements like radio buttons and checkboxes overlay when they become visible. (Ref# NPR-14335)
* Support added for HTML5 forms on Microsoft Edge browser. (Ref# NPR-13747)
* The Click event on checkboxes in HTML5 forms does not work on some browsers. (Ref# NPR-13705)

#### Forms JEE installer {#forms-jee-installer-7}

* When using Forms and Output service to generate PDF from an XDP template that uses subforms to create header and rows with **Overflow Leader** and **Keep with next** options enabled, a row moves on top of the header from second page onwards in the resultant PDF. (Ref# NPR-14506)

* The generatePrintedOutput API fails to select correct printer bypass tray. (#NPR-14316)

### Assets {#assets-11}

* The component *granite/ui/components/foundation/form/userpicker* triggers a query that is sluggish in displaying results on a system with many users. NPR-14691
* Cannot rename DAM folder if permission Edit ACL is missing. NPR-14441: Hotfix for CQ-104652
* Blank renditions generated for a PDF file. NPR-14433: Hotfix for CQ-107421
* Modified column remains empty when assets are published. NPR-14387: Hotfix for CQ-104406
* jcr:content with incorrect node type is created when a processing profile is attached to folder that does not exist. NPR-14378: Hotfix for CQ-107848
* Image cannot be previewed when cq:tags is inserted by Metadata Profiles.  
  NPR-14361: Hotfix for CQ-107401
* Asset Expiry notification job not deactivating some expired assets. NPR-14353: Hotfix for CQ-10776
* When a PDF with content protection enabled is uploaded, PDFSecurityAuthorizationException is raised when trying to create subassets. NPR-14293
* Metadata Processor stores jcr:title as a non-string datatype depending on the exif data stored in image. NPR-14206: Hotfix for CQ-102098

### Projects {#projects-3}

* Live copy properties not deleted while creating language copies. NPR-14304: Hotfix for CQ-106421

### Feature Packs included in Cumulative Fix Pack 4 {#feature-packs-included-in-cumulative-fix-pack-1}

* Fix Pack for AEM Target Integration (A/B Testing) 6.1. NPR-6985

**Platform**

* Unscheduling a previously scheduled job does not remove the corresponding node under */var/eventing/scheduled-jobs*. NPR-13653: Hotfix for SLING-5666
* AEM login failures due to NumberFormatException raised when reading history log. NPR-13693: Hotfix for CQ-101965
* Spellcheck does not work when searching from out-of-the-box search components. With this fix, you can define the node type used in search queries in the Settings dialog of the Search component. Default node type values are `cq:Page` and `dam:Asset`. NPR-14073: Hotfix for CQ-104956

### Sites {#sites-14}

* Issues with publishing resources associated with the Design Importer component when a page is activated. NPR-13901: Hotfix for CQ-102532  
* Issues with page properties in the page tree when many product variants are created in the product tree. NPR-13716: Backport for CQ-97547  
* `RangeError` occurs in Chrome when users include multiple tagspredicate in the Sites Editor search panel. NPR-13475: Hotfix for GRANITE-13855
* AEM has a race condition in i18n. NPR-12520: Hotfix for CQ-61862
* UI becomes unresponsive when users enter text in input fields for page properties. NPR-13598: Hotfix for CQ-101406
* Searching for products in the Workflow Models page in TouchUI returns errors. NPR-13076: Hotfix for CQ-97680

**Assets**

* Support for single quotes in filenames of video assets that are transcoded using FFMPEG on Linux. NPR-13845: Backport for CQ-104182

**Integration with Adobe Marketing Cloud**

* Issues with submitting teamMemberRole for each teamMemberPrincipalName when sharing a folder with multiple users from ccsharewizard page. NPR-13802: Hotfix for CQ-103297

**Projects**

* CompareLaunchServlet doesn't return changes for launches automatically created when adding page translation. NPR-13452: Hotfix for CQ-98556

**Security**

* No MIME type validation is performed when binaries of files are uploaded to AEM. NPR-16617

### Forms {#forms-14}

>[!NOTE]
>
>In addition to the hotfixes listed below, the cumulative AEM 6.1 SP2-CFP3 release includes hotfixes delivered in [previous cumulative fix packs](#previous).
>
>AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using separate Forms add-on package and JEE installer. For details, see [Install AEM Forms add-on](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms) and [Install AEM Forms JEE installer](release-notes-aem-6-1-cumulative-fix-pack.md#install-forms).

#### Forms add-on package {#forms-add-on-package-12}

* The file attachment map property in the CRX repository contains an entry for the form attachment components that do not have any attachment. (Ref# NPR-13986)
* If a user opens a draft containing an attachment and tries to save the draft after deleting the attachment, then the form fails to save and an error message is displayed. (Ref# NPR-13821)
* On submitting a new draft from the forms portal, the attachments are lost. (Ref# NPR-13472)
* When you add multiple attachments to a draft form, the metadata node in CRX lists only the latest attachment. (Ref# NPR-13081)
* In Google Chrome and Mozilla Firefox browsers the click event is not working on check boxes as expected. (Ref# NPR-14254)
* In Google Chrome the click event is not working on radio buttons as expected. (Ref# NPR-14132)

#### Forms JEE installer {#forms-jee-installer-8}

* HTML Workspace fails to render a PDF for assigned tasks. (Ref# NPR-9674)
* “Select save Draft" functionality of HTML Workspace fails to work as expected. (Ref# NPR-10504)
* If SSO is enabled, users are unable to open forms in the To Do tab of HTML Workspace. (Ref# NPR-11195)
* “Claim and Open” functionality in HTML workspace does not work. The issue occurs intermittently. (Ref# NPR-9666)
* While rendering an HTML5 form in HTML Workspace, all the text fields become read-only. The issue occurs intermittently. (NPR-10229)
* When a user clicks the refresh button in To Do tab, queue list is repeated. (Ref# NPR-9505)
* An XML parsing error occurs on opening the Forwarded task. (Ref# NPR-9378)
* Issues with submitting a form using HTML workspace. The submitted form does not contain any data. (Ref# NPR-11149)
* Users are able to submit the form even before the form is rendered. The issue occurs because the AWS_SUBMIT click event code is bypassed. (Ref# NPR-10880)
* Increase in CPU utilization up to 100% and result in performance degradation. (Ref# NPR-11917)
* "Select save Draft" functionality in HTML Workspace fails to work as expected. (Ref# NPR-11594)
* After a user reopens a task, forms associated with the task fail to open in HTML Workspace. (Ref# NPR-11883)
* An email notification is not sent for the stalled operations. (Ref# NPR-12321)
* Repeating XML elements are not bound properly in a form set. (Ref# NPR-11298)
* Unable to convert an Open Office file to a valid PDF/A that passes compliance validation in Adobe Acrobat and AEM Forms. (Ref# NPR-13931)
* Group member count differs in Active Directory and AEM Forms User Management. (Ref# NPR-10263)
* Users are unable to sync more than 1500 Active Directory users in a group. (Ref# NPR-9910)
* The file attachment map property in the CRX repository contains an entry for the form attachment components that do not have any attachment. (Ref# NPR-13986)
* When you add multiple attachments to a draft form, the metadata node in CRX lists only the latest attachment. (Ref# NPR-13081)
* On submitting a new draft from the forms portal, the attachments are lost. (Ref# NPR-13472)
* If a user opens a draft containing an attachment and tries to save the draft after deleting the attachment, then the form fails to save and an error message is displayed. (Ref# NPR-13821)
* If a file attached to a form contains special characters in the filename, then on opening the attachment, an error code is displayed instead of the contents of the file. The issue occurs only on opening a saved or submitted form. (Ref# NPR-13808)
* Issues with resolving images dynamically after upgrading to AEM 6.1 Forms. (Ref# NPR-11669)
* Issues with cache serialization in AEM Document Security. This issue leads to inconsistent data between servers in a cluster. It can also lead to performance issues even for single-server environments. (Ref# NPR-11049)
* For a hybrid domain configured with an alternate login provider, the login redirection screen shows LiveCycle ES3. (Ref# NPR-10131)
* The start button is not displayed in the tracking tab. (Ref# NPR-9254)

### Platform {#platform-10}

* NPR-11724: Hotfix for **Oak 1.2.18**

* Request for upgrade to Jackrabbit Filevault to 3.1.30. NPR-13455
* Hotfix for issues with SSL Filters. NPR-12543
* Tag search in content finder does not fetch expected results. NPR-12436
* If a newly-created user tries to access the Web console (or OSGi console), the request goes into an infinite loop. NPR-12660: Hotfix for GRANITE-9526
* Running a query generates a querybuilder stackoverflow exception. NPR-13077: Hotfix request for CQ-90181
* The audit log nodes that not older than the minimum age of Audit Log Purge Scheduler are removed by the AuditLog maintenance task. NPR-12735: Hotfix for CQ-96368
* NPR-10768: Hotfix for CQ-73794, CQ-87177

### Sites {#sites-15}

* References wrongly updated when promoting a nested launch. NPR-13272: Hotfix for CQ-75340
* Custom image reference added to page dialog not visible under page properties in TouchUI. NPR-12603: Hotfix for CQ-90189
* Hotfix for performance improvements of Launches and bug fixes. NPR-12596
* Language copies pages created as live copies. NPR-12838: Hotfix for CQ-96054
* Page properties not getting saved under certain conditions. NPR-13075: Hotfix for CQ-95235
* MSM ControlCenter option to create LiveCopy at shallow parent not available. NPR-13094: Hotfix for CQ-83090
* The References tab in the Sites TouchUI console displays only 10 results for Borrowed Content and Lent Content, even if a page has more. NPR-12413: Hotfix for CQ-85608
* Live copy status is not displayed correctly. NPR-12790: Hotfix for CQ-97086

### Integration with Adobe Marketing Cloud {#integration-with-adobe-marketing-cloud-1}

* Unable to drop a Target component in the page in targeting mode. NPR-12917: Hotfix for CQ-49942

### Assets {#assets-12}

* Users unable to download assets in bulk. NPR-12524: Hotfix for CQ-94202
* Invalid tags applied when processing assets using the Camera Raw package. NPR-12973: Hotfix for CQ-96409
* Resource leak when running the out-of-the-box Scene7 point-to-point upload integration in the AEM 6.1 SP1 Author instance. NPR-12995
* Unexpected behavior of Asset search form. Search directory field is pre-filled with current folder path. NPR-12152
* Downloading assets on Assets author instance takes a long time. NPR-11273
* Hotfix for incorrect behavior of AEM Assets when replacing an asset in DAM. NPR-13001
* AEM instance crashes when specific PDF files are uploaded. NPR-12826: Hotfix for CQ-92002
* AEM fails to upload files with long filename (over 127 characters) to Scene7. NPR-12999
* Calling the CoralUI addOption function for select form fields results in the error message RangeError: Maximum call stack size exceeded being displayed. NPR-13475: Hotfix for GRANITE-13855
* Request for disabling MissingMetadataNotificationJob by default, because it can crash AEM instances. NPR-12490: Hotfix for CQ-93573
* PDF files do not generate thumbnails properly: NPR-12446: Hotfix for CTG-4150222, CQ-90532
* Saved searches not saving the filters that user select. NPR-13331: Hotfix for CQ-98628
* Granite References retrieves references first, and filters them afterwards. To limit the performance impact, filtering should happen before the references are retrieved. NPR-12725: Hotfix for GRANITE-8011
* Checkbox in the Reference List header does not reset internal state after reloading references. NPR-12697: Hotfix for GRANITE-13823
* Autocompletion in the tagspicker component ignores filter defined in rootPath property. NPR-12539: Hotfix for CQ-82496
* Unable to edit asset properties in bulk mode. NPR-13118: Hotfix for CQ-96870

### Forms {#forms-15}

>[!NOTE]
>
>In addition to the hotfixes listed below, the cumulative AEM 6.1 SP2-CFP2 release includes hotfixes delivered in [previous cumulative fix packs](#previous).
>
>AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using separate Forms add-on package and JEE installer. For details, see [Install AEM Forms add-on](#install-forms) and [Install AEM Forms JEE installer](#install-forms).

* A valid PDF/A-1b file is flagged as invalid due to PDFAErrorSetFont error. (Ref# NPR-13018)  
* Custom properties are not saved as part of the form binary in Forms Manager. (Ref# NPR-12531)  
* If you modify and check in an XFS stylesheet multiple times and create a new version of the Workbench application, only the first checked-in changes are visible in the new version of the application. (Ref# NPR-12258)
* If you are using subforms to create header and rows in an XDP template with **Overflow Leader** and **Keep with next** options enabled, a row moves on top of the header from second page onwards in the final XFA form. (Ref# NPR-12208)

### Commerce {#commerce-3}

* Request to remove inappropriate wording from AEM 6.1 code-base. NPR-12745: Hotfix for CQ-49051

### Workflow {#workflow}

* SlingException occurs when the letter case of letters in the user-id of users does not match the letter case of letters in the user-id to which a task is assigned. NPR-13400
* Inconsistency in Workflow state across nodes in an author-cluster. NPR-12647

### Projects {#projects-4}

* When a new page is copied by Language Copy, the order of the page is not retained. NPR-12471: Hotfix for CQ-91704
* Running a machine translation job for multiple pages using Microsoft Translator produces the error 'too many open files.' NPR-12502: Hotfix for CQ-95166
* CompareLaunchServlet doesn't return changes for launches automatically created when adding page translation. NPR-12837: Hotfix for CQ-98556
* Importing a broken XML file to a translation job corrupts translationStatus on a manual translation project. NPR-12794: Hotfix for CQ-96366
* Path fields not translated for partial site translations backport in AEM 6.1. NPR-10672: Hotfix for CQ-81094

### Dynamic Media {#dynamic-media}

* Dynamic Media requests don't use proxy/HTTP common client. NPR-10727: Hotfix for CQ-45695, CQ-88800
* DynamicMediaPreprocessor error when replicating non-existing path. NPR-13007: Hotfix for CQ-52409

### API changes {#api-changes}

There is an API change between 6.1 SP2 and 6.1 SP2-CFP2:

* **com.day.cq.dam.scene7.api** exported package version changed from 6.1.0 to 7.1.0.

### Platform {#platform-11}

* NPR-11309: Hotfix for **Oak 1.2.17**
* User preferences not replicated using the reverse replication agent. NPR-11765: Hotfix for GRANITE-12965  
* Keeping link checker enabled on the publish instance breaks the mappings. NPR-11772: Hotfix for CQ-43269
* Replication fails if page moved before reaching OnTime. NPR-11545: Hotfix for CQ-89172
* Users synchronized from LDAP not searchable by user id. NPR-11457: Hotfix for CQ-82051
* Merged tag appears as duplicate on TouchUI. NPR-11319: Hotfix for CQ-88485

### Sites {#sites-16}

* Siteadmin search panel doesn't open the right dialog. NPR-11112: Hotfix for CQ-43790
* Search Rail Filters issue: Orientation and Style don't fetch/refresh the resultset. NPR-11589: Hotfix for CQ-87978
* Multiple issues around LiveCopy. NPR-11493: Hotfix for CQ-89375, CQ-86613, CQ-81114, CQ-58969
* Design importer generates incorrect client library for secondary HTML file. NPR-11632: Hotfix for CQ-85543
* Position of annotations altered after refreshing a page. NPR-11464: Hotfix for CQ-84878

### Rich Text Editor {#rich-text-editor}

* Anchor plugin enabled in RTE produces a non-compliant HTML5 page in TouchUI. NPR-11842: CQ-89782  
* Pasting content directly in RTE using CTRL+V skips the line breaks. NPR-11512: Hotfix for CQ-89043

### Integration with Adobe Marketing Cloud {#integration-with-adobe-marketing-cloud-2}

* Adobe Target Mbox component doesn't work as expected. NPR-11718: Hotfix for CQ-59499
* Offer template does not display the scroll bar if the page contains multiple components. NPR-11696: Hotfix for CQ-83783

### Assets {#assets-13}

* Uploading a PDF file completely exhausts CPU resources. NPR-11749: Hotfix for NPR-12929
* Cannot publish asset that is moved to a folder that already contains another asset of the same name. NPR-11732: Hotfix for CQ-90511  
* AEM unable to generate report for a large number of assets. NPR-11693: Hotfix for CQ-89359  
* The value of the Last modified field not updating properly for assets with MIME type docx. NPR-11612: Hotfix for CQ-87126
* AEM Assets metadata profile tags field creates a single value string when there is one default value. Any subsequent processes, or scripts to apply tags cannot add tags to the asset. NPR-11520: Hotfix for CQ-87621  
* Lightbox permissions issue. NPR-11517: Hotfix for CQ-89379  
* The Disable Edit option for Tag Fields in Asset Properties (Touch UI) not working. NPR-11515: Hotfix for CQ-88835  
* Users without Replication rights can't delete AEM folders. NPR-11491: Hotfix for CQ-88271
* Sharing AEM Assets with Adobe CC as a'Viewer' fails. Request to remove the Viewer role from Role list in UI. NPR-11450: Hotfix for CQ-89395  
* Files with extension DOC and DOCX (upper case) uploaded to AEM Assets get stuck in the upload workflow. NPR-11360: Hotfix for CQ-88722  
* Slow download of assets on author server. NPR-11273  
* PDF files do not render properly. NPR-11273: Hotfix for CQ-40650

### Forms {#forms-16}

>[!NOTE]
>
>The AEM Cumulative Fix Pack does not include fixes for AEM Forms. They are delivered using a separate Forms add-on package. For details, see [Install AEM Forms add-on](#install-forms).

* AEM Forms add-on package released with AEM 6.1 SP2-CFP1 is a cumulative package that includes all hotfixes up to **2.4.128** in the 2.4.x series and **2.2.28** in the 2.2.x series listed on [AEM 6.1 Forms hotfixes](https://helpx.adobe.com/content/help/en/experience-manager/kb/aem61-available-hotfixes/aem61-forms-hotfixes.html).
* Cumulative hotfixes for AEM 6.1 Forms on JEE are also available as part of the AEM 6.1 SP2-CFP1 release. It includes all hotfixes listed on [Hotfixes released before AEM 6.1 SP2-CF1](https://helpx.adobe.com/content/help/en/experience-manager/kb/aem61-available-hotfixes/aem61-forms-hotfixes.html#cf1) and [AEM 6.1 Forms Feature pack 2](https://helpx.adobe.com/content/help/en/aem-forms/6-1/fp2-release-notes.html), which adds Japanese language support for AEM forms on OSGi, AEM forms on JEE, and Forms Designer.

## Download Instructions for CFP via Package Share {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>For AEM Forms customers, it is essential to install AEM forms add-on package after installing any AEM Service Pack, Cumulative Service Pack or Feature Pack.

>[!NOTE]
>
>* HTTP 500 Internal Server Error is received when the Web console component detail page is opened. To resolve this issue, a newer version of org.apache.felix.webconsole.plugins.ds component to version 2.0.8 has been deployed in the latest package [AEM 6.1SP2-CFP18.1](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/cumulativefixpack/AEM-6.1-SP2-CFP18.1).
>* AEM Forms customers should install [AEM 6.1SP2-CFP18](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/cumulativefixpack/AEM-6.1-SP2-CFP18) and then install AEM forms add-on package. If the above fix is required, they can then opt to install CFP18.1 package.

You can download the CFP package directly from [Adobe Package Share](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/cumulativefixpack/AEM-6.1-SP2-CFP18.1) or perform the following steps:

1. On your AEM instance, click **Tools** > **Package Share**.
1. Log in using your Adobe ID credentials.
1. Search for [AEM-6.1-SP2-CFP18.1](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/cumulativefixpack/AEM-6.1-SP2-CFP18.1) and click the appropriate package in the search results to open the CFP details page.
1. On the CFP details page, click **Download** and accept the license agreement. Click **OK** to confirm the download.

## Installation instructions {#installation-instructions}

This section walks you through the requirements and steps to install the CFP.

### Before you install {#before-you-install}

>[!NOTE]
>
>Optional Feature Packs provided by Adobe have dependencies on the release version and Cumulative Fix Pack. If you have any Feature Pack installed, contact the [AEM Customer Care Team](https://helpx.adobe.com/marketing-cloud/contact-support.html) to validate the compatibility with this Cumulative Fix Pack for AEM 6.1.

>[!NOTE]
>
>It is recommended that you run validation on every new installation package before attempting to install the package. Pre-validation will analyze and report any errors found before installation and warn the users about such errors, overlays, permissions proactively.
>
>You can access documentation for Validate option at [https://docs.adobe.com/content/docs/en/aem/6-1/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-1/administer/content/package-manager.html#Package%20Validator)

* AEM version 6.1 Service Pack 2 is a prerequisite for the Cumulative Fix Pack. For installation instructions, see [AEM 6.1 Service Pack 2 release notes](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html).  

* For a cluster deployment using (RDBMK or MongoDB), the CFP package can be installed on any of the Author instances that uses Package Manager.
* Before installing the cumulative fix pack, ensure to have a snapshot or create a backup of your AEM instance. 
* Uninstalling the CFP package is not supported.

### Install the CFP via Package Share {#install-the-cfp-via-package-share}

Perform the following steps to install the Cumulative Fix Pack on an existing AEM 6.1 SP2 instance:

1. On your AEM instance, click **Tools &gt; Packages**.  

1. Find the downloaded CFP package and click Install.

### Automatic installation {#automatic-installation}

The CFP can be automatically installed into a running instance in the following ways:

* Place the package into ../crx-quickstart/install while the server is running. The package gets installed automatically.
* Use the [HTTP API from Package Manager](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html) - make sure you use `cmd=install&recursive=true` - so the nested package is installed.

### Validate installation {#validate-installation}

1. The Product Information page (/system/console/ productinfo) should now show the updated version string "Adobe Experience Manager, Version 6.1.0.SP2-CFP18" under Installed Products.
1. All  OSGI  bundles are either ACTIVE or FRAGMENT in the  OSGI  Console.
1. The OSGi bundle org.apache.jackrabbit.oak-core is on version 1.2.18 or higher (Use Web Console: /system/console/bundles).

### Install AEM Forms {#install-forms}

>[!NOTE]
>
>Skip this section if you are not using AEM Forms.

#### Install AEM Forms add-on package {#install-aem-forms-add-on-package}

1. Ensure that you have installed the AEM 6.1SP2-CFP18 package. 
1. Download the corresponding Forms add-on package listed at [AEM Forms releases](https://helpx.adobe.com/aem-forms/kb/aem-forms-releases.html) for your operating system.
1. Install the Forms add-on package as described in [Installing AEM forms add-on packages](https://helpx.adobe.com/aem-forms/6-1/installing-configuring-aem-forms.html#installingaemformsaddonpackages).

#### Install AEM Forms JEE bundles package {#install-aem-forms-jee-bundles-package}

Fixes in AEM Forms JEE are delivered through a separate installer. For information about installing a CFP on AEM Forms on JEE, see [Installing CFP on AEM Forms JEE](https://helpx.adobe.com/experience-manager/install-cfp-aem-forms-jee.html).

#### AEM Forms App source code {#mobile-app}

**Note:** Starting CFP8, you can use the source code for the 6.4 AEM Forms App, which is backward compatible with the 6.1 Forms server as well and has several improved features. Contact [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to obtain the AEM Forms App source code package.

1. After you have obtained the AEM Forms Source Code package and it is added in your AEM Forms Package Manager, navigate to: `http://<server>:<port>/crx/packmgr/index.jsp`, and install `adobe-aemfd-forms-app-src-pkg-<version>.zip`. 
1. Open `http://<server>:<port>/crx/de/content/forms/mobileapps/src/adobe-lc-mobileworkspace-src-<version>.zip` in your browser. The source code, which is now downloaded on your system, can be subsequently used to build the AEM Forms App.

Use the following instructions to build the AEM forms app as per your operating system:

* [Set up Visual Studio project and build Windows app](https://helpx.adobe.com/experience-manager/6-3/forms/using/setup-visual-studio-project-build-installer.html)
* [Set up Xcode project and build iOS app](https://docs.adobe.com/content/help/en/experience-manager-64/forms/aem-forms-app/setup-xcode-project-build-installer.html)
* [Set up Eclipse project and build Android app](https://docs.adobe.com/content/help/en/experience-manager-65/forms/aem-forms-app/setup-android-studio-project-build-installer.html)

#### Forms Designer installer {#forms-designer-installer}

1. To install the update, run the Designer6.1.0_&lt;Language&gt;_Cumulative_QF.msp file.
1. On the welcome screen, click **update**. The installation starts.
1. After the installation completes, click **finish**.

After installing the Quick Fix:

* This fix is protected with PI legacy flag `<?layout layOverflowHeaderBeforeKeepChain 1?>`. Use this flag in your template. This issue is applicable for Static forms only.

#### Forms Workbench installer {#forms-workbench-installer}

1. Contact [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to obtain the patch.  

1. In the Workbench installation directory, launch the installer.
1. Select the language to use in the install wizard and click **OK**.
1. On the Introduction panel, click **Next**.
1. On the Choose Install Folder screen, verify that the default location displayed is correct for your existing installation, or click Browse to select the alternate folder where Workbench is currently installed, and click **Next**.
1. Read the Quick Fix Patch Summary information and click **Next**.
1. Read the License Agreement, select **I accept** to accept the terms of the license agreement and then click **Next**. If you do not accept the license agreement, you cannot continue.

1. Read the Pre-Installation Summary information and click **Install**.
1. When the installation is complete, click **Next** to apply the quick fix updates to your installed files.
1. When the quick fix installation is complete, click **Finish** to exit the wizard.

## User Configurable timeout parameters for DTM, Analytics, Target, Search & Promote Connections {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Connection timeout periods have been made configurable on all above connections as per the details below:

| Connections |Connection timeout&#42; |Socket timeout&#42;&#42; |
|---|---|---|
| DTM |30000ms |30000ms |
| Analytics |30000ms |30000ms |
| Target |60000ms |30000ms |
| Search & Promote |30000ms |30000ms |

* **Connection timeout&#42;** - Timeout in milliseconds until a connection is established. A timeout value of zero is interpreted as an infinite timeout. 
* **Socket Timeout&#42;&#42;** - Timeout in milliseconds for waiting for data or a maximum period of inactivity between two consecutive data packets.

## Configuring OakResourceListener queue size with AEM  {#configuring-oakresourcelistener-queue-size-with-aem}

OakResourceListener queue size has been made configurable to  default  value of 1000. To configure the queue size, go to:

1. `http://localhost:portnumber/system/console/configMgr`
1. Open "apache sling  jcr  resource provider factory"
1. Edit observation queue length.

## Latest Java 8 Update 131 throws an exception (NPR-21347) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>These configuration settings are specific for AEM Forms customers using Document security.

NPR-21347 is included in CFP15. If you are installing CFP15 or later, then perform the below procedure to configure NPR-21347 on JBoss application server. If you are installing CFP15 on AEM Forms server running on Oracle WebLogic or IBM WebSpehere application servers, no additional configuration is required:

1. Backup, delete, and create new module.xml file. The default location of the file is `[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/`
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

1. Create a backup of the jsafeFIPS.jar, jsafeJCEFIPS.jar, and certjFIPS.jar files located at `[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/` and delete the files from the aforementioned directory.

   Contact [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) to get new JAR files. Place the JAR files obtained from [Adobe Support](https://helpx.adobe.com/marketing-cloud/contact-support.html) at `[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/`

1. (Windows only) Modify the [AEM_Forms_Installation_directory]/jboss/standalone.conf.bat or domain.conf.bat configuration files:

    * For JBoss server in standalone configuration, open the standalone.conf.bat for editing.
    * For JBoss server in cluster configuration, open the domain.conf.bat for editing.

   Add the following lines at the end and save the file:

   set "JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true"

   set "JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"

1. (Linux-based OS only) Modify the `[AEM_Forms_Installation_directory]/jboss/standalone.conf` or `domain.conf` configuration files:

    * For JBoss server in standalone configuration, open the standalone.conf for editing.
    * For JBoss server in cluster configuration, open the domain.conf for editing.

   Add the following lines at the end and save the file:

   JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"

   JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"

## Configuration settings required for NPR-15869 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>The NPR-15869 is a part of CFP8. The following configuration setting should be done if you are installing Cumulative Fix Pack 8 or any CFP package released post CFP8.

If the user needs to store data for page properties at a greater depth than 1 under `/jcr:content`, use the following steps to do configuration changes:

1. Configure the property JSON Max results of `Apache Sling Get Servlet`using `/system/console/configMgr`

1. Set its value to a number >1000 (which is the current default) such that this number is greater than the total number of nodes in the `/jcr:content` subtree till the configured depth above.

This will enable the sling GET servlet to be able to return all the required nodes.

## Configuration settings required for NPR-17041 {#set}

>[!NOTE]
>
>The NPR-17041 is a part of CFP9. The following configuration setting should be done if you are installing Cumulative Fix Pack 9 or any CFP package released post CFP9.

Use the following steps to create a profile node for the user:

In the **[!UICONTROL Apache Felix Web Management]** console, add `profile/nt:primaryType="nt:unstructured"` to the `User Property Mapping` property of the **[!UICONTROL Apache Jackrabbit Oak Default Sync Handler]** configuration.

## Additional instructions for indexing {#additional-instructions-for-indexing}

While using AEM Communities, searching for a community user when there are a large number of community users might take substantial time (NPR-15390: Hotfix for CQ-4199692).

Use the following steps for speeding up the query:

1. Add the `displayName` property to the Publish instance(s) so that indexing can be done.  

1. Steps to add this index manually using CRXDE Lite are as follows:

    1. Log in as an admin user in CRXDE Lite.
    1. Copy the node */oak:index/authorizables/indexRules/rep:Authorizable/properties/profileEmail* to a new node in the same 'Properties' folder and name it 'profileDisplayName'.
    1. In the newly created node, 'profileDisplayName', change the property 'name' to 'profile/displayName'.
    1. Re-index by navigating to the node */oak:index/authorizables* and changing the property 'reindex' to be 'true'.
    1. Save the change, and the 'reindex' property automatically changes back to 'false' when re-indexing is done.

***Note: ***The preceding steps should only be performed on the Publish instance and not the Author instance.

## Known issues {#known-issues}

The following errors may occur during installation of CFPx package on AEM 6.1 SP2 and can be safely ignored:

* (FelixFrameworkWiring) com.adobe.cq.social.cq-social-commons [com.adobe.cq.social.commons.impl.DefaultAttachmentTypeBlacklistService(1494)] Timeout waiting for reg change to complete unregistered.
* (FelixDispatchQueue) com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: ServiceFactory.getService() resulted in a cycle.)
* (FelixFrameworkWiring)com.day.cq.search.impl.builder.QueryBuilderImpl Unable to get PredicateEvaluator instance: path  
* org.apache.sling.servlets.resolver.internal.SlingServletResolver bindServlet: Servlet service not available from reference [javax.servlet.Servlet]
* **ERROR** (pool-34-thread-5) org.apache.sling.discovery.impl.common.heartbeat.HeartbeatHandler announcementRegistry is null 
* **ERROR** (pool-34-thread-5) org.apache.sling.discovery.impl.common.heartbeat.HeartbeatHandler getResourceResolver: resourceResolverFactory is null! 
* **ERROR** (pool-34-thread-5) org.apache.sling.discovery.impl.common.heartbeat.HeartbeatHandler checkView: encountered a runtime exception during view check: java.lang.NullPointerException
* **ERROR** (Thread-237) com.day.cq.dam.cq-dam-handler `[com.day.cq.dam.handler.standard.msoffice.MSPowerPointHandler(1210)]`Cannot create component instance due to failure to bind reference jcrResolverFactory 
* **ERROR** (Thread-237) com.day.cq.dam.cq-dam-handler `[com.day.cq.dam.handler.standard.msoffice.MSPowerPointHandler(1210)]`Failed creating the component instance; see log for reason

Other Known Issues:

* The ZIP file downloaded by administrator from the link in the email notification for downloading assets is invalid. CQ-4200974  
* The TaskContext variable is not populated for AEM Forms processes. CQ-4212223
* com.adobe.granite.installer - Unable to finish updating bundle Service already unregistered.
* Publishing  a uploaded  video generates   error  :  Unable to analyze /content/dam/video-testing.mp4 for YouTube publish java.lang.NullPointerException: null. CQ-4250538

* For a complete list of issues, see [Known Issues in AEM 6.1 SP2](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html).

## Uber Jar {#uber-jar}

For AEM 6.1 SP2-CFP2 and higher versions, use the Uber Jar for AEM 6.1 SP2-CFP2 that is available in the [Adobe Public Maven repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.1.SP2-CFP2/). To use Uber Jar in a Maven project, include the following dependency in your project POM:

```
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.1.SP2-CFP2</version>
    <classifier>obfuscated-apis</classifier>
    <scope>provided</scope>
</dependency>
```

## OSGi bundles and content packages included {#osgi-bundles-and-content-packages-included-3}

The following text document lists the OSGi bundles included in the latest CFP.

List of OSGi bundles included in AEM 6.1 SP2-CFP18

[Get File](assets/61cfp18updated_bundles.txt)

List of Content Packages included in AEM 6.1SP2-CFP18

[Get File](assets/content_packages61sp2-cfp18.txt)

## Helpful resources {#helpful-resources}

* [AEM releases and updates](https://helpx.adobe.com/experience-manager/aem-releases-updates.html)
* [AEM 6.1 release notes](https://docs.adobe.com/content/docs/en/aem/6-1/release-notes.html)
* [AEM 6.1 hotfixes page](https://helpx.adobe.com/experience-manager/kb/aem61-available-hotfixes.html)
* [AEM 6.1 SP2 release notes](https://docs.adobe.com/docs/en/aem/6-1/release-notes-sp2.html)  
* [AEM product page](http://www.adobe.com/solutions/web-experience-management.html)
* [AEM 6.1 documentation](https://docs.adobe.com/content/docs/en/aem/6-1.html)
* [Subscribe](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) to [Adobe Priority Product Updates](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)
