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

We welcome contributions to the Vibinex project. Please follow these steps to contribute:

1. Fork the main [Vibinex repository](https://github.com/vibinex/vibinex) on GitHub.
2. Manually fork each submodule repository ([vibinex-server](https://github.com/vibinex/vibinex-server), [vibi-dpu](https://github.com/vibinex/vibi-dup), and [chrome-extension](https://github.com/vibinex/chrome-extension)) on GitHub.

3. Clone your fork of the main repository:
	```bash
	git clone https://github.com/[your-username]/vibinex.git
	```
4. Update the submodule URLs to point to your forks:
	```bash
	cd vibinex
	git config --file=.gitmodules submodule.vibinex-server.url https://github.com/[your-username]/vibinex-server.git
	git config --file=.gitmodules submodule.vibi-dpu.url https://github.com/[your-username]/vibi-dpu.git
	git config --file=.gitmodules submodule.chrome-extension.url https://github.com/[your-username]/chrome-extension.git
	```
5. Initialize and update the submodules:
	```bash
	git submodule update --init --recursive
	```
6. Create a new branch in the relevant submodule(s) where you want to make changes:
	```bash
	cd [submodule-directory]
	git checkout -b [your-feature-branch]
	```
7. Make your changes in the submodule(s).
8. Commit and push your changes to your fork of the submodule:
	```bash
	git add [relevant-modified-files]
	git commit -m "Your descriptive commit message"
	git push origin [your-feature-branch]
	```
9. Create a pull request for the submodule changes from your fork to the original submodule repository.
10. Once the submodule pull request is merged, update the submodule reference in the main Vibinex repository:
	```bash
	cd [back-to-main-repo]
	git submodule update --remote
	git add [submodule-directory]
	git commit -m "Update submodules: [describe your feature]"
	git push origin main
	```
11. Create a pull request in the main Vibinex repository to update the submodule pointer.

For more detailed information on contributing, please see our [CONTRIBUTING.md](CONTRIBUTING.md) file.

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or concerns, please open an issue in this repository or contact [Discord](https://discord.gg/caVSraCvpk).
