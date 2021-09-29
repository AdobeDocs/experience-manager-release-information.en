---
title: Older versions of AEM, CQ, and CRX
description: Documentation packages for older versions of Adobe Experience Manager, CQ and CRX.
exl-id: c210eadb-58ec-4d40-ba72-5e4b11564510
---
# Older versions of [!DNL Adobe Experience Manager], CQ, and CRX {#older-versions-aem-cq-crx}

## Older versions of [!DNL Experience Manager] documentation {#older-version-aem-documentation}

The versions of [!DNL Adobe Experience Manager], CQ and CRX listed on this page are End of Life and no longer officially sold by Adobe. Our last versions of official documentation for these older versions are available for your self-help needs. We recommend you upgrade to the latest version - [[!DNL Adobe Experience Manager] as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html).

>[!NOTE]
>
>To know when an [!DNL Experience Manager] version will reach end of core support, see [products and technical support periods](https://helpx.adobe.com/support/programs/eol-matrix.html) and search `AEM`.

### Before you install {#before-installation}

Before you download the package, determine who will consume the content. This decision will determine how it is deployed:

* Developers can install locally for quick reference.
* For broader organizational documentation needs, it is recommended the package is deployed on an internally accessible, non-production AEM Author instance.

>[!NOTE]
>
>Users must be logged into the [!DNL Experience Manager] instance to access this content on [!DNL Experience Manager] Author. This content is not accessible by default on AEM Publish (as it exists under /libs).

## Software Distribution Locations {#software-distribution-locations}

You will require a valid Adobe ID:

* If you don't have an Adobe ID, you can create one at www.adobe.com
If you need assistance creating or managing your Adobe ID, [please refer to this guide](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] Version |             Software Distribution Link             |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.3     | [Download AEM-DOCS-6.3 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-3.zip)  |
| [!DNL Experience Manager] 6.2     | [Download AEM-DOCS-6.2 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-2.zip)  |
| [!DNL Experience Manager] 6.1     | [Download AEM-DOCS-6.1 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-6-1.zip)  |
| [!DNL Experience Manager] 6.0     | [Download AEM-DOCS-6.0 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip)  |
| [!DNL Experience Manager] 5.6.1   | [Download AEM-DOCS-5.6.1 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip)|
| [!DNL Experience Manager] 5.6     | [Download AEM-DOCS-5.6 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip)  |
| CQ 5.5      | [Download CQ-DOCS-5.5 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip)   |
| CQ 5.4      | [Download CQ-DOCS-5.4 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip)   |
| CQ 5.3      | [Download CQ-DOCS-5.3 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip)   |
| CRX 2.3     | [Download CRX-DOCS-2.3 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip)  |
| CRX 2.2     | [Download CRX-DOCS-2.2 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip)  |
| CRX 2.1     | [Download CRX-DOCS-2.1 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip)  |
| CRX 2.0     | [Download CRX-DOCS-2.0 from Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip)  |

## How to install a documentation package {#how-to-install-documentation-package}

In order to Install a legacy documentation package you must have [!DNL Experience Manager] installed and running on your local drive or network drive.

### Download the documentation package {#download-documentation-package}

1. From the table above, select the link for the [!DNL Experience Manager] documentation version to download. For example, AEM 5.6.1.

1. Login using your Adobe ID. If you don't have an ID, create one.

1. Select the the **[!UICONTROL Download]** button.

1. Here is an example of what you will see:

![Example Software Distribution](assets/screen_shot_2020-07-10at161922.jpg)

### Install the package on your local instance {#install-package-local-instance}

>[!NOTE]
>
>For AEM 6.2, you might need to start your local instance with an increased maximum heap size, by using this command for example: ` java -jar -XX:MaxPermSize=2048m aem-author.jar`

1. Open the [!DNL Experience Manager] user interface. In a web browser enter: `http://localhost:4502/`. Login as an Administrator.

1. Select **[!UICONTROL Tools]** > **[!UICONTROL Deployment]** > **[!UICONTROL Packages]**.

1. From the Package Manager UI, select **[!UICONTROL Upload Package]**.

1. Browse to the location where you downloaded the AEM package.

1. Select the package and click **[!UICONTROL OK]**.

1. Once the package has been uploaded you will need to install it.

1. In Package Manager UI, locate the package and select **[!UICONTROL Install]**.

1. On the confirmation dialog select **[!UICONTROL Install]** again. Note: the installation will take a few minutes.

1. In a web browser, launch the documentation page. Using the AEM 5.6.1 example, the URL would be: http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html.

## Get help from the [!DNL Experience Manager] community {#get-help-from-aem-community}

If you have questions about using Experience Manager, we recommend that you [reach out to our experienced community experts in the [!DNL Experience Manager] forums](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).
