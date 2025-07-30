# Techniques Table Maintenance

## Overview

The techniques table on the homepage is now generated dynamically from a data file, making it much easier to maintain and update.

## How it works

1. **Data File**: `_data/techniques-table.yml` contains the table structure organized by columns
2. **Template**: `index.html` uses Liquid templating to generate the table from the data
3. **Techniques**: Individual technique files in `_techniques/` provide the content and metadata

## Adding or Modifying Techniques

### 1. Add a new technique file

Create a new markdown file in `_techniques/` with the following structure:

```markdown
---
layout: technique
title: Your Technique Title
description: Brief description of the technique
---

# Your Technique Title

## Summary

Your technique content here...
```

### 2. Update the table

Edit `_data/techniques-table.yml` to include your new technique:

```yaml
columns:
  - name: "Column Name"
    techniques:
      - "existing-technique-1"
      - "your-new-technique"  # Add your technique reference here
      - null  # Empty cell for additional rows
```

### 3. Technique References

- Use the filename (without `.md` extension) as the reference
- Example: `aitm-phishing.md` → reference as `aitm-phishing`
- The system will automatically find the technique by matching the filename in the path and display its title

## Benefits

- **Easy Maintenance**: Just update the data file to change table structure
- **Column-Based Organization**: More intuitive to maintain by organizing techniques by category
- **Variable Length Columns**: Each column can have different numbers of techniques
- **Automatic Empty Cells**: Empty cells are automatically handled and styled
- **Consistent Links**: Links are automatically generated from technique metadata
- **Error Handling**: Missing techniques are clearly marked
- **Scalable**: Easy to add new columns or techniques within columns

## File Structure

```
_data/
  techniques-table.yml    # Table configuration
_techniques/
  technique-1.md         # Individual technique files
  technique-2.md
  ...
index.html               # Template that generates the table
```

## Example: Adding a New Technique

To add a new technique to the "Targeting" column:

1. Create `_techniques/new-targeting-technique.md`:
```markdown
---
layout: technique
title: New Targeting Technique
description: Description of the new technique
---

# New Targeting Technique
...
```

2. Update `_data/techniques-table.yml`:
```yaml
columns:
  - name: "Targeting"
    techniques:
      - "apps-weak-security"
      - "new-targeting-technique"  # Add your new technique here
      - null
```

## Troubleshooting

If a technique shows as "not found":
1. Check that the filename reference in `techniques-table.yml` matches the actual filename
2. Ensure the technique file has the correct front matter with `title` and `layout: technique`
3. Verify the technique file is in the `_techniques/` directory