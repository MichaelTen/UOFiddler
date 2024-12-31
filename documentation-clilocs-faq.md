# Clilocs FAQ: Understanding Text Localization in Ultima Online

This FAQ addresses common questions and issues related to clilocs (client localization entries) in Ultima Online, particularly for free shard developers using tools like UOFiddler. This document focuses on the distinction between clilocs (text elements) and other aspects of game development, such as graphical asset management.

---

## What Are Clilocs?

Clilocs, short for "client localization entries," are numerical identifiers linked to specific text strings in Ultima Online's localization files. These entries allow:

- Displaying text such as item names, descriptions, and system messages.
- Supporting multiple languages by referencing a cliloc ID instead of hardcoding text into the client.
- Efficient text management for modifications and updates.

---

## Do Clilocs Affect Editing or Adding Art in UOFiddler?

**No, clilocs primarily impact text and do not directly interfere with editing or adding art.** Here is a breakdown:

### **Clilocs Scope**
- Clilocs only affect **text display** (e.g., item names, descriptions, system messages).
- Issues with clilocs result in missing or incorrect text, such as "megacliloc entry not found," but do not impact visual elements like sprites, textures, or animations.

### **Art and Graphics Management**
- Editing or adding graphical assets involves different files, such as `art.mul` and `gumpart.mul`, which are entirely separate from clilocs.
- Graphical assets will function as intended even if clilocs are missing or incorrect, but they may lack proper in-game names or descriptions.

### **When Clilocs and Art Interact**
- Clilocs are relevant if you want to:
  - Assign a name or description to new art (e.g., a custom weapon or item).
  - Display custom system messages related to new art.
- In these cases, cliloc entries must be added or updated, but any issues with clilocs will only affect text, not visuals.

---

## Recommendations for Managing Clilocs

1. **Separate Concerns**:
   - Handle text (clilocs) and graphical assets (art files) as independent tasks.
   - Only modify clilocs if you need text changes or descriptions for new assets.

2. **Validate Changes**:
   - When editing clilocs, ensure entries are properly formatted and unique to avoid conflicts.
   - Test text changes thoroughly in the client.

3. **Distribute Files**:
   - Updated cliloc files must be distributed to players to reflect changes.

4. **Test Client-Server Integration**:
   - Ensure that graphical assets and their associated clilocs are correctly linked during testing.

---

## Related Tools and Resources

### UOFiddler
- **Purpose**: Manage and customize client files, including clilocs and graphical assets.
- **Features**: Edit cliloc entries, view and modify art, manage hue files.

### Useful Links
- [UOFiddler GitHub Repository](https://github.com/polserver/UOFiddler)
- [ServUO Developer Forum](https://www.servuo.com)
- [Cliloc Format Guide](https://docs.polserver.com/ClilocFormat)

---

## Conclusion

Clilocs are essential for managing text localization and descriptions in Ultima Online. While they do not directly impact art or graphical assets, they are required for naming and describing new content. Proper management and testing ensure a seamless integration of text and visuals in free shard development.

For more information, refer to [issue #124](https://github.com/polserver/UOFiddler/issues/124) on the UOFiddler repository or contact the developer community.
