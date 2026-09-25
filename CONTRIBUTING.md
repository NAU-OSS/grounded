# Contributing to grounded.io

Thank you for your interest in contributing to grounded.io! Contributions of all kinds are welcome, including bug reports, feature ideas, documentation improvements, design feedback, accessibility suggestions, and code changes.

grounded.io is a study and focus tool. Because it interacts with applications and desktop environments, safety is especially important. Contributions must keep the project reversible, transparent, and non-destructive.

## Code of Conduct

Please read through our [code of conduct](CODE_OF_CONDUCT.md)

## Ways to Contribute

The following types of contributions are welcome:

- Bug reports and reproduction steps
- Pull requests fixing bugs
- New productivity and focus-session features
- Improvements to the user interface
- Accessibility improvements
- Documentation updates
- Test coverage
- Performance improvements
- Translations and localization
- Platform compatibility improvements
- Security reviews and responsible disclosures
- Design feedback and usability testing
- Examples, tutorials, and project demonstrations

You do not need to write code to contribute. A well-written issue, helpful documentation improvement, or thoughtful design suggestion can make a meaningful difference.

## Before You Start

Before opening an issue or pull request:

1. Search existing issues and pull requests to see whether the topic has already been discussed.
2. Use the latest version of the project when reproducing a bug.
3. Check the documentation and configuration examples.
4. Make sure your proposed change fits the project’s focus and safety principles.
5. For larger changes, open an issue first so the approach can be discussed.

Please do not include passwords, API keys, private messages, personal data, or other sensitive information in issues, logs, screenshots, or pull requests.

## Safety Requirements

grounded.io must never intentionally:

- Crash or damage the host operating system
- Delete, encrypt, or corrupt user files
- Disable security software
- Modify unrelated applications or system settings
- Lock users out of their computer
- Collect unnecessary personal information
- Hide how blocking or interruption behavior works
- Make it difficult for users to stop an active session

Any interruption or blocking feature must be reversible and clearly explained to the user. Simulated crash screens and warning messages are preferred for demonstrations and testing.

Changes that interact with operating-system processes, application windows, network access, or startup behavior require additional documentation and tests.

## Development Setup

Refer to the [README](README.md)

## Branching and Commit Guidelines

Create a separate branch for each change:

```bash
git checkout -b feature/session-statistics
```

Use clear, descriptive branch names such as:

- `feature/add-break-reminders`
- `fix/session-stop-button`
- `docs/update-installation-guide`
- `test/add-focus-session-coverage`

Write commit messages in the imperative mood:

```text
Add configurable focus-session duration
```

Good commit messages are concise and describe one logical change. Avoid combining unrelated fixes in a single commit.

## Reporting a Bug

Please use the bug report template when opening an issue. Include enough information for someone else to reproduce the problem.

A helpful bug report should contain:

- A clear, descriptive title
- The version of grounded.io
- Your operating system and version
- Steps to reproduce the problem
- Expected behavior
- Actual behavior
- Relevant logs or error messages
- Screenshots or recordings, when useful
- Whether the issue occurs consistently
- Any temporary workaround you discovered

Please remove personal information and sensitive data from logs before posting them.

## Suggesting a New Feature

Feature suggestions are welcome. Before proposing a new feature, please consider:

- What problem would the feature solve?
- Who would benefit from it?
- How would it support focused study or responsible productivity?
- Could the feature be implemented in a reversible and transparent way?
- What would the simplest useful version look like?
- Are there existing features that could be improved instead?

Please describe the proposed behavior rather than prescribing a specific implementation. This gives maintainers and contributors room to explore the best solution together.

## Opening a Pull Request

Before opening a pull request:

1. Create a focused branch from the latest version of the default branch.
2. Make the smallest change that solves the problem.
3. Add or update tests where appropriate.
4. Update documentation if user-facing behavior changes.
5. Run the formatter, linter, type checker, and test suite.
6. Review your own changes before submitting.
7. Open the pull request using the pull request template.

Pull requests should:

- Explain what changed and why.
- Link to a related issue when one exists.
- Include testing instructions.
- Document platform-specific behavior.
- Call out limitations or follow-up work.
- Avoid unrelated formatting or refactoring changes.
- Preserve safe, reversible behavior.

## Documentation

- [ ] Documentation has been updated where necessary.
- [ ] Configuration examples have been updated where necessary.
- [ ] No documentation changes are needed.

## Safety Review

- [ ] This change does not intentionally crash or damage the host operating system.
- [ ] This change does not delete, encrypt, or corrupt user files.
- [ ] Any blocking or interruption behavior is reversible.
- [ ] The user can clearly understand what the feature does.
- [ ] No unnecessary personal information is collected.
- [ ] Operating-system integration has been tested safely.

## Screenshots or Recordings

Add screenshots or recordings for user-interface changes.

## Checklist

- [ ] I have searched for related issues and pull requests.
- [ ] I have added or updated tests where appropriate.
- [ ] I have run the formatter.
- [ ] I have run the linter.
- [ ] I have run the type checker.
- [ ] I have tested the relevant behavior locally.
- [ ] My commits are focused and clearly described.
- [ ] I have removed sensitive information from logs and screenshots.

## Review Process

After submitting a pull request, a maintainer may:

- Ask questions about the implementation.
- Request additional tests or documentation.
- Suggest a simpler or safer approach.
- Check behavior on another supported platform.
- Request changes to improve accessibility or usability.

Please do not take requested changes personally. Reviews help keep the project reliable, understandable, and safe for everyone.

If your pull request becomes outdated, update it with the latest changes from the default branch when requested. Maintainers may squash commits when merging to keep the project history easy to follow.

## Documentation and Accessibility

Documentation contributions should be clear and welcoming to people with different levels of technical experience.

When changing the interface or user experience:

- Use clear labels and instructions.
- Avoid relying on color alone to communicate status.
- Support keyboard navigation where practical.
- Provide useful text for warnings and errors.
- Make it clear how to pause or stop a focus session.
- Avoid confusing or alarming language.
- Include alternative text for meaningful images.

## Security Issues

Please do not report security vulnerabilities in a public issue.

Instead, contact the maintainers privately using the security contact listed in the repository. Include:

- A description of the potential vulnerability
- Steps to reproduce it
- The affected version
- The possible impact
- Any suggested mitigation

Please allow maintainers reasonable time to investigate before publicly disclosing a security issue.

## License

By contributing to grounded.io, you agree that your contributions will be licensed under the MIT License included in this repository.

Thank you for helping make grounded.io more useful, reliable, accessible, and enjoyable for people who want to focus.
