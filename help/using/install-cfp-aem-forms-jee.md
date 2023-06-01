---
title: Installing Cumulative Fix Packs on AEM Forms JEE
description: Summary of steps to install and configure Cumulative Fix Pack (CFP) on AEM Forms JEE
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
---
# Installing Cumulative Fix Packs on AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}

## Install CFP on AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

To install the cumulative fix pack on AEM 6.3 [!DNL Forms JEE], perform the following sequence of steps.

1. To obtain the AEM 6.3 [!DNL Forms JEE] installer for the CFP, contact [Adobe Support](https://experienceleague.adobe.com/?support-solution=General&support-tab=home#support).
1. Run the CFP installer and configure AEM [!DNL Forms JEE] as described in [Install and configure AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Install the latest AEM CFP 6.3.3.x
1. Install the [!DNL Forms] Add-on package for AEM CFP [6.3.3.x](aem-forms-releases.md)

### Install AEM [!DNL Forms JEE] bundles package {#install-aem-forms-jee-bundles-package}

AEM [!DNL  Forms JEE] package (aemfd-jee-bundles-package-6.3CFP1; version 1.0.2) provides [!DNL Forms] User on AEM [!DNL Forms JEE] the same rights and capabilities as found on AEM [!DNL Forms OSGi]. Check your installed packages in Package Manager and install the package if it is not already installed.  

### Additional instructions for CQ-4208044 {#additional-instructions-for-cq}

If you are using AEM 6.3 [!DNL Forms JEE] server with Oracle database, configure the following settings post deployment of the CFP1, that is, after the Configuration Manager is run. This setting is required to sync users, groups, and group members when the enterprise domain sync is run. 

1. Log in to the **Admin** UI.
1. Navigate to **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**
1. Export the config.xml file.
1. Modify the entry for " `groupMemberDBQueryBatchSize`" under your domain configurations in *config.xml*. Sample entry:

   &lt;entry key="groupMemberDBQueryBatchSize" value="999"/&gt;

1. Import the modified file again and then, re-run the sync.

## Install CFP on AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}

To install cumulative fix pack on AEM 6.2 [!DNL Forms JEE], perform the following sequence of steps.

1. To obtain the AEM 6.2 [!DNL Forms JEE] installer for the CFP, contact [Adobe Support](https://experienceleague.adobe.com/?support-solution=General&support-tab=home#support).
1. Run the CFP installer and configure AEM [!DNL Forms JEE] as described in [Install and configure AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Install AEM Hotfix 12785 version 7.0.
1. Install AEM 6.2 Service Pack 1.
1. Install the latest release-notes-aem-6-2-cumulative-fix-pack.md.
1. Install the [!DNL Forms] Add-on package for AEM 6.2 Service Pack 1 CFP.

### Install AEM [!DNL Forms JEE] bundles package {#install-aem-forms-jee-bundles-package-1}

AEM Forms JEE package (aemfd-jee-bundles-package-6.2CFP5; version 1.0.2) provides [!DNL Forms] User on AEM [!DNL Forms JEE] the same rights and capabilities as found on AEM [!DNL Forms OSGi]. Check your installed packages in Package Manager and install the package if it is not already installed.

### Configuring timeout for operations at component level (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Post AEM 6.2 CFP4, you can use the following instructions to configure the timeout for DSC operations in case you face problems due to timeout during the upgrade process.

DSC deployment takes a variable time due to which it might fail. To change the timeout of DSC operations such as Install, Load, Start, and Stop, you must set the `adobe.component.registry.timeout` using the JVM argument with the -D option.

Specify the value for the key in seconds. For example: `-Dadobe.component.registry.timeout=300`

You can also change the timeouts at the component level using the following three properties:

1. `adobe.all-component.timeout`: overwrites the timeouts of all the Services of the Product.
1. `adobe.<serviceName>.timeout`: overwrites the timeout only for the service (&lt;serviceName&gt;) mentioned in the key. If the value at service level is set, then using this command only overwrites the timeout value for the specified service if it is set at Application level.
1. `adobe.<serviceName>.<operationName>.timeout`: It only overwrites the timeout for the specific service's operation(&lt;serviceName&gt;.&lt;operationName&gt;) mentioned in the key. If the value is set at Operation level, then using this command only overwrites the timeout value for the specified service if it is set at Application level or Service level.

**Examples:**

Use the following commands to set the timeout at component level:

1. To set the timeout of all service operations to 600 sec:

   set " `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`"

1. To set the `DesigntimeService` operation values timeout to 500 sec, use:

   set " `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`"

1. To set the `DesigntimeService's previewLCA` operation values timeout to 700 sec, use:

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`"

1. To set the `DSC operations`, such as load and install, to 600 sec, use:

   set " `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`"

## Install and configure AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Take a backup of the /deploy folder. It is required if you decide to uninstall the quick fix.
1. Stop your application server.
1. Extract the patch installer archive file to your hard drive.
1. In the directory named according to the operating system that you are using:

   **Windows**

   Navigate to the appropriate directory on the installation media or folder on your hard disk where you copied the installer:

    * (Windows 32-bit): Disk1\InstData\Windows\VM
    * (Windows 64-bit): Disk1\InstData\Windows_64bit\VM

   Then, double-click the file named:

    * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**) 
    * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
    * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux&reg;, Solaris&trade;, AIX&reg;**

   Navigate to the appropriate directory:

    * (Linux&reg;): Disk1/InstData/Linux/ NoVM 
    * (Solaris&trade;): Disk1/InstData/Solaris/ NoVM 
    * (AIX&reg;): Disk1/InstData/AIX/VM

   From a command prompt, type:

    * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
    * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
    * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   The Install wizard is launched to guide you through the installation.

1. On the Introduction panel, click **[!UICONTROL Next]**.
1. On the Choose Install Folder screen, verify that the default location displayed is correct for your existing installation, or click **[!UICONTROL Browse]** to select the alternate folder where AEM [!DNL Forms] is installed, and click **[!UICONTROL Next]**.
1. Read the Quick Fix Patch Summary information and click **[!UICONTROL Next]**.
1. Read the Pre-Installation Summary information and click **[!UICONTROL Install]**.
1. When the installation is complete, click **[!UICONTROL Next]** to apply the quick fix updates to your installed files.
1. The Start Configuration Manager checkbox is selected by default. Click **[!UICONTROL Done]** to run the Configuration Manager.

   To run Configuration Manager later, deselect the **[!UICONTROL Start Configuration Manager]** option before you click **[!UICONTROL Done]**. You can start Configuration Manager later using the appropriate script in the *`[AEM_forms_root]`/configurationManager/bin* directory.

1. Depending on your application server, choose one of the following documents and follow the instructions in the *Configuring and Deploying AEM [!DNL Forms]* section.

   For AEM [!DNL Forms] 6.3, refer to:

    * Installing and Deploying AEM [!DNL Forms] for JBoss&reg;
    * Installing and Deploying AEM [!DNL Forms] for WebSphere&reg;
    * Installing and Deploying AEM [!DNL Forms] for WebLogic

1. Restart AEM [!DNL Forms] JEE server.
