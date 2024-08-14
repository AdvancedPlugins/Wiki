# AdvancedPlugins' Plugin Wiki

This repository contains the wiki content for AdvancedPlugins' products. It's integrated with GitBook for automatic updates and easy navigation.

## How to Contribute

### Adding a New Page

1. Create a new file with a `.md` extension in the appropriate directory.
2. Write your content using Markdown syntax.
3. Update the `SUMMARY.md` file to add your new page to the sidebar menu.

### Editing Existing Content

1. Navigate to the `.md` file you want to edit.
2. Make your changes, ensuring you maintain proper Markdown formatting.
3. If you've significantly changed the content or title, remember to update the `SUMMARY.md` file accordingly.

## Best Practices

- Use descriptive file names: For example, `multi-type-jobs.md` instead of `page1.md`.
- Organize content in logical directories: Group related pages in folders like `jobs/`, `commands/`, etc.
- Use proper Markdown formatting: Utilize headers, lists, code blocks, and other Markdown features for clear, readable content.

## GitBook Integration

- All changes pushed to the `main` branch will automatically update the GitBook wiki.
- The sidebar structure in GitBook is determined by the `SUMMARY.md` file.

## SUMMARY.md Structure

The `SUMMARY.md` file should follow this basic structure:

```markdown
# Table of contents

* [Introduction](README.md)

## Section 1

* [Page 1](section1/page1.md)
* [Page 2](section1/page2.md)

## Section 2

* [Page 3](section2/page3.md)
* [Page 4](section2/page4.md)
