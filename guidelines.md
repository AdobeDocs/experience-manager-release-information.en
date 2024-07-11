# Guidelines for Contributing to Adobe Experience Manager Documentation

## Documentation Philosophy

Adobe Experience Manager users are working in highly competitive environments, striving to create digital experiences that set them apart from their competitors. Therefore, when Adobe introduces advanced new tools in AEM, they provide accurate and clear documentation. This approach lets customers immediately use their AEM investment and maximize ROI.

The goal of the AEM documentation is to put documentation into the hands of AEM users as soon as possible. Therefore, accurate, usable documentation is created and continually updated and improved.

## Documentation Contributions

In the interest of continually improving AEM documentation, the entire community of AEM users is welcome to contribute to the documentation. Be it through pull requests or issues, improvements to the documentation can be corrections, clarifications, expansions, and more examples.

## Documentation Standards

Adobe welcomes contributions to the documentation. Any contribution to the AEM documentation, whether a pull request or an issue, must conform to Adobe's contribution and documentation standards.

Contributions that do not meet these standards may be rejected.

### Adobe writes about standard use cases.

AEM documentation covers standard use cases. Use cases beyond the scope of standard installation and usage of the product are not part of AEM documentation.

### Adobe does not generally document bugs or their workarounds.

AEM documentation covers standard use cases. For this reason, bugs, effects caused by bugs, and workarounds for bugs are not documented.

Exceptions to this rule apply to the release notes where known issues can be listed with possible solutions that AEM Product Management approves.

### Documentation contributions are not for answering technical questions.

Any ideas you may have to improve AEM documentation are welcome as contributions. However, comments, issues, and pull requests are intended for *contributions* only. They are not intended to answer your questions about how to use AEM, implement your AEM project, or solve technical problems.

Report any questions about the usage of AEM or technical errors using the [Experience Cloud Enterprise Support portal](https://experienceleague.adobe.com/?support-solution=General#support). Or, use the [Experience Manager community](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community).

***AEM documentation contributions are not a replacement for Adobe Customer Care*** and any such contributions seeking answers to support-related questions are rejected.

### Contributions must clearly reference affected documentation pages.

If you create an issue to suggest improvements to the documentation, include links to the pages affected. If you create an issue using the **Edit this page** link on a documentation page, the issue is created with a link to the page automatically.

This process does not apply to pull requests because pull requests, by their nature, reference the affected page or pages.

## Documentation Guidelines

Any contributions to the documentation must follow certain style guidelines.

Following these guidelines makes the review of your contribution easier and therefore integration into the documentation is faster.

### Language and Style

#### Language

* AEM documentation is authored and maintained in US English.
* Keep sentences as simple as possible.
* Keep the language clear and concise.

Remember, readers of AEM documentation are worldwide and cannot be expected to be native or fluent English speakers. Avoid colloquialisms and keep the language as clear and simple as possible.

#### Follow the Microsoft&reg; Manual of Style

[The Microsoft&reg; Manual of Style](https://learn.microsoft.com/en-us/style-guide/welcome/) is a freely available documentation style guide that focuses on software documentation and AEM documentation follows this guide wherever possible.

### Formatting

|Item|Style|
|---|---|
|UI Element or option|**bold**|
|Filename, path, user-input, parameter-values|`monospaced`|
|Code, command line|```Code Block```|

### Screenshots

Screenshots are to be used judiciously and only when a textual description is insufficient.

Markers or other annotations in screenshots (like red frames, arrows or text) should not be used. This way the screenshots are easier to reuse or replicate in localized versions of the documentation.

### Version-Specific References

Ideally, avoid any direct references to a specific version throughout the documentation content whenever possible. This approach makes the documentation more flexible and extensible for future versions.

### Use of Day, AEM, CQ, CRX

When mentioning the product for the first time in an article, always use its full name, **Adobe Experience Manager**. After that, you can refer to it as **AEM**.

Day, Day Software, CQ, and CRX should not be used except where unavoidable such as in class names or referring to the history of AEM.