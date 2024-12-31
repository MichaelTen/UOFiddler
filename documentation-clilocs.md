These are notes and nothing more. Some of what is here migtht be inaccurate. If any of this is wrong or inaccurate please submit a pull request or contact the original contributor. 

# Cliloc Documentation for Ultima Online Free Shards

This documentation provides an overview of "clilocs" in Ultima Online, particularly in the context of free shards and open development. The focus is to address their role in localization, customization, and their relevance to [issue #124 on the UOFiddler repository](https://github.com/polserver/UOFiddler/issues/124).

## What are Clilocs?

Clilocs (short for "client localization") are numerical identifiers that reference specific text strings in Ultima Online's localization files. These entries are used by the game client to display text such as item names, descriptions, and system messages.

### Key Features of Clilocs:
1. **Localization Support**: Clilocs allow the game to support multiple languages. By referencing a cliloc ID, the game displays text in the appropriate language, as configured by the player's client.
2. **Efficient Text Management**: Clilocs centralize the management of in-game text. This makes it easy to update or modify text strings without altering the core game code.
3. **Customization in Free Shards**: Developers use tools like UOFiddler to edit cliloc entries, enabling the addition of custom text for items, system messages, or other game elements.

## How Clilocs Relate to Issue #124 in UOFiddler

[Issue #124](https://github.com/polserver/UOFiddler/issues/124) discusses challenges or potential bugs related to cliloc entries within UOFiddler. UOFiddler is a tool widely used by free shard developers to manage and customize various aspects of the Ultima Online game client, including clilocs.

### Relevant Context:
- **Editing Cliloc Entries**: UOFiddler allows shard developers to modify cliloc entries for creating custom content. However, improper handling of cliloc files can result in errors or inconsistencies in the displayed text.
- **Distribution of Changes**: Custom cliloc entries need to be distributed to players via updated localization files. Without proper distribution, players will not see the intended text changes.
- **Error Handling**: Cliloc IDs set to `0` or invalid values may trigger errors such as "megacliloc entry not found" or similar fallback messages.

### Recommendations for Developers:
1. **Verify Cliloc Edits**: When modifying cliloc entries using UOFiddler, ensure that all entries are correctly formatted and validated to prevent errors in the game client.
2. **Distribute Updated Files**: Provide players with the updated cliloc files to ensure they experience the intended changes.
3. **Use Unique IDs**: Avoid reusing existing cliloc IDs for new content to prevent conflicts with the default localization strings.
4. **Test Thoroughly**: Always test changes on a local client before deploying updates to a live shard.

## Tools for Managing Clilocs

### UOFiddler
UOFiddler is a popular tool among free shard developers for editing Ultima Online's client files, including cliloc entries.

#### Features:
- View and edit existing cliloc entries.
- Add custom cliloc entries for new content.
- Export and distribute updated cliloc files.

#### Common Issues:
- Errors when saving or exporting cliloc files.
- Compatibility issues with older or modified game clients.

### Alternatives to UOFiddler
- **CentrED**: Primarily used for world editing but can handle certain localization tasks.
- **ServUO Tools**: Includes scripts and utilities for managing cliloc entries programmatically.

## Resources
- [UOFiddler Repository](https://github.com/polserver/UOFiddler)
- [Ultima Online Developer Community](https://www.servuo.com)
- [Cliloc Format Guide](https://docs.polserver.com/ClilocFormat)

## Conclusion
Clilocs are an essential component of Ultima Online's localization system, enabling dynamic and multilingual text display. Proper management of cliloc entries using tools like UOFiddler can greatly enhance the customization capabilities of free shards. Addressing challenges such as those in [issue #124](https://github.com/polserver/UOFiddler/issues/124) requires careful validation, testing, and distribution of updated localization files.
