# Puppet Plugins

Welcome to the Puppet Plugins repository! This is a community-driven collection of plugins for the Puppet Plugin Launcher. Here, developers can share their plugins by adding them to the `plugins.json` file, which is automatically validated and reviewed before inclusion.

## Purpose

This repository serves as a central hub for:
- Discovering community-created plugins for the Puppet Plugin Launcher
- Sharing your own plugins with the Puppet community
- Maintaining a curated list of plugins in `plugins.json`

## How to Contribute a Plugin

To add your plugin to this repository, follow these steps:

### 1. Create a Release in Your Plugin Repository
- Create a release in your own GitHub repository containing your plugin
- Include the following assets in your release:
  - `readme.md`: Documentation for your plugin
  - `plugin.wasm`: The compiled WebAssembly plugin file
  - `manifest.json`: Plugin metadata
- If your plugin requires additional files or executables:
  - Add them as release assets
  - These files (except `readme.md`, `plugin.wasm`, `manifest.json`, and source code) will be placed in your plugin's `data` folder
- Use [semantic versioning](https://semver.org/) for your release tag (e.g., `v1.0.0`)

### 2. Update `plugins.json`
- Fork this repository (https://github.com/Mr-1311/puppet-plugins)
- Edit `plugins.json` to add your plugin as a JSON object:
  ```json
  {
    "name": "your-plugin-name",
    "author": "Your Name",
    "description": "Brief plugin description",
    "platforms": ["macos", "windows", "linux"],
    "repo": "https://github.com/your-username/your-repo"
  }
  ```
- Requirements:
  - name: Must be unique (search plugins.json to confirm) and cannot contain "puppet" or "official"
  - platforms: Must be a subset of ["macos", "windows", "linux"]
  - repo: Must be a valid GitHub URL
  - Add a comma after the previous entry's closing brace } if you're not adding the last entry
- Make no other changes to the repository

### 3. Submit a Pull Request
- Create a pull request (PR) with your changes to plugins.json
- Use the provided PR template (automatically loaded) to document your submission
- Use your plugin name as PR title
- The automated workflow will validate your PR and label for last human check

## Automated Validation Process
A GitHub Action workflow automatically processes your PR:

- Validation Checks:
  - Only plugins.json is modified
  - JSON syntax is valid
  - Exactly one new plugin is added
  - All required fields are present
  - Plugin name is unique and follows naming rules
  - Platforms are valid
  - Repository URL is a valid GitHub URL
- Outcomes:
  - If validation fails: A comment will be added to your PR with the specific error
  - If validation succeeds:
    - The PR will be labeled "ready to merge"
    - Assigned to maintainer for final review
    - You’ll receive a comment confirming success
   
## License
MIT License

Thank you for contributing to the Puppet Plugins community!
