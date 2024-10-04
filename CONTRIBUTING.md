# Contributing to Vibinex

First off, thank you for considering contributing to Vibinex! It's people like you that make Vibinex such a great tool.

## Code of Conduct

By participating in this project, you are expected to uphold our [Code of Conduct](CODE_OF_CONDUCT.md).

## How Can I Contribute?

### Reporting Bugs

- Identify the right repository associated with your issue. (If your issue spans across multiple repositories, it belongs [here](https://github.com/vibinex/vibinex/issues))
- Ensure the bug was not already reported by searching the GitHub Issues of associated repository.
- If you're unable to find an open issue addressing the problem, open a new one. Be sure to include a title and clear description, as much relevant information as possible, and a code sample or an executable test case demonstrating the expected behavior that is not occurring.

### Suggesting Enhancements

- Open a new issue with a clear title and detailed description of the suggested enhancement.
- Provide any relevant examples or mock-ups if applicable.

### Pull Requests

#### Getting the code

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

#### Setting up the project locally

#### General guidelines for your contributions.
1. If you've added code that should be tested, add tests.
2. Ensure the test suite passes.
3. Make sure your code lints.

## Styleguides

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

### JavaScript Styleguide

All JavaScript must adhere to [JavaScript Standard Style](https://standardjs.com/).

### Rust Styleguide

All Rust code must adhere to `rustfmt` and `clippy` standards.

## Additional Notes

### Issue and Pull Request Labels

This section lists the labels we use to help us track and manage issues and pull requests.

* `bug` - Issues that are bugs.
* `enhancement` - Issues that are feature requests.
* `documentation` - Issues or pull requests related to documentation.
* `good first issue` - Good for newcomers.

## Getting Started

For more detailed information on contributing, please refer to the [README.md](README.md) file in the main repository.

Thank you for contributing to Vibinex!