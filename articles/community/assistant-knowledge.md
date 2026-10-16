# Improving the Wiki Assistant's Knowledge

The **Fissile Industries Wiki Assistant** uses written public wiki documentation. It does not automatically learn new facts from conversations or privately train Groq's model.

## How to add knowledge

1. Add or edit a Markdown article under the `articles/` folder in the [Fissile Industries Documentation repository](https://github.com/Hamster-Systems/Fissile-Industries-Documentation), or use the website's administrator wiki editor.
2. Use a clear title and descriptive section headings. State what is **confirmed**, what is **planned**, and which mod version applies.
3. Give direct answers to common questions early in each article. For example, the [Project page](/wiki/community/project) explains who maintains Fissile Industries.
4. Link related wiki pages and check technical statements against the current mod source or a verified release.
5. Publish the changes and allow for the website's GitHub cache to refresh (often about 10 minutes; deployment settings may vary).

## Good documentation

- **Who owns Fissile Industries?** The [About Fissile Industries](/wiki/community/project) article identifies Hamster Systems and the official repositories.
- **Who is on the development team?** The [Team](/wiki/community/team) page lists only members who have been approved for public attribution.
- **What ores exist?** The [Ores](/wiki/materials/ores) page links material articles, some of which are explicitly drafts.

For better search matches, put the subject's commonly used terms in the heading and first paragraph, rather than hiding them only in a large table.

## Safety and privacy

- Never publish API keys, database passwords, private Discord conversations or private personal information in documentation.
- Do not fabricate crafting recipes, drop rates, radiation values, development roles or contributor identities.
- Mark draft content clearly until it is verified.
- The Groq integration retrieves public documentation excerpts at question time. The assistant's text responses should always link the articles supporting them.

## Related pages

- [Team](/wiki/community/team)
- [Documentation index](/wiki/index)
