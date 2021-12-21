---
title: AEM 6.3 Cumulative Fix Pack
description: AEM 6.3 Cumulative Fix Pack Release Notes.
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
---
# AEM 6.3 Cumulative Fix Pack Release Notes {#release-notes-aem-cumulative-fix-pack}

## Release information {#release-information}

| **Product** |Adobe Experience Manager |
|---|---|
| **Version** |6.3 |
| **Release** |Cumulative Fix Pack 6.3.3.8 on [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Prerequisite** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **General availability** |March 05, 2020 |

### Cumulative Fix Pack {#cumulative-fix-pack}

Adobe introduced a single-delivery model for releasing fixes. Instead of releasing hot fixes for individual issues, Adobe now releases a Cumulative Fix Pack (CFP) every month (subject to passing quality checks). A CFP is an aggregated content package for multiple fixes. CFPs primarily include bug fixes but might also include Feature Packs. They have the following advantages over individual hotfix releases:

* Cumulative in nature (for example, a CFP contains fixes delivered through previous CFPs)
* Increased quality assurance
* Simplified installation (User installs a CFP as a single package that has no dependencies, except for the latest service pack)

For more information on CFP and other types of releases, see [Maintenance Release Vehicle Definitions.](https://docs.adobe.com/content/docs/en/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)

## About the release {#about-the-release}

AEM Cumulative Fix Pack 6.3.3.8 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.8 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.20.

>[!CAUTION]
>
>Applying CFP without validating compatibility between installed feature packs may result in system failure or loss of custom configurations, which could require restoration from backup to resolve.

>[!NOTE]
>
>For AEM instances with a version lower than 6.3.3.0, Adobe recommends  deploy ing SP/CFP via the install folder for customers having a large number of users on AEM instance.

>[!NOTE]
>
>MongoDB Enterprise 3.6 is supported starting with AEM version 6.3.3.1.

## List of issues {#changes}

This section lists all issues and hotfixes included in the current CFP.

In addition, this CFP includes hotfixes delivered in [previous cumulative fix packs](#previous).

### Assets {#assets}

* The Add to Collection page does not show all the available collections in Card View while adding assets to collection (NPR-32537).

### Sites {#sites}

* When you select a parsys and a component inside it and use the keyboard shortcut to delete selected items, the action deletes both the component and its parent parsys (NPR-32071).
* When the properties of a page are saved, an incorrect node is created (NPR-31774).

### Integrations {#integrations}

* ReportSuitesServlet is vulnerable to SSRF (NPR-32162).

### Campaign Targeting {#campaign-targeting}

* A component’s content changed, in Author instance and then activated, is not visible in Publish instance until the component is restarted **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 and NPR-32232).
* Contexthub performances crash on publishing (NPR-31170).

### Brand Portal {#brand-portal}

* Adobe I/O is not integrated with Adobe Experience Manager 6.3 for Brand Portal (NPR-32056).

### Forms {#forms}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

#### Forms add-on package {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms add-on packages help align forms functionality with AEM Service Packs and Cumulative Fix Packs. Therefore, it is imperative to install AEM Forms add-on package after installing any AEM Service Pack, Cumulative Fix Pack, or Feature Pack.

* Designer: If the tagging option is enabled, the subform border disappears in the generated PDF output (NPR-32324 and NPR-32545).  
* Designer: If there are merged cells in a table, the accessibility test fails for the output PDF file converted from an XDP form using the output service (NPR-32068).  
* Document Security: A protected PDF file fails to open offline with `DisableGlobalOfflineSynchronizationData` option set to `True` (NPR-32080).

**Issues fixed in 6.3.0-0047**

* (JEE Only) Critical security vulnerabilities (CVE-2021-44228 and CVE-2021-45046) reported for Apache Log4j2.

## Hotfixes and Feature Packs included in previous Cumulative Fix Packs {#previous}

### Cumulative Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.3.3.7 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.7 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Assets {#assets-1}

* Assets selected (in Column view in Touch UI) before selecting the filter option from the Content Only drop-down and then selecting move option are also moved (NPR-30693).
* The `${extension}` variable is not rendered in author instance on workflow processing (NPR-31694).
* The expiration (client cache time to live) value configured for Dynamic Media Hybrid mode is not replicated to the Dynamic Media delivery environment (NPR-31114).  
* Assets are replicated to Publish instance from Author instance running on Dynamic Media - Scene7 deployment even after using default filters (NPR-30856).

### Sites {#sites-1}

* Page properties of a master-page fail to load and a NullPointerException is returned. The issue is resolved on adding the cq:blueprint property (NPR-30901).
* Rollout configurations are not properly retrieved from the blueprintConfig on the root node. The deactivation is triggered for both blueprints and live copies. The deactivation should only be triggered for the blueprint (NPR-30866).
* When a user rolls-out a page, the roll-out configuration dialog displays duplicate live copy paths (NPR-30438).
* Out of the box, the scaffolding Rich Text Editor (RTE). applies inline font-size to elements, unexpectedly (NPR-31283, NPR-30922).
* Unable to synchronize campaign in Adobe campaign containing out-of-the-box design importer component (NPR-30890).
* Rich Text Editor (RTE). does not allow to insert an embedded Table as a list item (NPR-30878).
* When a user focuses on left rail fields and uses a keyboard shortcut to paste content, it pastes the content of the page editor clipboard instead of the content copied from the left rail fields (NPR-31173).
* When a user edits a content fragment, the already deleted variation of the content fragment is restored (NPR-31272).
* AEM Site does not have the option to create a language copy (NPR-30690).
* Page Editor's actions do not have the controls to roll-out live copies (NPR-30613).

### Communities {#communities}

* Activities and Notifications titles are inconsistent (NPR-30940). 
* Analytics reports are not populated in AEM author environment, blank page appears (NPR-30905).
* Pagination is not working properly in Communities Blogs (NPR-30827).

### Foundation {#foundation}

* Updates in buffer size configuration for Jetty-based HTTP service are not saved (NPR-30925).

### Forms {#forms-1}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

### Forms add-on package {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms add-on packages help align forms functionality with AEM Service Packs and Cumulative Fix Packs. Therefore, it is imperative to install AEM Forms add-on package after installing any AEM Service Pack, Cumulative Fix Pack, or Feature Pack.

#### Adaptive Forms {#adaptive-forms}

* Floating values calculated using a script do not display correctly in a form that is part of a formset (NPR-30802).

#### HTML5 Forms {#html-forms}

* Generating HTML5 preview of an XDP form displays a flicker while adding instances of a subform (NPR-30908).

### Forms JEE installer {#forms-jee-installer}

#### Document Services {#document-services}

* OutputService displays an incorrect response after applying a patch to fix HTML to PDF issues (NPR-31504).

#### PDFG Service {#pdfg-service}

* Max reuse count with JMX console does not display for HTML2PDF service (NPR-30305).

#### Foundation JEE {#foundation-jee}

* Max reuse count with JMX console does not display for HTML2PDF service (NPR-30136).

### Cumulative Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.3.3.6 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.6 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

### Assets {#assets-2}

* Video aggregation by Dynamic Video returns only the top 100 items in result set. NPR-30441; Hotfix for CQ-4213561
* Adobe Smart Tag connectivity issue through Datapower. NPR-30026: Hotfix for CQ-4269457
* Unzipping an archive with a folder having a percent sign (%) in its name can not be opened using Assets interface. NPR-29989: Hotfix for CQ-4270467
* Processing sub-assets of large PDF files cause an OutOfMemoryError (OOME) exception. NPR-29851: Hotfix for CQ-4269574

### Sites {#sites-2}

* ContextHub error during AEM and Campaign integration. NPR-30624: Hotfix for CQ-4250790
* 'onTime' or 'offTime' metadata properties saved on assets are not recalled if the AEM server gets restarted. NPR-30412: Hotfix for CQ-4272784
* While generating a CSV export, adding custom columns for the list view break the report. NPR-30208: Hotfix for CQ-4273344
* OOTB reports in /etc/reports/ are not working correctly and historical data graph is not displayed. NPR-30016: Hotfix for CQ-4220180
* The value of the resourceType request parameter is copied into the value of an HTML tag attribute which is encapsulated in double quotation marks. NPR-29832: Hotfix for CQ-4255365

### Communities {#communities-1}

* Duplicate content issue with AEM Communities moderation console. NPR-30667: Hotfix for CQ-4276829

### Translation {#translation}

* Translation issue - Only a few components are translated using Machine Translation. NPR-30079: Hotfix for CQ-4273764  
* When using the translation framework, the addition of pages to multiple translation jobs triggers an error. NPR-29746: Hotfix for CQ-4270953

### Forms {#forms-2}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

### Forms add-on package {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms add-on packages help align forms functionality with AEM Service Packs and Cumulative Fix Packs. Therefore, it is imperative to install AEM Forms add-on package after installing any AEM Service Pack, Cumulative Fix Pack, or Feature Pack.

#### HTML5 Forms {#html-forms-1}

* When using NonVisual Desktop Access in Browse mode to read an HTML5 form, the Chrome browser reads "graphic" before each Scalable Vector Graphic (SVG) in the form design. NPR-30451: Hotfix for CQ-4274732

#### Forms - Backend Integration {#forms-backend-integration}

* Unable to see the service/data source for the database connection while creating the Form Data Model (FDM). NPR-30108: Hotfix for CQ-4273359

### Forms JEE installer {#forms-jee-installer-1}

#### Forms - Document Services {#forms-document-services}

* When a load test is performed on HTML to PDF service, it fails with an error and file type settings are removed from AEM forms server. NPR-30111, NPR-30086: Hotfix for CQ-4271495

### Cumulative Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.3.3.5 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.5 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.17.

### Assets {#assets-3}

* Updated DAM DMGateway interface for S3 multipart support. NPR-29740: Hotfix for Q-4226303
* Cannot delete an image rendition on a video asset from the asset details page. NPR-29417: Hotfix for CQ-4268675
* The owner cannot create a private folder inside a private folder. NPR-29397: Hotfix for CQ-4229830
* Uploading an Adobe Illustrator Artwork file more than 2 GB generates Java heap space error. NPR-29265: Hotfix for CQ-4226217
* Assets becomes unusable after DAM CQ Mime Type Service applies text for m3u8. NPR-29259: Hotfix for CQ-4264052
* Create option does not work when attempting to create collections in Edge. NPR-29248: Hotfix for CQ-4265699 and CQ-4265438
* Asset link share displays blank gray cards for some assets in the folder. NPR-29831: Hotfix for CQ-4270187
* The new tags added to assets fail to save and disappear from the properties. Hotfix for CQ-4271931, CQ-4270476

### Sites {#sites-3}

* CoralUI, when used with Multifield, stores the fileReferenceParameter at the component level instead of multifield level. NPR-29535: Hotfix for CQ-4266129
* Issue while trying to compare the newest and current page version on AEM 6.3.3.3. NPR-29532: Hotfix for CQ-4269639
* The path field opens at root path irrespective of the path specified to search. NPR-29398: Hotfix for CQ-4268897
* (Experience Fragments) FacebookApplication#setUpApp uses deprecated API, which doesn't work anymore. NPR-29213: Hotfix for CQ-4266630
* Error alert is generated when adding components to WCM page when minification is enabled on the instance. NPR-29476: Hotfix for CQ-4266197
* Empty properties and multiple properties are not propagated from blueprint during rollout. Reset live copy with blueprint does not work for components.NPR-29252: Hotfix for CQ-4264928, CQ-4264926, CQ-4267722
* Minimizing Rich Text Editor from fullscreen while in source edit mode leads to loss of content. NPR-28838: Hotfix for CQ-4260584

### Communities {#communities-2}

* Visitors and members, with no moderator privileges, can see unapproved and pending posts by pasting the URL. NPR-29726: Hotfix for CQ-4271124
* High response time up to 40-50 seconds is observed on user sign-in for Community. NPR-29679: Hotfix for CQ-4269444
* Unable to reset the password when logged in with different user name and email as the key appears to be generated with a swapped user name and email. NPR-29281: Hotfix for CQ-4268694

### Experience Fragments {#experience-fragments}

* Cannot export Experience Fragments to target when smart image is used. Hotfix for CQ-4269606

### Replication {#replication}

* Replication Agent component is susceptible to a vulnerability which discloses sensitive information to unauthorized users. NPR-29613: Hotfix for Granite-25070
* User-provided data is not escaped on output in the `cq/replication/components/agent`component, resulting in a stored Cross-site scripting (XSS) vulnerability. NPR-29452: Hotfix for CQ-4266263

### Forms {#forms-3}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

### Forms add-on package {#forms-add-on-package-3}

* No new AEM Forms fixes in Forms add-on package.

### Forms JEE installer {#forms-jee-installer-2}

* No new AEM Forms fixes in Forms JEE installer.

### OSGI bundles and content packages included in 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

List of OSGi bundles included in AEM 6.3.3.5

[Get File](assets/do-not-localize/6_5-bundle-list.txt)

List of Content Packages included in AEM 6.3.3.5

[Get File](assets/do-not-localize/content_packages6335.txt)

### Cumulative Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.3.3.4 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.4 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.16.
* Added socket timeout & connection timeout in Brand Portal replication agents.

### Assets {#assets-4}

* If re-uploading an archive with the same name, renditions are not generated for the new processed assets. NPR-28643: Hotfix for CQ-4262286  
* Workflow CommandLineProcess fails with filename having single quote. NPR-28805: Hotfix for CQ-4262287  
* Values are different between collection page and the collection page using filter. NPR-28642: Hotfix for CQ-4261405
* CommitFailedException triggers with upload of big zip archive assets. NPR-28528: Hotfix for CQ-4260903
* Folder meta-data fails to save when editing a folder that contains special characters. NPR-28211: Hotfix for CQ-4260401
* Unable to delete image renditions of a video asset from Asset Details page. NPR-29149: Hotfix for CQ-4266073
* DMS7 desktop video delivery using DMComponent uses progressive download for playing video in publish mode and does not stream. NPR-28754: Hotfix for CQ-4263732
* Unable to create/edit image presets as restricting access to /etc/dam/video/dynamicmedia disables features for Image Managers. NPR-28662: Hotfix for CQ-4263022
* Link Share with DMS7 encoded video files result in empty folders. NPR-28851: Hotfix for CQ-4206743
* The replication from AEM to Brand Portal gets stuck for long periods. NPR-28913: Hotfix for CQ-4254932

### Communities {#communities-3}

* Unable to open messages having attachments in outlook sent and inbox folder. NPR-28559: Hotfix for CQ-4217072

### Sites {#sites-4}

* Cross-site scripting (XSS) in SuggestionHandler for 6.3. NPR-28692: Hotfix for CQ-4253821
* Deep rollout ends without containing all branches in the respective LiveCopy. NPR-29175: Hotfix for CQ-4239472
* (MSM) Implement LiveCopyIndex using oak-index. NPR-29198: Hotfix for CQ-4222472
* The file 'coral.js' includes a vulnerable version of the library 'handlebars.js'. NPR-26973: Hotfix for CQ-4255377
* Using a Target component with a nested Layout Container and Text Component throws a JavaScript error 'Cannot read property currentPos of null' when editing text or clicking on the container. NPR-29077: Hotfix for CQ-4246594
* (Touch UI) Unable to bulk updating tags to pages that are already tagged by different tags. NPR-28729: Hotfix for CQ-4262922
* Opening the variation in card View causes a 500 error. NPR-28611: Hotfix for CQ-4263571
* Rollout of a structure which has been moved in a master leads to a wrong cq:moveTarget. NPR-28968: Hotfix for CQ-4265280

### Integration {#integration}

* (Cloud Service Configs) The "inherited from" checkbox appearing at the root level should be removed. NPR-28771: Hotfix for CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler goes into an infinite loop and causes updates to nodes on publish instances. NPR-28561: Hotfix for CQ-4263096
* Using Brightedge credential fails with connection error. NPR-29167: Hotfix for CQ-4265872
* Compilation issue in OfferproxyTandtProvider.java due to missing import statement for 'Resource' class: missing import statement: import org.apache.sling.api.resource.Resource. NPR-28772

### Commerce {#commerce}

* Sort option is not working for assets inside the Commerce collection. NPR-28755: Hotfix for CQ-4213622

### Jetty {#jetty}

* Jetty exceptions in error.log for every 302 redirects after installing CFP2 on top of 6.3.3. NPR-28606: Backport for CQ-4262844

### UI - Foundation {#ui-foundation}

* Clicking on tag removes global mouseup event and the dialog is frozen in "draggable mode". NPR-28641: Hotfix for CUI-7294

### WCM - MSM {#wcm-msm}

* PushOnModify roll-out for PageManager move commits multiple times from two sessions causing a race-condition. NPR-28880: Hotfix for CQ-4266191

### Vulnerability {#vulnerability}

* CSRF protection framework is not working with AEM foundation forms. NPR-28612: Hotfix for GRANITE-22231

### Forms {#forms-4}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

The key highlights for AEM Forms are:

* Enabled option to select items per page on Policy set view page.
* Added Share queue functionality for all the browsers.

### Forms add-on package {#forms-add-on-package-4}

#### Forms - Workflow {#forms-workflow}

* Shared queue response task open a flash element in the HTML5 workspace. NPR-29161: Hotfix for CQ-4266498
* Unable to submit from Workspace if the button contains Umlaut character. NPR-29014: Hotfix for CQ-4263172

#### Forms - Document Security {#forms-document-security}

* Enable option to select items per page on Policy set view page. NPR-29243: Hotfix for CQ-4268567 & CQ-4265132

#### Forms - Document Services {#forms-document-services-1}

* OSGi Forms Assembler fails to work on Acrobat files. NPR-29049: Hotfix for CQ-4254426

#### HTML5 Forms {#html-forms-2}

* Different behavior is experienced while previewing an XDP as PDF versus same XDP as HTML in Designer. NPR-28602: Hotfix for CQ-4260239

### Forms JEE installer {#forms-jee-installer-3}

* No new AEM Forms fixes in Forms JEE installer.

### OSGI bundles and content packages included in 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

List of OSGi bundles included in AEM 6.3.3.4

[Get File](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

List of Content Packages included in AEM 6.3.3.4

[Get File](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulative Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.3.3.3 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.3 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.16.
* Policy setlist pagination changes to limit 50 records per page. 
* Added rep: cache into Ignorable Nodes at AEM Communities User Sync Listener on publish instances.
* Added aria-label for list and card view button.
* Included an escape character for the comma when any search is performed.
* Enabled support of synthetic resources for content policy.

#### Assets {#assets-5}

* Unable to download multiple files of type .jp2,.max,.oft,.msg. NPR-28002: Hotfix for CQ-4210856
* ImageServer publish settings do not replicate to hybrid delivery. NPR-28329: Hotfix for CQ-4253030

#### Communities {#communities-4}

* Enabled keyboard navigation for AEM Communities Enablement components on Publish. NPR-27739: Hotfix for CQ-4253856
* Enabled keyboard navigation to trigger content play. NPR-27738: Hotfix for CQ-4254026
* Added aria-label for list and card view button. NPR-27736: Hotfix for CQ-4254027
* (Backport) Added rep: cache into Ignorable Nodes at AEM Communities User Sync Listener on publish instances. NPR-27841: Hotfix for CQ-4247234
* The special characters are prefixed with escape character (\) in the search box at UI level. NPR-27839: Hotfix for CQ-4259757
* Error while searching for characters like ( , +,? in quick search. NPR-28212: Hotfix for CQ-4260969
* Unable to delete comments in the User Generated Content using API. NPR-28075: Hotfix for CQ-4260534
* Comments posted to next page gets highlighted with yellow when a new comment is posted. NPR-28148: Hotfix for CQ-4259681
* Can't open messages having attachments in outlook sent and inbox folder. NPR-28559: Hotfix for CQ-4217072

#### Sites {#sites-5}

* Running Version Purge in AEM 6.3 causes a constantly repeated warning in the logs. NPR-27750; Hotfix for CQ-4206870
* The style plugin is not supported in Rich Text Editor full-screen mode. NPR-27622: Hotfix for CQ-4258674
* List 'loaderPromises' is not cleared after the content frame is loaded in editor.js NPR-27768: Hotfix for CQ-4205337
* Unable to set template policy on nested parsys without setting on parent component. NPR-27987: Hotfix for CQ-4246095
* The component browser is not sanitizing user input and hence, can throw javascript errors. NPR-27986: Hotfix for CQ-4247590
* The page appears blank when the user tries to edit the content fragment. NPR-27669
* The annotation highlight disappears as soon as the user clicks on the annotation. BPR-27196: Hotfix for CQ-4254423

#### Integration {#integration-1}

* ResourceResolver not resolving multiple domains for Target Component. NPR-28265: Hotfix for CQ-107847
* LiveCopy inheritance cancellation does not work properly on targeted containers as no actions are shown. NPR-28129: Hotfix for CQ-4259813

#### Replication {#replication-1}

* DispatcherFlushRules break replication in 6.3.3.1 NPR-28150: Hotfix for CQ-4261401

#### Campaign - Targeting {#campaign-targeting-1}

* NullPointerException in TargetedContentManager. Hotfix for CQ-4263485

#### Social - SCORM {#social-scorm}

* Remove reference to Shareable Content Object Reference Model (SCORM) Cloud in the player. Hotfix for CQ-4260779

#### DAM - General {#dam-general}

* Download via link share email returns empty/corrupt zip. Hotfix for CQ-4259686

#### MAC - Test&Target Integration {#mac-test-target-integration}

* Configuring Target Component option is not available for the audiences apart from Default audience. Hotfix for CQ-4261370

#### Translation {#translation-1}

* Enable support for MS Translator service in AEM 6.3 after upgrade of MS Translator to API v3.0. NPR-28365: Hotfix for CQ-4259096

### Forms {#forms-5}

### Forms add-on package {#forms-add-on-package-5}

#### Forms - Workflow {#forms-workflow-1}

* Unable to render PDF Forms on HTML5 workspace. NPR-28059: Hotfix for CQ-4260373

#### Forms - Document Services {#forms-document-services-2}

* Unable to see any Policy Sets beyond the first 1000 listed in the Policy Sets view in the admin console. NPR-28060, NPR-26047: Hotfix for CQ-4249865 
* An exception is thrown with name java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE preventing the short-lived process from completing. NPR-28652

#### Forms - Adaptive Forms {#forms-adaptive-forms}

* Add/remove items in the drop-down list does not update on checking the checkbox items. NPR-28224: Hotfix for CQ-4252834

### Forms - JEE Installer {#forms-jee-installer-4}

* No new AEM Forms fixes in Forms JEE installer.

### OSGI bundles and content packages included in 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

List of OSGi bundles included in AEM 6.3.3.3

[Get File](assets/do-not-localize/6333_bundle_list.txt)

List of Content packages included in AEM 6.3.3.3

[Get File](assets/do-not-localize/content_package_list_6333.txt)

### Cumulative Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.3.3.2 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.2 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see AEM 6.3 Service Pack 3 release notes.

The key highlights of the AEM Cumulative Fix Pack are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.15.
* Added support for the Rules Tab and its enforcement on the Asset Folder into the Folder Metadata Schema.
* Enabled pagination support to group listing page on  publish . 
* Enabled notification unreadCount to be configured with any number. Default value set to 20.
* Fixes in External Link Checker.

#### Assets {#assets-6}

* Cascading dropdown is not supported on dynamic dropdown lists. NPR-27044; Hotfix for CQ-4252564
* Improve query to use ExpiryNotification feature. NPR-26999: Hotfix for CQ-4251188
* Rules migration from Metadata Schema to Folder Metadata Schema. NPR-27771: Backport for CQ-4257737, CQ-4257735, CQ-4259822
* Asset reference adjustment fails to update references for assets which are part of Sling ResourceCollections. NPR-26759: Hotfix for CQ-4252605
* Download via link share email returns empty/corrupt zip file. NPR-27997: Hotfix for CQ-4259686
* Hybrid video encoding does not complete and no thumbnail is created. NPR-27122: Hotfix for CQ-4255080

#### Sites {#sites-6}

* Suspending parent page removes  cq : LiveRelationship mixin type from the missing page. NPR-26996: Hotfix for CQ-4254113
* (External Link Checker) Internal links are shown as broken on individual pages but the same is not working for external links. NPR-27481: Hotfix for CQ-4257780
* Cloud Service Config inheritance is breaking when editing other page properties. NPR-27311: Hotfix for CQ-4256785
* Null Pointer Exception when using a Core Components  form  alongside with a Foundation Form. NPR-27333: Hotfix for CQ-4249176
* Rich Text Editor removes the empty alt tag. NPR-26938: Hotfix for CQ-4253267
* (Classic UI) Performance issues with   selectionchanged   listener in case of multiple dropdowns. NPR-27115: Hotfix for CQ-4237215
* When the rich text editor is combined with multiple fields, the Uncaught TypeError: fieldAPI.getName is not a function at foundation.js error occurs. NPR-27146: Hotfix for CQ-4253155, CQ-4259967
* Focus/Cursor remains on Rich Text Editor even when clicking a radio button in Safari browser. NPR-27144: Hotfix for CQ-4249635
* The page appears as blank when the user tries to edit the content fragment. NPR-27669
* Unable to create a version for Experience Fragments. NPR-27689: Hotfix for CQ-4259009

#### Integration {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever walks the entire tree to gather the available brands. NPR-27060: Hotfix for CQ-4255790
* The   cq  : actions are not considered for a targeted component. NPR-27616: Hotfix for CQ-4257497

#### Sling {#sling}

* When data-sly-use is used with classes with an identical name, the non-compliable code is produced. NPR-27282: Hotfix for Sling-7581

#### Commerce {#commerce-1}

* Update to Apache Felix Http Jetty 4.0.6. NPR-26472: Hotfix for Granite-22916

#### DAM - DM Client {#dam-dm-client}

* An image doesn't show after specifying breakpoints in dynamic media component. Hotfix for CQ-4256168

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet with related video does not sync properly. Hotfix for CQ-4251650
* Video  does not playback in Viewer Preset editor for Mixed Media Set. Hotfix for CQ-4251442

#### DAM - General {#dam-general-1}

* The link to Content Fragment model is missing after applying SP3 patch. Hotfix for CQ-4259029

#### DAM - UI {#dam-ui}

* Folder metadata schema UI is breaking after installing SP3. Hotfix for CQ-4257737

#### Communities {#communities-5}

* Add pagination support for group listing on publish. NPR-26953: Hotfix for CQ-4246525
* Unread count notification cannot be set beyond 21. NPR-27496: Hotfix for CQ-4252829
* User Subscription limit is limited to 1000. NPR-27615: Hotfix for CQ-4254689
* Error observed when uploading an attachment other than image (for example .pdf) in Forum. NPR-27375: Hotfix for CQ-4257753
* Link for replies is not working on row click. NPR-24556: Hotfix for CQ-4256138 
* Relationships to UGC are not deleted upon deletion of UGC. NPR-27631: Hotfix for CQ-4258706
* Unable to search by address value in Keyword search if the community is set with Database Storage Resource Provider (DSRP). NPR-27652: Hotfix for CQ-4253261
* Clicking on the trash icon on the image after delete confirmation removes the attachment permanently. NPR-27340: Hotfix for CQ-4255150
* Forum posts and replies are added on top of the second page and when refreshed, the post moves to the correct location on top of the first page. NPR-27341: Hotfix for CQ-4247338
* Enablement Scorm Resource completion status label appears empty in UI. NPR-27152: Hotfix for CQ-4249994
* On enabling 'Allow privileged', the privileged members should only be able to compose for users who are community members. NPR-27901: Hotfix for CQ-4251235

#### Sustenance {#sustenance}

* Package manager activity logs should be extracted in a separate log file. NPR-27323: Hotfix for Granite-14866

#### Translation {#translation-2}

* Translation preview does not work with  the we .retail sample content. NPR-27170: Hotfix for CQ-4241179

* Proactive platform.login fixes. NPR-26961
* Save and Close on page properties doesn't return to  proper  page in AEM WAR with Tomcat. NPR-27567: Hotfix for Granite-23671

* The Text entered is lost through  sourceEdit  feature once saved. Hotfix for CQ-4259273

### Forms {#forms-6}

### Forms add-on package {#forms-add-on-package-6}

#### Forms - Document Security {#forms-document-security-1}

* Concurrency problem with JEE Client SDK. NPR-27572: Hotfix for CQ-4247156

#### Forms - Document Services {#forms-document-services-3}

* Creating a Form Data Model based on SOAP fails on WebSphere. NPR-27692: Hotfix for CQ-4253702

#### Forms - Adaptive forms {#forms-adaptive-forms-1}

* XML Injection vulnerability with AEM forms. NPR-27863: Hotfix for CQ-4257315
* AEM Forms Container component gets invisible once the wrong form gets configured in sites page and the 'forms cover the entire width of the page' checkbox is selected. NPR-25972: Hotfix for CQ-4239287, CQ-4249133

### Forms JEE installer {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* Creating a Form Data Model based on SOAP fails on WebSphere. NPR-27692: Hotfix for CQ-4253702

#### OSGI bundles and Content Packages included {#osgi-bundles-and-content-packages-included}

List of OSGi bundles included in AEM 6.3.3.2

[Get File](assets/do-not-localize/63332bundle_list.txt)

List of Content Packages included in AEM 6.3.3.2

[Get File](assets/do-not-localize/6332content_package.txt)

### Cumulative Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

AEM Cumulative Fix Pack 6.3.3.1 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 3 (6.3.3.0) in September 2018.

AEM Cumulative Fix Pack 6.3.3.1 is dependent on AEM 6.3 Service Pack 3. Therefore, you must install the AEM Cumulative Fix Pack 6.3.3.x package after installing AEM 6.3 Service Pack 3. For installation instructions, see [AEM 6.3 Service Pack 3 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.14.
* Performance improvements in predicates and search.
* Fixed issue in the FormData handling for the default value.
* Upgraded FormBuilder to the latest Handlebars version.
* Added config servlet for the edit config for the RTE in dialog mode.
* Added support for composite fields.
* Enabled/disabled toolbar items of the Rich Text Editor with a content policy for the edit dialog.

#### Assets {#assets-7}

* With IDS Decoupling enabled, DAM Update Asset workflow does not link references any longer. NPR-26135: Hotfix for CQ-4250933
* Unzipping an archive created by the unarchiver step with a folder having a % in its name does not open. NPR-26275: Hotfix for CQ-4251482
* Single quote character prevents the metadata update. NPR-26808: Hotfix for CQ-4254305
* (Omnisearch) Performance issue when searching within a collection. NPR-26714: Hotfix for CQ-4253408
* Using GQLConverter with a full-text search containing the "OR" letters within the text is incorrectly processed. NPR-26564: Hotfix for CQ-4247362
* Sharing asset link from multi-tenant prepends tenant ID forming an invalid URL. NPR-26482: Hotfix for CQ-4253540
* Disable "Company Root Folder Path" in the Dynamic Media Cloud Configuration UI. NPR-26361: Hotfix for CQ-4249505
* Ingestion of .mos RAW files is prolonged. NPR-26296: Hotfix for CQ-4250661
* Asset Link Sharing does not allow adding more than one internal user with numeric user Id. NPR-26206: Hotfix for CQ-4251466
* Corruption in zip files compressed with the deflate64 algorithm. NPR-26793: Hotfix for CQ-4253995 
* Thumbnail generation process doesn't work correctly for complex PDF files resulting in thumbnails, where part of the image is missing. NPR-26057: Hotfix for CQ-4250944
* Heap memory utilization issue with thumbnail generation. NPR-25545: Hotfix for CQ-4246960
* Creating a large number of relations on an asset causes error. NPR-26309: Hotfix for CQ-4250708
* "Delete Rendition" option does not work and throws an error "nothing to delete." NPR-26007: Hotfix for CQ-4213414
* Unable to delete default values for multi-valued fields. NPR-25116: Hotfix for CQ-4247856
* (DM Hybrid) Catalog replication breaks for AEM 6.3.2 with Dynamic Media. NPR-26406: Hotfix for CQ-4251306

#### Sites {#sites-7}

* Proactive Backport of Sites fixes. NPR-26963
* Tags get created twice when there is a difference in the case type of Title and Name. NPR-26877: Hotfix for CQ-4254134
* Rich Text Editor features in edit dialog are not controlled by policies. NPR-27059, NPR-26750: Hotfix for CQ-4241130
* Client Context segment.js caching vs. non-caching questions. NPR-26622: Hotfix for CQ-4253486
* Segment Rule (/etc/segmentation) activation for child rules in classical causes publish to go down. NPR-26601: Hotfix for CQ-4253588
* Adding 'special character' scrolls the Rich Text Editor dialog to top. NPR-26435: Hotfix for CQ-4249869
* (Touch UI) Toolbar becomes un-usable with multiple Rich Text Editor while switching from fullscreen to  floating  dialog. NPR-25652: Hotfix for CQ-4206008
* Promoting a multi-page launch creates multiple versions for each page. NPR-26810: Hotfix for CQ-4254663
* Tag move operations are not reflected by  structured  content fragment model tag fields. NPR-26801: Hotfix for CQ-4251805
* (Touch UI) Unpublishing the child page from the page editor does not work after renaming the page in the blueprint. NPR-26774: Hotfix for CQ-4254175
* Unpublished  page is not working with references. NPR-26749: Hotfix for CQ-4254372
* Creating variation as live copy requires the user to refresh the page to reflect. NPR-26663: Hotfix for CQ-4254328
* (Classic UI) Going back to the page properties, thumbnail image no longer uses inheritance and disappears from site admin and sidekick and the image is displayed as blank. NPR-26562: Hotfix for CQ-4252346
* When a version of a page is created and a comparison is triggered, the nodes from /content/ versionshistory  are listed in the list of live copies for the Blueprint. NPR-26506: Hotfix for CQ-4243957
* URLs in Experience Fragment Admin Editor does not allow for overlays. NPR-26318: Hotfix for CQ-4252156

#### Platform {#platform}

* Session leak in ReplicationEventListener with test events. NPR-25937: Hotfix for CQ-4251090 
* Replication uses the expired token for OAuth causing multiple errors. NPR-25894: Hotfix for GRANITE-22388

#### Integration {#integration-3}

* TSDK embedded with AEM breaks with an upgrade to Handlebars 4 due to the use of incompatible templates. NPR-26699: Hotfix for CQ-4248974
* Publishing a page with a new asset deactivates the child page from the publish instance without notification. NPR-24869: Hotfix for CQ-4247832
* Replication uses an expired token for  oauth . NPR-25984: Hotfix for Granite-22388

#### Replication {#replication-2}

* Http transport may leak open sessions. Hotfix for Granite-17434
* Exceptions in logs while access token node is being accessed simultaneously by more than one replication agents. NPR-26964: Hotfix for GRANITE-23276, Granite-23155

#### ContextHub {#contexthub}

* The file 'coral.js' includes a vulnerable version of the library 'handlebars.js'. Hotfix for CQ-4255377

#### DAM - DM Client {#dam-dm-client-1}

* Deleting a copy of an image asset makes the original image asset unusable. Hotfix for CQ-4251648
* Redundant download of extra image content from S7 servers. Hotfix for CQ-4248770

#### Granite {#granite}

* AEM OAuth Provider does not perform the case-insensitive search. NPR-26133: Hotfix for GRANITE-22650
* Package Validator does not validate packages included in CFP/SP. NPR-26775: Hotfix for Granite-22825

#### Communities {#communities-6}

* Delimiter issue with search results. NPR-27051: Hotfix for CQ-4248939
* Change the drop-down value from Dallas to Virginia in Adobe Storage Resource Provider. NPR-26936: Hotfix for CQ-4254434
* Enable support for localized title search in SocialTagManager. NPR-26932: Hotfix for CQ-4250276
* Attachment images do not show thumbnail on creating a forum post. NPR-26380: Hotfix for CQ-4253105
* Paste from Word plugin fails to load more than one image. NPR-26728: Hotfix for CQ-4253638 
* Unable to filter the content in the moderation page. NPR-26697: Hotfix for CQ-4213766
* (Security Vulnerability) Account takeover due to JWT misconfiguration. NPR-26440: Hotfix for CQ-4253314
* Retrieving data from Adobe Storage Resource Provider is slow. NPR-26237: Hotfix for NPR-24152
* Private message compose page behaves erratically and sluggishly. NPR-26120: Hotfix for CQ-4250923
* "Mark all read" notification renders only the first 10 as unread without page refresh. NPR-27036: Hotfix for CQ-4254058
* Communities Comment Section Pagination Click and Page Load behavior. NPR-27030: Hotfix for CQ-4251228
* (Forum Search) Back button skips the page and transfers back to forum.html. NPR-26949: Hotfix for CQ-4254804
* Unread Notification does not increase more than 21. NPR-26947: Hotfix for CQ-4251251
* (SearchScheduledPosts job) Add enable/disable switch in ConfigMgr. NPR-26924: Hotfix for CQ-4250463
* Tomcat Context(/aempublish) Path drops when scrolling on the Assignments page. NPR-26919: Hotfix for CQ-4254345
* NullPointerException while creating a group and member. NPR-26778: Hotfix for CQ-4248095
* Moderator unpin and unfeatured content does not work with MySQL Single Responsibility Principle (SRP). NPR-26767: Hotfix for CQ-4251520 
* Search functionality issues with certain characters. NPR-26726: Hotfix for CQ-4247744
* Enable deep links for moderation UI and enablement resources. NPR-26705: Hotfix for CQ-4251381
* Search issue on the forum component. NPR-26577: Hotfix for CQ-4251303
* Searching with the first and last name together in communities messaging does not return the expected results. NPR-26377: Hotfix for CQ-4253150
* Pagination does not update upon removal of replies. NPR-26327
* Deletion of post works but gives an error on console and post remains visible on UI. NPR-26292: Hotfix for CQ-4252803
* The pagination does not update dynamically and the list of replies keep on getting longer. NPR-26145: Hotfix for CQ-4251586
* Group settings do not load on a group that contains 50K~100K users. NPR-25642: Hotfix for CQ-4238426
* Catalog Resource Player failing for context paths. NPR-25640: Hotfix for CQ-4238426
* (Forum Search) - Paginated links to threads with lots of posts do not work on notifications. Hotfix for CQ-4254202
* Moderation console displays only 5 entries with Firefox. Hotfix for CQ-4254128
* Groups are not visible while creating a site. NPR-27148: Hotfix for CQ-4251788
* Null Pointer exception while adding group and members to Role settings and allowing the privileged member in blog function. NPR-21732, NPR-27176: Hotfix for CQ-4255909
* Editing the site and adding members in the role settings throws null pointer exception. NPR-27132: Hotfix for CQ-4255909

#### User Interface {#user-interface}

* Proactive platform login fixes. NPR-26961
* (Multifield) Allow composite items to have custom names. NPR-26493: Hotfix for Granite-20568
* Column view is not updated after pasting a page until refreshed. NPR-26030: Hotfix for CQ-4236346
* Proactive granite.ui.commons fixes. NPR-26960
* Proactive granite.ui.content fixes. NPR-26959
* Proactive CQ/experience log fixes. NPR-26943
* Proactive Foundation UI Backports. NPR-26942
* (IE11) "NaN" is displayed in the number field when typing a negative value. NPR-26701: Hotfix for CQ-100826 
* (Coral. Multifield) Nested multi-fields use the wrong template to create the items. NPR-25649: Hotfix for CUI-6743 
* Update granite coralui2 and coralui3  clientlibs  to remove Handlebars from the build. NPR-25606: Hotfix for Granite-22116

### Forms {#forms-7}

### Forms add-on package {#forms-add-on-package-7}

#### Forms - Document Security {#forms-document-security-2}

* Principal Key Rollover exceptions in server logs for in-active keys. NPR-26748: Hotfix for CQ-4253705
* Unable to create or modify watermark settings of Document Security. NPR-26267, NPR-26129: Hotfix for CQ-4250234

#### Forms - Document Services {#forms-document-services-4}

* PDF/A validation not showing valid with "validate PDF/A. NPR-25934: Hotfix for CQ-4248558

#### Forms - Interactive Communication {#forms-interactive-communication}

* The PDF and HTML Preview of the Letter are visible and functional in the same window when an editable module is edited, saved and then PDF Preview is opened/closed. NPR-26770: Hotfix for CQ-4253217

#### Forms - Workflow {#forms-workflow-2}

* Workspace intermittently hangs and shows the start points repeatedly. NPR-26461: Hotfix for CQ-4253439
* ESAPI exception is thrown in the logs when braces are used in the task name. Hotfix for CQ-4256627
* Null pointer exception is thrown when non-prefilled adaptive form/formset associated start point is opened. Hotfix for CQ-4256124
* Unable to send email using the global setting. NPR-26163: Hotfix for CQ-111110
* Unable to open workspace after applying axis.jar file. NPR-26131: Hotfix for CQ-4251126
* The refresh button fails to sync the latest data from the server to Adaptive forms. Hotfix for CQ-4255670
* Setting search template from admin UI and then using the same for searching the task in AEM Forms workspace throws an exception. Hotfix for CQ-4255649
* Tracking details of the processes under the applications with parentheses symbol in the name are not displayed in HTML workspace. Hotfix for CQ-4242101
* Saving changes in preferences screen of the HTML Workspace throws an exception. Hotfix for CQ-4241485
* Bulk approval is broken on the latest JEE setup. Hotfix for CQ-4241486
* Draft of task/start point is failing on latest 6.4 JEE server. Hotfix for CQ-4241484
* Set Date().getTime().toString parameter to initialize session instead of Date.toString(). Hotfix for CQ-4241483
* While opening /lc/ws, a vulnerable character exception is observed in HTML parameter. Hotfix for CQ-4241481

#### Vulnerability {#vulnerability-1}

* Stored Cross-Site Scripting (XSS) vulnerability in the notes tab of the Forms Manager. NPR-27157: Hotfix for CQ-4255556

### Forms JEE installer {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Code review for Enterprise Security API. Hotfix for CQ-4255638
* Failed to load esapi.properties as classloader resource in WAS9. Hotfix for CQ-4255631
* Clicking on Add Authentication during Domain Configuration throws an error. Hotfix for CQ-4255634
* Forms JEE Supports PKCS#11 Mutual Authentication. NPR-21372
* Fixed the issues reported in static code analysis of Core. Hotfix for CQ-104446
* Deployment of adobe.livecycle.weblogic.ear and adobe.livecycle.websphere.ear is failing while running LCM. Hotfix for CQ-4255629, CQ-4255630
* Invalid error messages in the Application Management. NPR-23289: Hotfix for CQ-4233163, CQ-4255636
* Clicking on Add Authentication during Domain Configuration results in an error. Hotfix for CQ-4255634

#### Forms - JEE Connector {#forms-jee-connector}

* Fixing the issues reported in static code analysis of Connector. NPR-22260

#### PDFG Service {#pdfg-service-1}

* org.jgroups.Message error in the logs after upgrading from LiveCycle to AEM 6.2 forms. NPR-26795: Hotfix for CQ-4220415
* AEM forms - Error while migrating styles. Hotfix for CQ-4251969
* Fixed the issues reported in static code analysis report of PDFG. NPR-23251: Hotfix for CQ-4213930

#### OSGI bundles and content packages included in 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}

List of OSGi bundles included in AEM 6.3.3.1

[Get File](assets/do-not-localize/63sp3cfp1bundlelist.txt)

List of Content Packages included in AEM 6.3.3.1

### Cumulative Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

AEM Cumulative Fix Pack 6.3.2.2 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 2 (6.3.2.0) in April 2018.

AEM Cumulative Fix Pack 6.3.2.2 is dependent on AEM 6.3 Service Pack 2. Therefore, you must install the AEM Cumulative Fix Pack 6.3.2.x package after installing AEM 6.3 Service Pack 2. For installation instructions, see [AEM 6.3 Service Pack 2 release notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp2-release-notes.html).

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.11.
* Enabled subassets and multipage asset viewer on Brand Portal.
* Changed length of field type to 255 to support all possible mime types for the different type of attachments.
* Configured error message from the server when an image violates the upload criteria.
* Added STARTTLS support in Day CQ Mail Service.
* Update to latest versions of cq-wcm-content and com.adobe.cq.launches.it.serverside.
* Update com.adobe.granite.ui.coralui3-rte to latest version released.
* Ensured render condition returns a sane result if  expressionResolver  is null.
* Coral.ColumnView: Added support for shift+click.

### Assets {#assets-8}

* Asset Folder Closed User Group (CUG) field does not return the 'everyone' group. NPR-23163: Hotfix for CQ-4239377
* Search for smart collection saved searches does not return all results. NPR-23243: Hotfix for CQ-4240355
* (ExpiryNotificationJobImpl) Optimization of the existing query. NPR-23330: Hotfix for CQ-4205249
* (Metadata profile) Standard tag values set at the time of creation are not available after saving. NPR-23370: Hotfix for CQ-4235458
* (Touch UI) Unable to move multiple assets due to JS error. NPR-23395: Hotfix for CQ-4241279
* Mismatch in the download size versus the information displayed is incorrect leading to confusion for the users. NPR- 23418: Hotfix for CQ-4242774
* Extracted mimetype for file extension LSR and SKETCH is incorrect and leads to invalid file download. NPR-23644: Hotfix for CQ-4243260
* (Firefox/Chrome) Unable to download assets in Asset Share page. NPR-23963: Hotfix for CQ-4244391
* Asset admin search facets disappear in search panels after previewing. NPR-23964: Hotfix for CQ-4244410
* Unpublish the search form removes the default search form completely. NPR-23291: Hotfix for CQ-4241382
* (Brand Portal) Search in directory predicate should be filtered out on replication. NPR-23292: Hotfix for CQ-4241385
* Publish to Brand Portal UI action is not available. NPR-23293: Hotfix for CQ-4241161
* Publish/Unpublish to Brand Portal button should not be available for content fragments. NPR-23318: Hotfix for CQ-4245086
* (Brand Portal) Enable creation of sub assets when an asset is published. NPR-23331: Hotfix for CQ-4242018
* Dynamic Media requests don't use proxy/HTTP common client. NPR-10727: Hotfix for CQ-45695, CQ-88800
* Unable to annotate single rendition MP4 Video Asset in Dynamic Media S7 (DMS7). NPR-22046: Hotfix for CQ-4215912
* EmbedXMP data is always set to “active” for Ptiff generation process. NPR-22903: Hotfix for CQ-4234498
* Dynamic Rendition display / selection issues with large Image Preset count. NPR-23151: Hotfix for CQ-4217511
* Issue with Dynamic Media Encode Video - Modification / Reupload launcher. NPR-23237: Hotfix for CQ-4240260
* Proxy handling fix for HTTP forwarder in Dynamic Media S7. NPR-24001: Hotfix for CQ-244140

### Sites {#sites-8}

* Query Builder discrepancies resulting different xPath translation between 6.2 and 6.3. NPR-23245: Hotfix for CQ-4240396
* Thumbnail tab in page property does not work on extending the dialog. NPR-22844: Hotfix for CQ-4241474
* Parsys breaks the emulator device frame width and crops off any component added into it. NPR-22926: Hotfix for CQ-4238224
* When executing the multiple launches, the launch promotes in Author but the changes don’t get replicated on the Publish server due to lack of replication permissions. NPR-22934: Hotfix for CQ-4234746
* A page locked by a user in the first session can be modified by another user in another session. NPR-23057; Hotfix for CQ-4199017
* Fix re-orderable option in List View. NPR-23065: Hotfix for CQ-4239321
* (Page Editor) Image on an Image component disappears when opening dialog box again. NPR-23156: Hotfix for CQ-4239978
* Template Editor only showing up 20 templates/folders and does not load the other ones when scrolling to the bottom of the page. NPR-23185: Hotfix for CQ-4238483
* (Classic UI) An error is generated while moving or renaming the pages. NPR-23213: Hotfix for CQ-4240971
* Unable to edit/create ContextHub segments. NPR-23218: Hotfix for CQ-4226948
* (Rich Text Editor) - Replace operation changes the format of a word. NPR-23271: Hotfix for CQ-4239677
* Rollout button is missing in the Blueprint Tab for XF Variations. NPR-23320: Hotfix for CQ-4240404
* Classic UI does not work to edit CUG due to deprecation. NPR-24122: Hotfix for 4241823
* Proactive fix to protect against unwanted content promotions. NPR-24387: Hotfix for 4244993
* Once approx. 80 fragments are added in a folder in Assets, errors encountered when workflow is triggered from Timeline console. NPR-23393; Hotfix for CQ-4211216
* Unable to drag and drop images into the Rich Text Editor dialog from content finder. NPR-23403: Hotfix for CQ-4242094
* 'Invalid recursion selector value' error while migrating a component from AEM 6.0 to AEM 6.2. NPR-23532: Hotfix for CQ-4241258 
* (Rich Text Editor) Tooltips show variable name of plugin instead of the readable plugin name. NPR-23550: Hotfix for CQ-4243269
* Unable to save dialog with required select dropdown in mobile/tablet version. NPR-23904: Hotfix for CQ-4243096
* Style system options appear on all pages post 6.3.2.1 installation. NPR-23972: Hotfix for CQ-4244394
* Classic UI does not work to edit CUG due to deprecation. NPR-24122: Hotfix for 4241823
* Proactive fix to protect against unwanted content promotions. NPR-24387: Hotfix for 4244993
* Asset references are not updated when assets are moved. NPR-23208: Hotfix for CQ-4239879

### Platform {#platform-1}

* Smart collection doesn't display results after save if using tags predicate in the search facet. NPR-23401: Hotfix for Granite-21278
* Patch jQuery 1.12.4 from clientlib to include security fix. NPR-24128: Hotfix for Granite-20058
* Internationalization translations are not updated unless bundle is restarted. NPR-23193: Hotfix for Sling-7190
* Unclosed resource resolver in ReplicationEventListener. NPR-23240: Hotfix for CQ-4241350
* Support STARTTLS in "Day CQ Mail Service.” NPR-23941: Hotfix for CQ-4240397
* JCR complaint tag name should be auto-populated based on Tag Title. NPR-24173: Hotfix for CQ-4199411

### Integration {#integration-4}

* (Target) Campaigns are not activated when using API type as XML. NPR-23199: Hotfix for CQ-4240936****
* Configuration reference replication fails with intermediate folder structure. NPR-23485: Hotfix for CQ-4242751

### Vulnerability {#vulnerability-2}

* Salesforce integration is vulnerable to Server Side Request Forgery (SSRF). NPR-24289: Hotfix for CQ-424527
* Cross-site scripting (XSS) in Admin UI Project links. NPR-23272: Hotfix for CQ-4241795

### WCM - Foundation Components {#wcm-foundation-components}

* Foundation table is vulnerable to Stored Cross Site Scripting. NPR-23214: Hotfix for CQ-4240760

### Translation {#translation-3}

* Live copy properties not deleted while creating language copies. NPR-23123: Hotfix for CQ-4230641

### User Interface {#user-interface-1}

* DatePicker doesn’t support manually set external type hint set by hidden field. Changing the type hint gets a conversion error. NPR-23371: Hotfix for Granite-21194
* Coral.ColumnView: Add support for shift+click. NPR-23404: Hotfix for Granite-13338
* Select RT doesn't validate when item with empty value is selected. NPR-23405: Hotfix for Granite-21283
* (OMEGA) Report "Feature" in English only. NPR-23990: Hotfix for Granite-21231
* Fixes to Coral.Autocomplete API. NPR- 23516

### Granite {#granite-1}

* Apache Http client tracking connections and high heap utilization cause AEM server to crash. NPR-23906: Hotfix for Granite-21056

### Commerce {#commerce-2}

* Campaign json output does not contain servlet context root. NPR-23733: Hotfix for CQ-4243827

### Communities {#communities-7}

* Search on communities is failing for few words. NPR-23256: Hotfix for CQ-4240717
* Unable to assign groups for community managers role issue. NPR-23317: Hotfix for CQ-4241233: CQ-4221399
* Issues in Resource creation with similar assets name. NPR-23319: Hotfix for CQ-4240700
* (ContextPath) Breaking message functionality breaks for Jetty configs and error while searching group members in community group member list. NPR-23336: Hotfix for CQ-4241519, CQ-4242080
* Uploading an image to a Communities Forum does not appear in Adobe Storage Resource Provider (ASRP). NPR-23397: Hotfix for CQ-4242497
* Deleted ideas show as active links in Activities. NPR-23406
* imsmanifest.xml can't be loaded with AEM running with context root. NPR-23483: Hotfix for CQ-4242193
* Security vulnerabilities in an older version of Handlebars. NPR-23518: Hotfix for CQ-4243055
* Tunnel service is not working. NPR-23543: Hotfix for CQ-4242217
* Issues with communities components when accessed through dispatcher and sling dynamic include enabled to it. NPR-23586: Hotfix for CQ-4242360, CQ-4241522
* When searching for a search term that produces many results through search and then entering a new search term, the paging is not reset. NPR-23739: Hotfix for CQ-4222593
* Issues while performing  search  on the forum component. NPR-23838: Hotfix for CQ-4243770 
* (Communities Moderation Flagging) Bulk Allow of flagged messages is not working. NPR-23845: Hotfix for CQ-4243962
* Sort button text not showing up the default selected  value  inspite   of selecting the default sorting order. NPR-23881: Hotfix for CQ-4243375
* Web and mail notifications do not get triggered due to message failure to the groups. NPR-23934: Hotfix for CQ-4242880
* No details on the flag users and reasons are displayed using DSRP configuration. NPR-23973: Hotfix for CQ-4243205
* Flag reasons from users that are unflagged remain visible/ NPR-23974: Hotfix for CQ-4243822
* Attaching two files with the same name twice to a form post leads to a server error. NPR-24166: Hotfix for CQ-4244367
* Unable to store attachments with mime types more than 15 characters using Database Storage Resource Developer (DSRP). NPR-24174
* When an image that violates the upload criteria is dragged and dropped into the post text, a server error is thrown, and a generic error message is displayed to the user. NPR-24243
* Fixes to several AEM Communities server-side issues. NPR-23971: Hotfix for CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Fixes to several Adobe Social issues. NPR-24242: Hotfix for CQ-4245054, CQ-4245120, CQ-4245296

### Campaign {#campaign}

* Campaign json output does not contain servlet context root. NPR-23733: Hotfix for CQ-4243827

### MSM {#msm}

* When rolling out the page, the livecopy does not show the on/off time properties inherited from the master. NPR-23873: Hotfix for CQ-4243431
* LiveCopy operation does not ignore child nodes of deleted components. NPR-23058: Hotfix for CQ-4211662

### Offloading {#offloading}

* Request for mechanism to clean up assets from the worker instances after processing or on a regular basis. NPR-23638: Hotfix for Granite-21337

## Forms {#forms-8}

### Forms add-on package {#forms-add-on-package-8}

#### Adaptive Forms {#adaptive-forms-1}

* Move ReCaptchaConfigService to internal package. Hotfix for CQ-4217459
* Numeric field doesn't respect minimum value. NPR-23967: Hotfix for CQ-4244830
* Support of Multi Shard in Adaptive Forms integration with AdobeSign. NPR-23383

#### Backend Integration {#backend-integration}

* (FDM) (WebService) Supporting the extensions construct of WSDL in WSDL Parser. NPR-23640, NPR:23236: Hotfix for 4205821
* To include SDLInvokerParams in Forms Add-on Client SDK. NPR-23157

### Forms JEE Installer {#forms-jee-installer-7}

#### Process Management {#process-management}

* Unable to open workspace after applying the new axis.jar file. NPR-23316
* LiveCycle vulnerable to XSS on PMAdmin. NPR-23267
* After upgrading to AEM 6.1 Forms, HTML Workspace freezes on accessing Task List for specific users. NPR-23943

#### Core {#core}

* Forms JEE Supports PKCS#11 Mutual Authentication. NPR-21372

#### PDFG Service {#pdfg-service-2}

* The Paper capture service is crashing while concurrently processing of TIFF files ( around 50 KB size ). NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server Output - Alternative description missing for annotations. NPR-22207
* Add PDF/UA support to XML forms generated via Designer and Output Service. NPR-23132

### OSGI bundles and content packages included in 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

List of OSGi bundles included in AEM 6.3.2.2

[Get File](assets/do-not-localize/6_3_2_2_bundle-list.txt)

List of Content Packages included in AEM 6.3.2.2

[Get File](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulative Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

AEM Cumulative Fix Pack 6.3.2.1 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 2 (6.3.2.0) in April 2018.

The key highlights of the **AEM Cumulative Fix Pack** are:

* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.10.
* Improved rendering of Parsys components in Classic UI.
* Updated sling models bundles to include character set fix.
* Made publish to Brand Portal async for all assets types.
* Updated coralui-component-richtexteditor.git from 0.1.15 to 0.1.16
* Fixes in show/hide functionality of drop-down component.
* Enabled image flipping for the Core Image Component.
* Updated  felix   http  bundles to enable session attributes.

* Removed cache=true on Sling Models due to memory consumption issues.

### Assets {#assets-9}

* When changing the title or thumbnail picture in Asset Folder settings, the original group and permissions of the folder are overridden. NPR-22171: Hotfix for CQ-4216080
* UI throws false error "Publish to Brand Portal failed" whereas job is added to Replication queue and assets are published to Brand Portal. NPR-22179: Hotfix for CQ-4205273
* (Touch UI) Default upload location for assets in column view. NPR-22465: Hotfix for CQ-4237057
* AEM throws StackOverflow error when trying to copy an asset schema from /conf/global to /conf/ mytenant . NPR-22489: Hotfix for CQ-4235875
* Attempting to unzip a ZIP archive fails due to trailing space at the end of the folder name. NPR-22522: Hotfix for CQ-4238036
* Sorting using Asset title column does not work for search results. NPR-22908: Hotfix for CQ-4239076
* Youtube video is tagged with the full path instead of the tag name itself. NPR-22976: Hotfix for CQ-4238669
* Reordering of folders under a re-orderable folder is not persisted. NPR-23125: Hotfix for CQ-4231761
* HTTP 504: Gateway Timeout error when trying to share collections using share link. NPR-21928: Hotfix for CQ-4234507
* PDF keyword metadata is not properly extracted and modified incorrectly when there are multiple keywords associated with a PDF Asset. To resolve the issue, the Subject field metadata property has been removed for PDF Assets. However, you can edit the metadata schema to add a multi-value text field for the Subject field. NPR-21972: Hotfix for 4215741****
* Wrong assets are deleted if the selected folder is changed between the time the 2 popups are displayed. NPR-21980: Hotfix for CQ-4233675
* (DAM) Multiple cross-site scripting (XSS) vulnerabilities while adding to collection wizard. NPR-22432: Hotfix for CQ-4327086
* Asset download fails when using Digital Rights Management in Assets on Safari. Users unable to download assets with disclaimer and long filenames. NPR-22747: Hotfix for CQ-4236460 and CQ-4235274
* Make public share as default option while publishing assets to Brand Portal. NPR-21931: Hotfix for CQ-4218816

### Sites {#sites-9}

* New item in Workflow inbox shows page path instead of  title  of the page. NPR-21634: Hotfix for CQ-4230672
* Editable structure components lose CSS class names needed for the responsive grid when edited. NPR-21741: Hotfix for CQ-4232374
* (TouchUI) Multiple cross-site scripting (XSS) vulnerabilities for HTL components. NPR-21899: Hotfix for CQ-4232511
* Unable to change content fragment mixed-media image resource type. NPR-21907: Hotfix for CQ-4233401
* RTE Fullscreen For the Touch UI Dialog is Hiding the RTE plugins. NPR-22034: Hotfix for CQ-4235457
* (Touch UI) Rich Text Editor removes all attributes other than id from &lt;a&gt; tag. NPR-22044: Hotfix for CQ-4234133
* Multiple stacked Parsys due to long-running queries (more than 6) makes AEM sluggish. NPR-22134: Hotfix for CQ-4233904
* Unable to change permissions on nodes having colons in the name. NPR-22136: Hotfix for CQ-4236221
* (Classic UI) Rich text editor output  html  adds 'list-position-style: inside;' as inline style to the &lt;ul&gt; tag. NPR-22145: Hotfix for CRTE-114
* Make TreeNode fallback to the name attribute when text is empty. NPR-22146: Hotfix for CQ-4234724/CQ-4236300
* RSS Feed issues, port -1 to AEM 6.3. NPR-22176: Hotfix for CQ-4233339
* (Classic UI) Pasting text shortcut (Ctrl+V) does not work for OOTB Text (Rich Text) component. NPR-22224: Hotfix for CQ-4236224
* Tagfield's  filtering is not working as expected on typing the text. NPR-22236: Hotfix for CQ-4236655
* (Page Editor) When pasting text data in image map component, Text component also gets pasted when pasting text data in image map component. NPR-22264: Hotfix for CQ-4236230
* Dialog FileUpload field required causes problems in dialog submission. NPR-22464: Hotfix for CQ-4222192
* Moving w/o replication permissions starts a request for activation workflow if the moved page or its referrers cannot be activated. NPR-22467: Hotfix for CQ-4211765
* Performance issues when loading a page with large (2000+) audiences. NPR-22478; Hotfix for CQ-4209567
* Persistence issues when ContextHub stores overwrite default persistence layer during initialization. NPR-22479: Hotfix for CQ-4218399
* Launch with multiple pages does not publish subpages to publish servers if "include subpages" is not checked on  first  content root. NPR-22482: Hotfix for CQ-4237818
* (Touch UI) Deletion of launches via Classic UI console make all pages uneditable. NPR-22491: Hotfix for CQ-4225074
* Issues with Image component due to extra space in  dialog . NPR-22528: Hotfix for CQ-4238183
* While opening the component using  inlide  mode, plugins loaded previously are not visible the second time. NPR-22591: Hotfix for CQ-4236850
* Deleting a launch in a nested launch causes sub-launches to become orphaned. NPR-22621; Hotfix for CQ-4202639
* (Classic UI sidekick) Workflow tab is disabled when the page is in workflow lock stage. NPR-22722: Hotfix for CQ-4237557
* After flipping an image added in the image component on a page, the changes are not saved and  original  image is displayed on the page. Rendering support has been added to the image core component via [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: Hotfix for CQ-4221539
* When the user tries to delete the existing anchor from the anchor menu, Rich text editor component window gets closed and the changes remain unsaved. NPR-22802: Hotfix for CQ-4238167
* Omnisearch filter does not show all actions in Sites console. NPR-22804: Hotfix for CQ-4239007
* Issue  with Copy/Paste in Touch UI with OS Clipboard and internal AEM Clipboard. NPR-22807: Hotfix for CQ-4220383
* Inconsistency in the Excerpt highlighting returned by Lucene Search. NPR-22879: Hotfix for CQ-4238513
* Activating a page with  publish  instances off results in green status instead of turning to amber. NPR-22927: Hotfix for CQ-4236310
* (StyleSystem) Screen position jumps while selecting  style  from the pop-up. NPR-23183: Hotfix for CQ-4238867
* (Manage Publication) Move to next month of calendar requires multiple clicks. NPR-23508: Hotfix for CQ-4242732

### Platform {#platform-2}

* Sling Exporter servlet does not export Japanese characters correctly. NPR-22153: Hotfix for CQ-4228920
* Scheduler deadlock during startup. NPR-22440: Hotfix for Sling-7004
* Unable to sync groups between two publish instances. NPR-21943: Hotfix for Granite-19564
* Performance issues with org.apache.sling.i18n shared session/resource resolver. NPR-23390: Hotfix for Sling-7543

### Integration {#integration-5}

* Unclosed ResourceResolver in com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix for CQ-4236515
* TargetContentImpl makes AEM sluggish during long running queries. NPR-22361: Hotfix for CQ-4236907
* Target engine (mbox.js, at.js) does not use mangled URLs and uses URLs containing colons which might fail with certain deployments. NPR-22366: Hotfix for CQ-4237854
* When supplying a custom at.js or mbox.js, the include script is getting written to page as text instead of HTML tags. NPR-22441: Hotfix for CQ-4203691
* In Target mode, Authors can modify a component inherited from the blueprint without cancelling the inheritance. NPR-22751: Hotfix for CQ-4237907
* The PersonalizationDataSource throws a Null Pointer Exception due to missing  jcr : content node. NPR-22850: Hotfix for CQ-4222122
* AEM targeting fails when using  non  English language. NPR-22917: Hotfix for CQ-4218213
* Publishing a page with targeted content is missing related resources. NPR-23064: Hotfix for CQ-4227119
* Users are not able to see test Static Param values in the  mbox  call which can be seen when testing with AT.js as the client library in cloud configuration. NPR-21930: Hotfix for CQ-4234520

### WCM-Foundation Components {#wcm-foundation-components-1}

* iParsys creates the position shift after unchecking cancel/disable inheritance checkbox. NPR-21905: Hotfix for CQ-4230951
* Show/Hide functionality of the form drop-down component is not working as expected. NPR-22327: Hotfix for CQ-4222853
* CAPTCHA Component has been deprecated for better security, if you are using CAPTCHA component, then message "Captcha component is deprecated and should no longer be used." will be displayed after installing 6.3.2.1 or later release. AEM component can be customized to include reCAPTCHA for better security NPR-22151: Hotfix for CQ-4220052

### WCM - Page Editor {#wcm-page-editor}

* Reflected Cross-site scripting (XSS) when using an invalid selector. Hotfix for CQ-4270397

### Translation {#translation-4}

* Investigate issues with Preview functionality. NPR-22114: Hotfix for CQ-4223753

### User Interface {#user-interface-2}

* Issues with Coral Calendar month picker when 'min' and 'max' date range is set. NPR-22716: Hotfix for CUI-7187
* (Classic UI) Component displays the default values even if the associated form data model service is set to empty field. NPR-22272: Hotfix for GRANITE-19744

### Granite {#granite-2}

* Stability issues with Asset Share AEM publisher instance caused by  memory  leak. NPR-22205, NPR-23178: Hotfix for Sling-5668, Sling-7292 and Sling-7470.
* Unstable service id should not be used for session attribute names. NPR-22821: Hotfix for Granite-21059
* When  a  http   whiteboard managed session is invalidated, the container session is also invalidated if the session has no other session attributes. NPR-23059: Hotfix for FELIX-5819
* LogbackManager may miss out some OSGi config at time of startup. NPR-23060: Hotfix for Granite-19791

### Commerce {#commerce-3}

* Enable creating workflow in Experience Fragments menu. NPR-22347: Hotfix for CQ-4221661
* Experience Fragments errors reproducible on WeRetail. NPR-21958: Hotfix for CQ-4220061
* Activating a page containing a deleted experience fragment throws a NullPointerException. NPR-23179: Hotfix for CQ-4239939

### Projects {#projects}

* (Multi-language project) Project does not list translation jobs for more than 19 languages. NPR-22498: Hotfix for CQ-4229978

### Workflow {#workflow}

* (Classic UI) Enabling or disabling a workflow launcher leads to bad behavior. NPR-22907: Hotfix for CQ-4239153

## Forms {#forms-9}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

The key highlights for AEM Forms are:

* Added support for HTML5 Input Type.
* Fixed Basic SOAP Header Authentication. 
* Added support for title attribute for hyperlink.
* Enabled PDF/UA Identifier in the accessibility tree of Forms Designer.
* Enabled certificate authentication for Workbench users.
* Added support to produce PDF files which are PDF/A-2a or PDF/A-3a compliant.

### Forms add-on package {#forms-add-on-package-9}

#### Forms-Admin UI {#forms-admin-ui}

* Password is visible in plain text on inspecting password field for ECM Connectors Configuration pages. NPR-22508: Hotfix for CQ-4236065

#### Forms Service {#forms-service}

* When SSL is enabled, Submit and Abandon events do not work with Form Analytics. NPR-22637; Hotfix for CQ-4237973

#### User Management {#user-management}

* Unable to synchronize LDAP due to incorrect cglib-nodep version. NPR-22493: Hotfix for CQ-4234099

#### Adaptive Forms {#adaptive-forms-2}

* Custom functions for rule editor are adding an extra; after  function  call, hence, failing the validation even though the custom function returns true. NPR-22481: Hotfix for CQ-4235499
* Irrespective of date pattern selected, date-Picker component does not follow the pattern when displaying minimum and maximum validation messages. NPR-22444: Hotfix for CQ-4236269
* The date format being sent in submit request should align to the pattern provided in the date-picker component. NPR-22384
* The specified maximum number of characters for an adaptive form text box is not honored on Android 6.0 Samsung devices. NPR-22363, NPR-22364: Hotfix for CQ-4235205
* (Microsoft Edge) (IE11) Adaptive Form text-field component having multiline field displays 'Null' as default value instead of blank. NPR-22284: Hotfix for CQ-69107
* SOAP UTF-8 Input Encoding in Adaptive Forms returns errors with garbled page. NPR-20105: Hotfix for CQ-4222669
* AEM Forms Container Component is not available to edit once wrong form is configured in sites page. Hotfix for CQ-4237456
* Development tests are failing when executed on JEE servers. Hotfix for CQ-4222082
* AF tests failing on JEE servers due to minification issues in Calvin framework. Hotfix for CQ-4217220

#### Forms Manager {#forms-manager}

* (Firefox) Unable to update XML Schema properties of Adaptive Forms as the options in the Document of Record (DOR) are not coming as pre-selected in the properties page. NPR-22298: Hotfix for CQ-4237402
* Forms that are modified after publishing the page do not get published again on publishing the site. NPR-23013: Hotfix for CQ-4236566

#### Backend Integration {#backend-integration-1}

* OOTB basic authentication for SOAP services does not work for basic authentication in FDM integration. NPR-23238: Hotfix for CQ-4241308

#### Correspondence Management {#correspondence-management}

* The OOTB XDPs, when used inside the letter and previewed, shows the content overlapped with the footer. Hotfix for CQ-4212414

#### Assembler Service {#assembler-service}

* Discrepancy  between Acrobat DC and AEM reports about PDF/A-1b compliance check error. NPR-22051, NPR-22050: Hotfix for CQ-4226128, CQ-4227671

### Forms JEE installer {#forms-jee-installer-8}

#### Workbench {#workbench}

* Enabled certificate authentication for Workbench users. NPR-20644: Hotfix for CQ-4214486
* Downloading server log using Workbench works only for one server while for the other server, it does not work. NPR-21079: Hotfix for CQ-4229842

#### Process Management {#process-management-1}

* (HTML Workspace) Screen size issues with scroll bars. NPR-23288
* (HTML Workspace) Process Startpoints are not sorted in alphanumerical order. NPR-22841 Hotfix for CQ-4238944
* (HTML Workspace) Prepare Data gets triggered on closing of form in workspace. NPR-21127: Hotfix for CQ-4224574
* (HTML Workspace) When invoking a process that requires notes with long descriptions, the Notes expand button does not work. Hotfix for CQ-4241488

#### Core {#core-1}

* Error encountered at startup while starting the Scheduler. NPR-22990
* Prevent browsers from storing credentials entered into HTML forms. NPR-21762: Hotfix for CQ-4206543
* The issues reported in the static code analysis of Core should be fixed. Hotfix for CQ-104446

#### PDFG Service {#pdfg-service-3}

* PDF Generator fails to produce PDF documents with specified bookmarks levels. NPR-22921, NPR-22285: Hotfix for CQ-4230562
* Added support to produce PDF files which are PDF/A-2a or PDF/A-3a compliant. NPR-23021: Hotfix for CQ-4214172

#### Forms Designer {#forms-designer-1}

* PDF/UA Identifier is missing when saved as PDF from Designer. NPR-23137
* Path objects, for example: borders, underlines, and hyperlinks, are not getting tagged when saved as PDF from Designer. NPR-23136
* Image Object has no bounding box when saved as PDF from Designer. NPR-23134
* inline Hyperlinks defined in Designer do not get tagged nor they have alternate text when saved as PDF from Designer. NPR-23133
* Opening the XML Data Package with AEM 6.3 Forms Designer removes XHTML formatting from the XML source. NPR-21178: Hotfix for LC-3917046

#### Install LCM {#install-lcm}

* Update Jsafe Jars to Cryptoj 6.1.3.1 in installer and LCM. NPR-21370

#### Signatures Service {#signatures-service}

* Exception encountered while trying to digitally sign/certify a PDF document via HSM. NPR-21154: Hotfix for CQ-4226978

### OSGI bundles and content packages included in 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}

List of OSGi bundles included in AEM 6.3.2.1

[Get File](assets/do-not-localize/bundle-list_002_.txt)

List of Content Packages included in AEM 6.3.2.1

[Get File](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 1 (6.3.1.0) in October 2017.

The key highlights of the AEM Cumulative Fix Pack are:

* Modified UI to support implementing CUG functionality in AEM Assets.
* Fixed UI issues on license check page for better experience.
* Enabled OSGi workflow task support in AEM Forms App.

### Assets {#assets-10}

* Modified UI to support implementing CUG functionality in AEM Assets. NPR-19485
* Uploading an asset as a direct child node of itself using the Touch UI causes an issue. The asset is uploaded as a direct child of the previously selected asset. NPR-19736  
* Date Range predicate and Range predicate do not work when loading a saved search/Smart collection. NPR-19844: Hotfix for CQ-4220808  
* AEM instance becomes sluggish when multiple assets (more than 4) are being published to Brand Portal. NPR-20009: Hotfix for CQ-4213426  
* Unable to download assets with spaces from license check page. NPR-20067: Hotfix for CQ-4216557  
* Processing issues when uploading PSB files with multiple alpha layers. NPR-20250: Hotfix for CQ-4220869  
* Users unable to download assets with long filenames and disclaimer defined. NPR-20254  
* ProductAssetsUploader leaves the temporary files of JAVA cache in Java TEMP folder. NPR-20256: Hotfix for CQ-4221801  
* Replace version comparison code with Adobe proprietary code due to licensing issues. NPR-20272: Hotfix for CQ-4223758  
* The metadata for a string property, documentNumber shows up as a date whereas it should be a number. NPR-20291: Hotfix for CQ-4223991  
* Text extraction gets stuck for a corrupt PDF. NPR-20416: Hotfix for CTG-4150375  
* Compressed files that include assets with  non  UTF-8 compatible names are not downloaded correctly. NPR-20420: Hotfix for CQ-4219961
* Too many characters in OmniSearch causes AEM server to crash. NPR-20434: Hotfix for CQ-4223602  
* DAM Asset API metadata defect breaks the  xmp -write-back APIs. NPR-20607: Hotfix for CQ-4220455
* Performance issues while adding users to collections. NPR-20699: Hotfix for CQ-4225733  
* Publish to Brand Portal from AEM should not be allowed for Dynamic Media sets. NPR-20320: Hotfix for CQ-4221147  
* Video with spaces and accent yields no video for the Renditions page. NPR-19961: Hotfix for CQ-4221014  
* Resolved multiple folder handling issues with Assets APIs. NPR-20569
* AEM Dynamic Media Classic (former Scene7) fails to sync assets from AEM server when the destination path in the cloud service configuration points to a subfolder in the root path. CQ-4228265
* Email bundle of apache commons `{org.apache.commons/commons-email/1.5}` has been added replacing `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`.

### Sites {#sites-10}

* Admin Permission issues: Unable to remove Closed User Group members from page properties. NPR-20631
* Typed workflow name should be available in Notification box when publishing page through Manage Publication. NPR-20046: Hotfix for CQ-4221586  
* Applying styled text on two rows in Rich Text Editor and then merging them into one paragraph removes the styled spans. NPR-20110: Hotfix for CQ-4223051  
* Changes made to field properties in multiple tabs in the Property edit dialogue sometimes do not get saved. NPR-20286  
* Unexpected tag at the end of the pasted content in Content fragment. NPR-20413: Hotfix for CQ-4224014  
* Implemented a mechanism in Adobe Campaign to fetch the policy of a content resource from an external targeting resource. NPR-20667  
* Richtext plugin is not working for both inline and fullscreen bar in multifield Touch UI. NPR-20973

### Campaign {#campaign-1}

* Placeholders are not visible in a page that contains multiple parsys components. NPR-20436; Hotfix for CQ-4215000

### Commerce {#commerce-4}

* Experience Fragments do not display properly in Internet Explorer 11. NPR-20161: Hotfix for CQ-4223319
* In commerce workflows, a blank image is automatically inserted when creating a variant based on a primary product with multiple images. NPR-20068: Hotfix for CQ-4222048
* Filtering by tags on collection pages in products console do not work. NPR-20292: Hotfix for CQ-4224023

### Communities {#communities-8}

* Inconsistent search results with searchresult component. NPR-20070: Hotfix for CQ-4220913
* Email notifications do not get triggered for any of the moderator-related activities on published components. NPR-20122
* Blank pagination with no results is displayed for anonymous community users. NPR-20136: Hotfix for CQ-4220738
* Configure alert trigger when a UGC is detected as spam or when a user posts on a pre-moderated site. NPR-20274: Hotfix for CQ-96850
* Resolved multiple issues in AEM Communities site pages, including incorrect redirects and page refresh issues. NPR-20344
* CommunityUserOperationExtension runs into a class cast exception. NPR-20532: Hotfix for CQ-4224385
* After creating a Communities site, users unable to open it from the sitemap because the context path does not get prepended to the URL. NPR-20730

### Integration {#integration-6}

* Migrating Analytics existing credentials to WSSE Authentication. NPR-19962: Hotfix for CQ-4218071
* Reactivating the segment after any modification fails and throws an error. NPR-20054: Hotfix for CQ-4218401  
* The Search&Promote cloud service configuration ignores the form retrieval method making it unusable on the author instance. NPR-20447: Hotfix for CQ-4206076  
* Ambiguous filter definition in content package causes paths to be overwritten when the Search&Promote feature is installed. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* Metadata properties for assets of type TXT displayed in different metadata editors each time their properties are displayed. NPR-20239

### Platform {#platform-3}

* Resolved an unclosed resource resolver exception. NPR-19749: Hotfix for Granite - 19143
* Request for custom cards to be displayed along with default health-checks in the operations dashboard. NPR-20145  
* Annotation layer of the page editor does not work properly in Internet Explorer 11. NPR-20222: Hotfix for CQ-4222818  
* Session leaks on setting User agent as admin in replication agent. NPR-20578  
* The requestAttributes is not unset for the other data-sly-resource statements. NPR-20639: Hotfix for 4226206
* Fixed issues with curl Head requests for OOTB assets in AEM. NPR-20781: Hotfix for CQ-4221520

### Projects {#projects-1}

* Accessing different projects from Projects console takes longer time to load. NPR-20314
* Installing AEM 6.3.0.1 removes the dam-update-service user's keystore. NPR-20018
* In some custom deployments, users trying to select assignee in addTask module take longer to populate the list in the userpicker. NPR-20283: Hotfix for CQ-4224193

### User Interface {#user-interface-3}

* Colorfield is set to "always required" despite attributes in dialog. NPR-19702
* Scroll Bar does not display for Multi-field component in full screen on Internet Explorer 11. NPR-20261: Hotfix for CQ-4219782  
* Previous queries do not get aborted in case consecutive queries are triggered leading to incorrect results. NPR-20398: Hotfix for GRANITE-19306

### Workflow {#workflow-1}

* Users are not notified about the workflow tasks they receive in their inbox. NPR-20213: Hotfix for CQ-4221639
* OOTB granite user picker does not load any users when clicked dropdown in Dialog participant step of the workflow model. NPR-20236

## Forms {#forms-10}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-10}

#### Adaptive Forms {#adaptive-forms-3}

* Support for aggregation expression for repeated panels is missing. NPR-20861
* Dropdown displays the last stored value even if the associated form data model service doesn’t return a value. NPR-20710
* Unable to edit the existing rules with Boolean constraints in Rule Editor. NPR-21128

#### Form Portal {#form-portal}

* HTML profile is displayed for an adaptive form even when its asset type is not XDP. NPR-20079

#### Backend Integration {#backend-integration-2}

* Unable to set value of switch component between true/false. NPR-21111

#### OSGI Workflow {#osgi-workflow}

* Manage workflow submission lists only ten applications. CQ-4230193

#### HTML5 Forms {#html-forms-3}

* The name of an XDP form object like subform is displayed as its tooltip when it is not defined in the accessibility configurations. NPR-20523

### Forms JEE installer {#forms-jee-installer-9}

#### Process Management {#process-management-2}

* The FormSetPrefillApp startpoint does not prefill formset fields in AEM Forms app. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Install the latest CTJPEG2K library for a critical security vulnerability. This impacts XMLFM (AEM and IfBA), RM, PDFG modules. NPR-20625: NPR-21337.

### Feature Packs Included {#feature-packs-included}

#### AEM Forms App {#aem-forms-app}

* Enabled OSGi workflow task support in AEM Forms App. CQ-4222638

### OSGI bundles and content packages included in 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

List of OSGi bundles included in AEM 6.3.1.2

[Get File](assets/do-not-localize/6_3_1_2-bundle-list.txt)

List of Content Packages included in AEM 6.3.1.2

[Get File](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM Cumulative Fix Pack 6.3.1.1 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 Service Pack 1 (6.3.1.0) in October 2017.

The key highlights of the AEM Cumulative Fix Pack are:

* Enabled publish to Brand Portal action for default metadata schema form.
* Behavior change in displaying titles on Image card for Image having dc: title property set to String [] (multifield).
* Replaced server-side rendering of time with foundation-time component.
* Enabled publish tags from AEM to Brand Portal from tagadmin/tagging console.
* Published JSON API to consume content fragments.
* The built-in repository (Apache Jackrabbit Oak) is updated to version 1.6.5.

### Assets {#assets-11}

* Mapping two fields with same property with different types of property field throws an internal error. NPR-19462: HF for CQ-4216828
* dc: title and dc: description does not change to a multi-field value in  crx /de. NPR-19570: HF for CQ-4209086
* Dynamic Viewer loads lowest quality video rendition for testing video playback experience in author mode. NPR-19004
* Dynamic rendition cannot be downloaded for assets that include spaces in their names. NPR-19433: Hotfix for CQ-4211738
* Unable to load complete list of pages/assets in Column view using Chrome. NPR-19566: Hotfix for CQ-4214248
* Publish to Brand Portal option is not available on selecting any schema or search facet or preset. NPR-19550
* On selecting an asset in column view and clicking edit, the page returns an error. NPR-20301: Hotfix for CQ-4224052
* Asset Expiration display is off when crossing positive and negative timezones. NPR-20329: Hotfix for CQ-4219333

### Campaign {#campaign-2}

* Campaign Slider components do not appear when the Default experience is chosen for a campaign. NPR-19213

### Integration {#integration-7}

* Custom at.js file does not publish when accessed with the anonymous user. NPR-19542: Hotfix for CQ-4219592
* Targeting Engine field in the config wizard is set to ContextHub (AEM) instead of Adobe Target. NPR-19320: HF for CQ-4218465
* Audience section gets corrupted while creating experience. NPR-19110
* Targeting dialog not displayed in targeting mode when a target module is edited and save more than once. NPR-19144: Hotfix for CQ-4216708
* Access properties for articles getting incorrectly set in Adobe Digital Publishing Solution on Classic UI. NPR-19367
* Incorrect behavior of auto-folding when personalizing offers through Campaign if users have access to multiple areas. NPR-19290: Hotfix for CQ-4218029

### Sites {#sites-11}

* Multi-composite field dropdown values do not get re-populated due to change code in Sidekick.js after upgrading the instance to AEM 6.1SP2-CFP3. NPR-19450: HF for CQ-4194771
* WCMMode.EDIT does not work for targeted components on authoring mode. NPR-19387
* Published JSON API to consume content fragments. NPR-19500
* Bold, italic, underline functionality does not work for rich text editor fields in the author dialog. NPR-19670: NPR-19718: Hotfix for CQ-4219088

### Mobile On-Demand {#mobile-on-demand-1}

* Rendering issues with AEM article console as using the full-size images makes it sluggish. NPR-19088

### Translation {#translation-5}

* Unable to generate preview for Translation projects. NPR-19289

### Security {#security}

* SSL connection error. Unable to make a secure connection to the server. NPR-19628

### Communities {#communities-9}

* Mail gets triggered on content posting with pre-moderated sites. NPR-20008
* Email notifications do not work for any of the moderator-related activities on published components. NPR-19767: HF for CQ-4218060

### Platform {#platform-4}

* Stability issues with AEM production server deployment. NPR-19707
* Custom taglib that reference tags implemented as a script are not found after upgrading to AEM 6.3. NPR-19087  
* HTL bug fixes for AEM 6.3.1. NPR-19161  
* Richtext field is not editable in the multi-field components. NPR-19604: Hotfix for Granite-16755  
* The Adobe Email Template service adds tags to custom user templates. NPR-19190
* Hotfix for Oak 1.6.5. NPR-19148

### Commerce {#commerce-5}

* Start Workflow button after selecting an XF variation editor has no effect. NPR-19642: Hotfix for CQ-4207796

### Projects {#projects-2}

* Project editors unable to copy/paste assets into the project asset folder. NPR-19619: Hotfix for CQ-4215321

### Web Content Management {#web-content-management}

* In Rollout screen, checkboxes corresponding to livecopy pages cannot be checked or unchecked. NPR-19518
* The bulk editing of page properties is not properly usable as currently all tabs and fields are available for bulk edition. NPR-19451
* OOTB properties and image alignment properties do not appear when editing an image in classic UI. NPR-19488: HF for CQ-4217914

### User interface {#user-interface-4}

* When using the Google Chrome browser, users are not able to load the complete list of pages/assets using column view in TouchUI. NPR-19566: Hotfix for CQ-4214248

### Brand Portal {#brand-portal-1}

* Unable to publish assets from AEM with comments and annotations. NPR-19590: Hotfix for CQ-4218386
* Enabling publish tags from AEM to Brand Portal from tagadmin/tagging console. NPR-20271: Hotfix for CQ-4223948
* Fix “enabled” field on Brand Portal cloudservice config UI. Hotfix for CQ-4211101
* Search form replication is failing. Hotfix for CQ-4220080

## Forms {#forms-11}

AEM Forms fixes are delivered through add-on packages and other patch installers provided with the release. For details, see AEM Forms Releases.

### Forms add-on package {#forms-add-on-package-11}

#### Adaptive forms {#adaptive-forms-4}

* Submit to JEE workflow doesn't return back output parameter from JEE side to AEM and throws "Ignoring because the value is not primitive" error. NPR-20265
* Adaptive Forms doesnot allow PDF as an attachment in Safari. NPR-19625
* RestoreGuideState overwrites customcontextproperty map. CQ-4222877
* When configuring Google reCaptcha using Cloud Service, in environments requiring configuration of org.apache.http.proxyconfigurator for external connections, POST calls doesn't seem to go through PROXY. NPR-20454
* Adaptive Forms based on XSD schemas submit faulty XML values for numeric fields on installations with locales that have a decimal separator other than "." resulting in errors. NPR-20444  
* Proxy settings set for 'Apache HTTP Components Proxy Configuration' are not honored while making HTTP request to third-party server. Connection timeout issues using HTTP GET or POST calls. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Forms Data Integration {#forms-data-integration}

* UTF-8 characters as output of SOAP service are not correctly copied into Adaptive Forms fields for non-English locales. NPR-20238: NPR-20103

#### Correspondence Management {#correspondence-management-1}

* Copy Paste content from the word file looses its content color and font in Text Editor. NPR-19521

#### Assembler Services {#assembler-services}

* Discrepancy between results of Acrobat and AEM during a compliance verification of a document to PDFA-1b format. NPR-19280

#### Workflow {#workflow-2}

* Workflow Sign step to allow http calls to connect through the proxy. NPR-20529

#### HTML5 Forms {#html-forms-4}

* Added support for preSubmit event. NPR-20604

### Forms JEE installer {#forms-jee-installer-10}

#### Process Management {#process-management-3}

* Workflow attachment, notes, and details tabs do not function in  workspace  when the form is maximized/minimized and saved as a draft or forwarded. NPR-20243
* Multiline text field (TextArea) does not retain new line character or break in text after submitting data in HTML workspace. NPR-20085

#### Process Reporting {#process-reporting}

* Process reporting does not fetch data properly because of Null Pointer Exception. NPR-19759

>[!NOTE]
>
>Install LiveCycle embed package listed in [AEM Forms Releases](aem-forms-releases.md) article to fix the issue.

#### Standard Services {#standard-services}

* docConvertor is not supporting flattening transparencies in PDF and fails to produce a PDF/A. NPR-16228: Hotfix for CQ-4214488

#### Core {#core-2}

* When AEM Forms server running in a cluster configuration on JBoss application is stopped, the application server is disconnected from the database. It can lead to data corruption issues. NPR-19724

### Feature Packs Included {#feature-packs-included-1}

* Drop down metadata schema field cannot be made mandatory as mandatory field validation is missing for assets. NPR-17882: FP for CQ-4208373

### OSGI bundles and content packages included in 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}

List of OSGi bundles included in AEM CFP 6.3.1.1

[Get File](assets/do-not-localize/bundle-list.txt)

List of Content Packages included in AEM CFP 6.3.1.1

[Get File](assets/do-not-localize/content-package-list.txt)

AEM Cumulative Fix Pack 6.3.0.2 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 in April 2017.

The key highlights of the AEM Cumulative Fix Pack are:

* Auditability of user access control
* Includes version 1.6.2 of the built-in repository (Apache Jackrabbit Oak)
* Resolved unclosed resource resolver issues
* Simplified configuration for smart content services
* Resolved content fragment validation issues
* Improved editability of metadata schemas on hybrid devices
* Resolved component-level synchronization issues in live copies
* Improved usability of content-heavy pages in column view
* Improved compliance with page naming convention for pages with long titles
* Improved campaign personalization experience on Touch UI
* Fixes for various project overlay issues

### Platform {#platform-5}

* Hotfix for Oak 1.6.2. NPR-16993  
* While opening the omnisearch using a filter, the path is no longer set. NPR-17398: Hotfix for CQ-4204870
* Requirement for auditability of user permission changes in AEM. NPR-17061
* Lingering connections to DM Cloud Services causing "Too many open files" exceptions. CQ-4211407

### Assets {#assets-12}

* Usability issues with configuring smart content services using different options. NPR-18200: Hotfix for CQ-4201557
* Resource leakage in binary streams to S3 datastore. NPR-18041: Hotfix for CQ-4209506
* An error occurs when an ASCII/UTF-8 encoded text file is uploaded to AEM Assets and thumbnail generation fails. NPR-18006: CFP for CQ-4209345
* Default metadata schema causes content fragment validation failure. NPR-17769: Hotfix for CQ-4211111
* Unclosed resource resolver in com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP for CQ-4209018
* Request to create multiple replication agents for publishing assets to Brand Portal. NPR-17189
* Review task for assets under Japanese language folder doesn't work. CQ-4204782
* Null pointer exception occurs when an asset is moved from its properties page. CQ-4204251
* AEM fails to track subsequent references to an asset in the properties page if it is linked to an InDesign document multiple times. CQ-4204186
* Issues with adding new tabs in the metadata schema form when it is edited in Chrome on hybrid devices. CQ-4201810
* When duplicate assets are uploaded, the (delete/keep) option is applied to all assets even when it is not selected in duplicates detected dialog. CQ-4201673
* A null pointer exception is raised when an asset folder with more than 150 incoming references is moved. CQ-4200981
* For a downloaded asset folder, if a conflict occurs when extracting the contents of the ZIP file the default option appears as Create version instead of Keep both. CQ-97800
* Users with read-only permissions to app cannot preview content from AEM Mobile content management. NPR-17486: CFP for CQ-4209690
* The Create Catalog button does not work in column view in the Catalog console. CQ-4209952

### Sites {#sites-12}

* Issues with embedding image/video components via data-sly-resource attribute. NPR-18182: CFP for CQ-4212100
* Modified localized components not restored to their original form when inheritance is reapplied in a LiveCopy. NPR-18172: Hotfix for CQ-4211379
* Issues with navigating a content-heavy page in column view in Touch UI. NPR-17799: Hotfix for CQ-4199611
* Unclosed resource resolver in `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP for CQ-4211152
* Page name not getting generated as per convention for long page titles. NPR-17633: Hotfix for CQ-4209056
* Issues with page creation on Touch UI in AEM 6.3 deployed on Jboss EAP 6.4. NPR-17589: Hotfix of CQ-4210137
* Workflow status provider causes the instance to lock up when nested groups are present. NPR-17556: CFP request for CQ-4202056
* Unclosed resource resolver in the following objects:

  * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP for CQ-4208673
  * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP for CQ-4208668
  * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP for CQ-4208669
  * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP for GRANITE-17404

### Integrations {#integrations-1}

* Resolved AEM Search component errors that can occur when AEM Day HTTP Client 3.1 OSGI is configured with a Proxy that requires Digest Authentication. NPR 18128: Hotfix for NPR-18029  
* Issues with personalizing campaigns and associated experiences via Classic UI. NPR-18127: Hotfix for CQ-4211559
* When setting a brand/zone to a root page of a site, inheritance once cancelled cannot be restored for Areas in subpages. NPR-17753: Hotfix for CQ-4210139

### Workflow {#workflow-3}

* In a non-transient workflow, the process history and metadata changes made before an external process step are not persisted. NPR-17848: Hotfix for GRANITE-17757
* Values from workflow dialog fields are not persisted in the work item node. NPR-17734: Hotfix for CQ-4210369
* Unparsable date error occurs when editing task from inbox. CQ-4208749

### Projects {#projects-3}

* Fixes for various project overlay issues. NPR-17733
* Restructuring of the pods in the projects module makes it less configurable. CQ-4209859
* Path of assets path changes to the respective localized sites when pages are added to the translation job. CQ-4206007

### Security {#security-1}

* Issues with uploading avatar images for LDAP users. NPR-16561
* Request to use an upgraded version of org.apache.sling.servlets.post servlet (2.3.22) in Apache Sling API to pre-empt an XSS vulnerability. NPR-18963

## Forms {#forms-12}

AEM Forms fixes are delivered through Forms add-on package and other patch installers provided with the release. For details, see [AEM Forms Releases](aem-forms-releases.md).

The key highlights for AEM Forms are:

* Fixes in correspondence management text modules, letter previews, and programmatically launching create correspondence management UI.
* Fixes for PDF/A-1b validation, conversion of large image files to PDF, and Japanese language PDF documents in PDF Generator.  
* Usability fixes for correspondence management, document security, and forms workflow.  
* Added support to capture audit events for the scribble signature field.

### Forms add-on package {#forms-add-on-package-12}

**Correspondence Management**

* On editing a correspondence management fragment, the text editor displays inline conditions along with the processed text. CQ-4211930
* On creating a correspondence management letter, description of the letter is not saved. NPR-18089
* Additional margin above and below a bulleted list is visible in text editor but not in HTML and PDF rendition. NPR-18126
* When HTML submit used the POST method, the create correspondence UI fails to launch. NPR-18202
* When a text module is saved and an expression in the text module does not contain opening or closing expression tags, no error message is displayed. The text module displays an error message and fails to render in the letter. NPR-18535
* When new content is added or the Enter key is pressed, a div tag is added to the text module. NPR-18240

**Assembler**

* On validating a PDF document for PDF/A-1b compliance, AEM Forms returns a validation error: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. The PDF document does not return the error when validated with Adobe Preflight and third-party software. NPR-18011
* On validating PDF documents for PDF/A-1b compliance, AEM Forms returns a validation error: Form field has multiple appearances. The PDF documents are PDF/A-1b compliant. NPR-18013

**Watch Folder**

* On selecting to process files using a workflow, while creating a watch folder, the workflow model selection drop-down appears truncated. NPR-17566

**HTML5 Forms**

* AEM Forms does not capture audit events for the scribble signature field. NPR-15286

**Forms Manger**

* AEM Forms UI lists all the assets in the oldest first order. Users are not able to reorder the assets in newest first order. NPR-18450

**Java API Reference**

Added JavaDocs for the com.adobe.livecycle.content class. NPR-18468

### Forms JEE installer {#forms-jee-installer-11}

**PDF Generator**

* PDF Generator service fails to convert images larger than 100 MB to PDF documents. Ref# CQ-4208628
* On using PDF Generator service with a Japanese language OCR, an inverted PDF is generated. NPR-17602

**Process Management**

* The TaskContext variable is not populated for AEM Forms processes. NPR-18199

**Document Security**

* Microsoft Excel and Microsoft PowerPoint take much longer time to open the documents protected with AEM Document Security Extension for Microsoft Office. CQ-4212358
* When a new policy is created and a policy with the same name as existing, an internal server error occurs. NPR-18247

## Feature Packs included {#feature-packs-included-2}

* Requirement for auditability of user permission changes in AEM. NPR-17061

AEM Cumulative Fix Pack 6.3.0.1 is an important update that includes several internal and customer fixes since the general availability of AEM 6.3 in April 2017 .The  key highlights of the AEM Cumulative Fix Pack are:

* Improvements in the following area:

  * Content Fragments, Sites, and Rich Text Editor, Rule Editor, and Template Editor components
  * Social Review and Facebook Social login
  * Configuring and starting Translation jobs
  * Response time for accessing notifications in Social Communities
  * Display of review tasks in the DAM repository

* Provides validation option in Package Manager for detecting conflicts between overlay and CFP

## Download Instructions for CFP via Software Distribution {#download-instructions-for-cfp-via-package-share}

You can download the CFP package directly from [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) or perform the following steps:

1. Open [Software Distribution](https://experience.adobe.com/downloads). You require an Adobe ID to log in to the Software Distribution.
1. Tap **[!UICONTROL Adobe Experience Manager]** available in the header menu.
1. Tap the package name, select **[!UICONTROL Accept EULA Terms]**, and tap **[!UICONTROL Download]**.

## Installation instructions {#installation-instructions}

This section walks you through the requirements and steps to install the CFP.

### Before you install {#before-you-install}

>[!NOTE]
>
>Optional Feature Packs provided by Adobe have dependencies on the release version and Cumulative Fix Pack. If you have any Feature Pack installed, please contact the [AEM Customer Care team](https://helpx.adobe.com/marketing-cloud/contact-support.html) to validate the compatibility with this Cumulative Fix Pack for AEM 6.3.

>[!NOTE]
>
>It is recommended that you run validation on every new installation package before attempting to install the package. Pre-validation analyzes and reports any errors found before installation and warns the users about such errors proactively.
>
>You can access documentation for Validate option at [https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 is a prerequisite for the CFP. Please visit [Upgrade Documentation](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html) for detailed instructions about upgrading an AEM installation to AEM 6.3.
* For a cluster deployment using RDBMK or MongoDB, the CFP package can be installed on any of the Author instances that  uses  Package Manager.
* Before installing the cumulative fix pack, ensure to take a snapshot or make a backup of your AEM instance.
* Uninstalling the CFP is not supported.

### Adding new loggers {#adding-new-loggers}

To configure debug level logging and retrieve an activity log during installation of SPs/CFPs, you can follow the steps below:

* You may add a new logger at the default location [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) with the below properties:

  * Log Level: Debug
  * Additive: false
  * Log File: logs/activity.log
  * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

The activity.log will be created in   crx -quickstart /logs folder.

### Install the Cumulative Fix Pack via Software Distribution {#install-the-cumulative-fix-pack-via-package-share}

Perform the following steps to install the Cumulative Fix Pack on an existing AEM 6.3 instance:

1. Click the [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) link to download the package.

1. Open [Package Manager](http://localhost:4502/crx/packmgr/index.jsp) and click **[!UICONTROL Upload Package]** to upload the package.

1. Select the package name and click **[!UICONTROL Install]**.

### Automatic installation {#automatic-installation}

The CFP can be automatically installed into a running instance in the following ways:

* Place the package into `../crx-quickstart/install` while the server is running. The package gets installed automatically.
* Use the [HTTP API from Package Manager](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/package-manager.html) - make sure that you use `cmd=install&recursive=true` - so the nested package is installed.

### Validate installation {#validate-installation}

1. The Product Information page ( `/system/console/  productinfo`) should now show the updated version string "Adobe Experience Manager, Version 6.3.3.8" under Installed Products.
1. All OSGI bundles are either ACTIVE or FRAGMENT in the OSGI Console (Use Web Console: `/system/console/bundles`).

>[!NOTE]
>
>On successful installation of the package, an informational message appears on the error logs indicating that the content package has installed successfully, such as "Content Package **AEM-6.3.3-Cumulative-Fix-Pack-7** installed successfully."

>[!NOTE]
>
>Since AEM 6.3.3.1, the log level in Jackrabbit FileVault has changed from INFO to DEBUG for most of the messages. To obtain installation logs for a content package installed on AEM 6.3.3.1 or higher, enable DEBUG log level for org.apache.jackrabbit.vault.packaging.impl.

### Install AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Skip this section if you are not using AEM Forms.

#### Install AEM Forms add-on {#install-forms}

1. Ensure that you have installed the AEM 6.3.3.x CFP package. 
1. Download the corresponding Forms add-on package listed at [AEM Forms releases](aem-forms-releases.md) for your operating system.
1. Install the Forms add-on package as described in [Installing AEM forms add-on packages](https://helpx.adobe.com/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### Install AEM Forms JEE bundles package {#install-aem-forms-jee-bundles-package}

Fixes in AEM Forms JEE are delivered through a separate installer. For information about installing a CFP on AEM Forms on JEE, see [Installing CFP on AEM Forms JEE](install-cfp-aem-forms-jee.md).

#### Forms Designer installer {#designer-installer}

1. To install the update, run the Designer 6.2.0_&lt;Language&gt;_Cumulative_QF.msp file.
1. On the welcome screen, click **update**. The installation starts.
1. After the installation completes, click **finish**.

## Configuration settings for AEM Forms JEE (JBoss EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>If you are installing 6.3.3.0 or later releases, perform the below procedure to configure settings for JBoss application server. If you are installing 6.3.3.0 on AEM Forms server running on Oracle WebLogic or IBM WebSpehere application servers, no additional configuration is required. For further details, see [AEM 6.3.3.0 Release Notes](https://helpx.adobe.com/experience-manager/6-3/release-notes/sp3-release-notes.html).

## Configuration updates for Search&Promote Integration {#configuration-updates-for-search-promote-integration}

With AEM Cumulative Fix Pack 6.3.0.2 and later releases, the OSGi configuration used for Search&Promote Integration is **Apache HTTP Components Proxy Configuration**. The Proxy configuration from Day Commons HTTP Client 3.1 is no longer used.

## Known issues {#known-issues}

* The following errors and warning may occur during installation of AEM CFP 6.3.3.x and can be safely ignored:

  * &#42;WARN&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar threw runtime exception.
  * &#42;ERROR&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Timeout waiting for reg change to complete unregistered. CQ-4209974.  
  * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver service missing, cannot service requests , sending status 503  
  * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: cannot check resource [/bin/receive], page manager unavailable
  * org.apache.sling.servlets.resolver.internal.SlingServletResolver: Calling the error handler resulted in an error
  * org.apache.sling.servlets.resolver.internal.SlingServletResolver Original error null
  * org.apache.sling.engine.impl.DefaultErrorHandler Error handler failed:java.io.IOException
  * &#42;ERROR&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Component: com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* With 6.3.1.2 onwards, Publish to Brand Portal button for smart collections has been removed.

**User Interface**

>[!NOTE]
>
>In case you are impacted with any of these two issues, contact [AEM Customer Care](https://helpx.adobe.com/marketing-cloud/contact-support.html).

* High CPU utilization is observed due to lot of requests in Admin Search functionality. NPR-24229
* PathField is not selected in the pathBrowser when re-opening the component. NPR-24177

## Configuration settings required for NPR-27692 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>This configuration setting applies to CFP 6.3.3.2 and later. It directs you to update the boot delegation properties in `sling` .properties file.

To update changes in adobe- livecycle - cq -author.ear/ cq .war manually, follow the steps mentioned below:

* Stop the AEM server.
* Go to adobe-livecycle-cq-author.ear/cq.war
* Open adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml for editing:

  * update the **sling.bootdelegation.ibm** param-name value with:

    * com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat

  * After the above change, init-param should look like:

    * &lt;init-param&gt;  
      &lt;param-name&gt;sling.bootdelegation.ibm&lt;/param-name&gt; &lt;param-value&gt;com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value&gt;  
      &lt;/init-param&gt;

* Uninstall the previous enterprise archive (EAR) file from the websphere application server and install the updated EAR file following the steps at Section 10.2 of [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Save the file and restart the server. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Configuration settings required for NPR-23208 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>This configuration setting applies to 6.3.2.2 and later. It directs you to update Access Control Lists (ACL) policies manually through CRX-DE as ACLs do not get updated through the CFP installation due to "merge_preserve"  acHandling .

**Documentation for adding ACL policies manually**

To update ACL policies, add the below Access controls through CRX-DE:

`1)` At "/content" path  
`a)` Principal : reference-adjustment-service  
Type : Allow  
Privileges : jcr:read , jcr:modifyProperties  
Restrictions : rep:glob="/&#42;/jcr:content"  
`b)` Principal : reference-adjustment-service  
Type : Allow  
Privileges : jcr:read , jcr:modifyProperties  
Restrictions : rep:glob="/&#42;/jcr:content/&#42;"

`2)` At "/content/usergenerated" path  
`a)` Principal : reference-adjustment-service  
Type : Allow  
Privileges : jcr:write

`3)` At "/etc" path  
`a)` Principal : reference-adjustment-service  
Type : Allow  
Privileges : jcr:read , jcr:modifyProperties  
Restrictions : rep:glob="/&#42;/jcr:content"  
`b)` Principal : reference-adjustment-service  
Type : Allow  
Privileges : jcr:read , jcr:modifyProperties  
Restrictions : rep:glob="/&#42;/jcr:content/&#42;"

## Configuration settings required for NPR-19450 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>This configuration setting applies to CFP 6.3.1.1 and later.

**Configure the property CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

The property controls the maximum depth of the node subtree under the page ` /  jcr   :content` node, until which the nodes present in the repository shall be used for getting the page properties. Any node present below the specified depth in this property is ignored.

The default value is 1. The value can be  overriden  by overlaying the file constants.js (`/libs/cq/ui/widgets/source/constants.js`) uncommenting the CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL property and assigning it the required value ( the max depth under the page's / jcr  :content  till which the page properties' data is stored).

**If the user needs to create multiple pages variants such that the number of nodes under the page's /  jcr   :content  node becomes greater than 1000, use the following steps to do configuration changes:**

* Configure the property JSON Max results of Apache Sling
* Get Servlet using `/system/console/  configMgr`
* Set its value to a number &gt;1000 (which is the current default) such that this number is greater than the total number of nodes in the / jcr  :content  subtree until the configured depth above.

This enables the sling GET servlet to be able to return all the required nodes.

## Uber Jar {#uber-jar}

The Uber Jar for 6.3.3.8 is available at [Adobe Public Maven repository](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

To use Uber Jar in a Maven project, refer to the article, [How to use Uber jar](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) and include the following dependency in your project POM:

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## Removed/Deprecated Features {#deprecated}

This section lists features and capabilities that have been removed or deprecated from AEM 6.3.

|Area| Feature | Replacement | Version |
|----|-----|-----|-----|
|Assets and Adobe Creative Cloud integration | [AEM to Creative Cloud folder sharing](https://helpx.adobe.com/experience-manager/6-3/sites/administering/using/creative-cloud.html) was introduced in AEM 6.2 as a way to give creative users access to assets from AEM. A new capability released in Creative Cloud application, Adobe Asset Link, provides a much better user experience and more powerful access to assets from AEM directly from inside Photoshop, InDesign, and Illustrator.<br /> Adobe will not make further enhancements to the folder sharing capability. While the feature is included in AEM, customers are strongly advised to use the replacement. | Adobe Asset Link or Desktop App. For more info, see [AEM Creative Cloud integration](https://helpx.adobe.com/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html) article.| AEM 6.3.3.x |

## OSGi bundles and Content Packages included {#osgi-bundles-and-content-packages-included-1}

The following text documents list the OSGi bundles and Content Packages included in the CFP.

* [List of OSGi bundles included in AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [List of Content Packages included in AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM releases and updates](https://helpx.adobe.com/experience-manager/aem-releases-updates.html)
>* [AEM 6.3 hotfixes page](https://helpx.adobe.com/experience-manager/kb/aem63-available-hotfixes.html)
>* [AEM 6.3 release notes](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM product page](http://www.adobe.com/solutions/web-experience-management.html)
>* [AEM 6.3 documentation](https://docs.adobe.com/content/docs/en/aem/6-3.html)
>* Subscribe to [Adobe priority product updates](https://www.adobe.com/subscription/priority-product-update.html)
