# Workflow Files

This directory contains the n8n workflow JSON export.

## Files

- **workflow.json** - The main n8n workflow file

## Replacing the Template

To use this template for your own workflow:

1. Export your workflow from n8n:
   - Open your workflow in n8n
   - Click the three dots menu (⋮)
   - Select "Download"
   - Save the JSON file

2. Replace `workflow.json` with your exported file:
   ```bash
   cp /path/to/your-workflow.json workflow/workflow.json
   ```

3. Update the documentation:
   - Edit the README.md with your workflow details
   - Update the Mermaid diagram to match your workflow
   - Document any required credentials or configuration

## Workflow Structure

Your workflow file should include:

- **Nodes**: All workflow nodes with their configurations
- **Connections**: How nodes are connected
- **Settings**: Workflow execution settings
- **Credentials**: Referenced (but not containing actual credential data)

## Important Notes

- **Never commit actual credentials** or API keys in the workflow file
- **Use credential names** that reference n8n's credential store
- **Test the workflow** before committing to ensure it imports correctly
- **Document any custom nodes** or special requirements

## Validation

Before committing changes, validate the JSON:

```bash
# Check JSON syntax
jq . workflow.json > /dev/null && echo "Valid JSON"

# Check for sensitive data (basic check)
grep -i "password\|token\|secret\|key" workflow.json
```

If the grep command finds anything, review those fields to ensure they're credential references, not actual values.
