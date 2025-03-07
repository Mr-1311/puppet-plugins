# Add New Plugin to Puppet Plugins

Thank you for contributing to the Puppet Plugins community! Please follow the steps below to ensure your plugin is properly submitted. Fill out this template and check all boxes to confirm completion.

## Plugin Submission Steps

1. **Create a Release in Your Plugin Repository**
   - [ ] Created a release in my plugin repository
   - [ ] Included `readme.md`, `plugin.wasm`, and `manifest.json` as release assets
   - [ ] If extra files or executables are needed under the plugin's data folder, added them as release assets
   - [ ] Used semantic versioning (e.g., `v1.0.0`) for the release tag

2. **Edit plugins.json**
   - [ ] Edited `plugins.json` in this PR to add my plugin as a JSON object
   - [ ] Verified that the plugin `name` is unique (search `plugins.json` for existing names)
   - [ ] Ensured the `name` does not contain "puppet" or "official"
   - [ ] Added a comma after the previous entry's closing brace `}` if applicable
   - [ ] Made no other changes to the repository in this PR

   Example plugin entry:
   ```json
   {
     "name": "your-plugin-name",
     "author": "Your Name",
     "description": "Brief plugin description",
     "platforms": ["macos", "windows", "linux"],
     "repo": "https://github.com/your-username/your-repo"
   }
   ```

## Validation Checklist
The bot will automatically validate your PR. Ensure:

- [ ] Only plugins.json is modified in this PR
- [ ] JSON syntax is valid
- [ ] All required fields are present (name, author, description, platforms, repo)
- [ ] Plugin name is unique and follows naming rules
- [ ] Platforms are valid (macos, windows, linux)
- [ ] Repository URL is a valid GitHub URL `(https://github.com/username/repo)`

## Additional Notes
- If this PR fails validation, check the bot's comment for specific reasons
- After successful validation, the bot will automatically merge this PR
- For questions, refer to the `Puppet` documentation or contact the maintainers

Thank you for your contribution!
