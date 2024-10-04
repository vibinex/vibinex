# Vibinex Code Review
[![Discord](https://img.shields.io/discord/534485763354787851.svg)](https://discord.gg/caVSraCvpk)

Central repository for the Vibinex project, containing other repositories as submodules.

## Overview
Vibinex modifies the UX for code-hosting websites like GitHub and Bitbucket to make it easier to perform high-quality code reviews.
If you spend a significant part of your day reviewing pull requests, try out tool out.

- To know more about the features of the product, visit our website ([vibinex.com](https://vibinex.com))
- To setup Vibinex in your repositories, get started from [our documentation page](https://vibinex.com/docs)
- If you face any issues in setting up, contact us on [Discord](https://discord.gg/caVSraCvpk), [email](mailto:contact@vibinex.com) or [WhatsApp](https://wa.me/918511557566).

## Submodules
There are three submodules of this product:
1. [User-side data processing unit (Rust)](https://github.com/vibinex/vibi-dpu)
2. [Server for backend and website (NextJS)](https://github.com/vibinex/vibinex-server)
3. [Browser Extension](https://github.com/vibinex/chrome-extension)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/vibinex/.github/assets/7858932/1246e2b8-9ba9-4e27-af30-b159b9c8e9bb">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/vibinex/.github/assets/7858932/1530e2d0-b118-484f-84a1-ef26ab305326">
  <img alt="Vibinex core repo" src="https://github.com/vibinex/.github/assets/7858932/1530e2d0-b118-484f-84a1-ef26ab305326">
</picture>

### Architectural Overview
We take privacy extremely seriously. The purpose of the Rust service is to keep the user's data (code, events, config, server logs, etc.) in the user's infrastructure.
Only non-reproducible encrypted/hashed metadata is shared with Vibinex's servers.

This project follows a dual-backend architecture to ensure privacy while serving data-enabled features. Here is the architectural diagram (over-simplified for high-level understanding):

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/vibinex/.github/assets/7858932/493b3052-b462-4bb8-a9cd-ffa8e1018960">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/vibinex/.github/assets/7858932/d5a97883-64ef-498f-b97a-318b6675ac87">
  <img alt="2-backend architecture" src="https://github.com/vibinex/.github/assets/7858932/d5a97883-64ef-498f-b97a-318b6675ac87">
</picture>

## Contributing

We welcome contributions to the Vibinex project. We also provide compensation for timely contributions to important issues.

To start contributing to Vibinex, please see our [CONTRIBUTING.md](CONTRIBUTING.md) file.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or concerns, please open an issue in this repository or contact [Discord](https://discord.gg/caVSraCvpk).
