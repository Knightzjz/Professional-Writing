## Link

Links in technical documents direct users to other titles in the same document, other adjacent documents, or external sites. This section mainly introduces the recommended guidelines for using links in technical documentation written in the Markdown language.

Example of link formatting in Markdown:

- Links to other headings in the same document: `[Product_Architecture](#Product_Architecture)`
- Links to other adjacent documents: `[Product Architecture](../docs/architecture.md)`
- Links to external sites: `[Contributor Guidelines](https://docs.microsoft.com/en-us/contribute/)`

### Description of the link

The content in square brackets `[]` in a Markdown link is the descriptive text of the link. The description of the link needs to conform to the following specifications.

- The link description must summarize the general content of the linked document or page, which is good for search engine optimization. For example, the link description can be the title of the linked page.

    - [Error example]

        - See `[trouble-shooting.md](trouble-shooting.md)` for details
        - For details, please click `[here](trouble-shooting.md)`

    - 【Correct example】

        - For more details about the above configuration items, please refer to the related configuration items of `[function configuration set](#function configuration set)`.
        - See `[Troubleshooting Documentation](trouble-shooting.md)` for details.

- Link descriptions of the same type should be as uniform as possible. For example, it is not advisable to have different descriptions with the same meaning, such as "see details", "see details", "see details", "see details", etc. multiple times in the same document.

### link path

The content in parentheses `()` in a Markdown link is the path of the link. The path of the link needs to conform to the following specifications.

- **If you link to other adjacent documents, and the linked document is long, it is recommended to link to the anchor**. Linking to an anchor means linking to a certain level of heading. Markdown supports adding "#title name" after the file name of the link path, that is, you can link to a specific title of the file.

    - [Example] `[Configuration File](trouble-shooting.md#Configuration File)` This link will link to the "Configuration File" heading of the trouble-shooting.md file.

- Link paths should be as uniform as possible. For example, relative or absolute paths should be used consistently when linking to non-external sites. Mixing relative and absolute paths is not recommended.

- It is recommended to reduce the number of times users are linked to external sites, so as not to affect the user experience due to the failure of the pages of external sites.

    > Meaning of external site: A link B appears in the document of website A. If the domain name or server of B is different from that of A, then for the document of website A, the link B is an external site. For example: cloud.google.com is an internal site relative to support.google.com; cloud.google.com is an external site relative to kubernetes.io.

- **If the user must be linked to an external site, it is recommended to add a clear sign after the external link to remind the user that the link will lead to an external site. **

    > Due to the different terms of use and privacy policies of different websites, users who use the current site generally default that the user has accepted the legal provisions of the current site. Before jumping out of the current site, the website maintainer has the responsibility to remind the user that the current link is to an external site. If the user has a problem after jumping out, it is not the responsibility of the current site.

    - [Example 1] If the front-end capability is sufficient, you can add a general external link icon effect after the external link, for example: [Contributor list](https://github.com/yikeke/zh-style-guide/graphs/contributors ).

    - [Example 2] In Markdown, you can simply add `"click to go to an external site"` or `"click to go to XXX website"` and other information after the link path, such as `[link description](link path" Go to the prompt ")` of external links, you can achieve the effect of prompting when the mouse hovers over a hyperlink under normal rendering.
