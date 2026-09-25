# grounded.io

`grounded.io` is a study-focused productivity tool that helps users stay away from distracting applications and websites during dedicated focus sessions. When a blocked service such as YouTube, Discord, Steam, or another configured distraction is opened, grounded.io safely interrupts the session by displaying a warning, closing the distraction, or activating a simulated “system crash” screen (evidently if it actually crashes your pc it is "malware" and not legal???). The project is designed for education and experimentation and does not intentionally damage files, crash the operating system, or interfere with unrelated applications.

## Getting Started

These instructions will help you get a copy of the project up and running on your local machine for development and testing purposes. See [Deployment](#deployment) for notes on how to deploy the project on a live system.

### Prerequisites

You will need the following software:

- Git
- Node.js 20 or later
- npm 10 or later
- Supported operating system
- Permission to run local desktop automation during development

Verify your installation:

```bash
git --version
node --version
npm --version
```

For safety, development and testing should be performed in a virtual machine or isolated test account. The project should use simulated lockouts and warning screens rather than forcibly crashing the host operating system.

### Installing

Clone the repository:

```bash
git clone https://github.com/NAU-OSS/grounded
cd grounded
```

Install the project dependencies:

```bash
npm install
```

Create a local configuration file:

```bash
touch .env
```

Update the configuration with the applications and websites that should be blocked during a focus session:

```env
FOCUS_DURATION=50
WARNING_MODE=simulated
BLOCKED_APPS=youtube,discord,steam
```

Start the development environment:

```bash
npm run dev
```

Create a test focus session:

```bash
npm run focus -- --duration 25
```

When a configured distraction is detected, grounded.io displays a warning or simulated interruption screen. The demonstration mode must not terminate the operating system, delete files, corrupt data, or interfere with applications outside the configured test scope.

Stop the development environment with:

```bash
npm run stop
```

Example status output:

```text
Focus session active
Duration: 25 minutes
Blocked distractions: YouTube, Discord, Steam
Mode: Simulated
Status: Grounded
```

## Running the Tests

Run the complete automated test suite with:

```bash
npm test
```

Run tests in watch mode during development:

```bash
npm run test:watch
```

### Break down into end-to-end tests

End-to-end tests verify that a focus session can be created, configured, started, paused, and completed successfully. They also confirm that configured distractions trigger the expected warning or simulated lockout behavior without causing system damage.

Run the end-to-end tests with:

```bash
npm run test:e2e
```

Example scenarios include:

- Starting a focus session with a custom duration
- Detecting a configured distraction
- Displaying the simulated interruption screen
- Allowing the user to end a session safely
- Preserving session history after completion
- Ignoring applications that are not on the block list

### And coding style tests

Coding style tests check formatting, naming conventions, static analysis, and common programming errors. Keeping these checks consistent makes the project easier to review and maintain.

Run the formatter:

```bash
npm run format
```

Run the linter:

```bash
npm run lint
```

Run the type checker:

```bash
npm run typecheck
```

## Deployment

grounded.io should be deployed in a controlled environment where users understand how focus sessions operate and can safely stop the application.

Before deployment:

1. Set `WARNING_MODE=simulated` unless a platform-specific, reversible blocking mechanism has been reviewed and approved.
2. Configure the list of blocked applications and websites.
3. Set appropriate default focus-session durations.
4. Test the application in a virtual machine or non-production user account.
5. Confirm that the application has a reliable emergency stop mechanism.
6. Verify that no files are deleted, encrypted, corrupted, or modified outside the application’s data directory.

Build the production package with:

```bash
npm run build
```

Start the production build with:

```bash
npm start
```

For a live deployment, use a process manager such as `systemd`, Docker, or another approved service manager. Avoid deploying the application with unrestricted administrator or root privileges.

## Built With

- [Node.js](https://nodejs.org/) - Runtime environment
- [TypeScript](https://www.typescriptlang.org/) - Programming language
- [Electron](https://www.electronjs.org/) - Desktop application framework
- [Vitest](https://vitest.dev/) - Unit and integration testing
- [Playwright](https://playwright.dev/) - End-to-end testing
- [ESLint](https://eslint.org/) - Code quality and linting
- [Prettier](https://prettier.io/) - Code formatting

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details about the code of conduct, development workflow, testing requirements, and the process for submitting pull requests.

All contributions should preserve the project’s safety requirements:

- Do not add destructive behavior.
- Do not intentionally crash or damage the host operating system.
- Do not collect unnecessary personal information.
- Ensure that blocking behavior is reversible.
- Include tests for new functionality.
- Document any platform-specific behavior.

## Versioning

We use [Semantic Versioning](https://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/NAU-OSS/grounded/tags).

## Authors

- **SWBodenhemier** - _Initial work_ - [swBodenhemier](https://github.com/swBodenhemier)

See also the list of [contributors](https://github.com/NAU-OSS/grounded/contributors) who participated in this project.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by focus timers, distraction blockers, and digital well-being tools
- Thanks to the open-source communities behind Node.js, TypeScript, Electron, Vitest, and Playwright
- Thanks to contributors who improve the project’s accessibility and safety
- Hat tip to anyone whose code or ideas were used in accordance with their license
- Created as an educational open-source project about productivity software and responsible desktop automation
