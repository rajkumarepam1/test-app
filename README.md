# Quiz CLI

An interactive command-line quiz game for practicing JavaScript, Node.js, and general programming knowledge. Choose a category and question count, answer multiple-choice questions, and review your score, explanations, and missed answers.

## Features

- Three categories: JavaScript Basics, Node.js Fundamentals, and General Programming.
- Choose all available questions or a set of three or five when the selected category has enough questions.
- Shuffled question order, numbered answer choices, and input validation.
- Per-question feedback and explanations, plus a progress bar.
- Final score, percentage-based feedback, and review of incorrect answers.
- Option to play again.
- ANSI terminal colors implemented without third-party runtime dependencies.

## Technology stack

- JavaScript with Node.js ES modules.
- Node.js built-ins: `node:fs/promises`, `node:url`, `node:path`, and `node:readline`.
- JSON for the question bank.
- npm scripts for starting the application and invoking Node's test runner.

`package.json` does not declare third-party package dependencies.

## Project structure

```text
.
├── README.md
├── colors.js         # ANSI terminal color helpers
├── index.js          # CLI entry point and application loop
├── input.js          # Readline prompts and input handling
├── package.json      # Metadata, scripts, and Node requirement
├── questions.json    # Categories and quiz question data
└── quiz.js           # Quiz state, question flow, scoring, and results
```

The repository listing also includes `.DS_Store`, a macOS metadata file not used by the application.

> **File layout mismatch:** The listed JavaScript and JSON files are at the repository root. However, `index.js` imports modules from `./src/` and loads question data from `./data/questions.json`. Those paths do not match the files in the repository listing. The application will need the paths corrected or the files placed in the expected directories before it can run successfully.

## Prerequisites

- Node.js 18 or later (`engines` in `package.json`).
- npm to run the package scripts.

## Installation and setup

```sh
git clone https://github.com/rajkumarepam1/test-app.git
cd test-app
```

No external dependencies are declared, so no dependency installation is required. Resolve the file layout mismatch above before running the CLI.

## Environment configuration

No environment variables or environment configuration files are specified in the repository.

## Usage

The configured start command is:

```sh
npm start
```

This runs `node index.js`. Once the file paths resolve, the CLI prompts for a category and question count, then accepts numbered answers. Press Enter to continue between prompts; after the results, answer `y` at the replay prompt to begin another quiz.

As checked in, the root-level file layout does not satisfy the paths referenced by `index.js`, so the command is not expected to run until that mismatch is addressed.

## Available scripts

| Script | Command | Description |
| --- | --- | --- |
| `start` | `node index.js` | Starts the interactive quiz CLI. |
| `test` | `node --test` | Runs Node.js's built-in test runner. |

## Testing

Run the configured test script:

```sh
npm test
```

It invokes `node --test`. The repository listing does not include test files, so no project-specific tests are present in the inspected contents.

## Build and deployment

No build or deployment configuration is listed. `package.json` defines no build script.

## API

No HTTP or other network API is defined in the inspected files; this is a local command-line application.

## Contributing

Use the usual Git workflow to propose changes. Keep changes consistent with the existing JavaScript ES module structure, and update documentation or tests when relevant. No project-specific contribution policy is specified in the repository.

## License

`package.json` declares the MIT license. No separate license file appears in the repository listing.

## Notes and limitations

- The paths in `index.js` (`./src/input.js`, `./src/quiz.js`, `./src/colors.js`, and `./data/questions.json`) conflict with the root-level file paths in the repository listing. Fix the mismatch before expecting the app to launch.
- No test files, environment-variable requirements, build configuration, or deployment instructions were found in the listed contents.
- The package description emphasizes JavaScript learning; the included questions also cover Node.js and general programming.