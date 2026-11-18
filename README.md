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
├── package-lock.json # npm lockfile
├── package.json      # Metadata, scripts, and Node requirement
├── questions.json    # Categories and quiz question data
└── quiz.js           # Quiz state, question flow, scoring, and results
```

The repository listing also includes `.DS_Store`, a macOS metadata file not used by the application.

## Application Execution Flow

1. On startup, `index.js` loads and parses the question bank from `questions.json`.
2. The CLI displays the available quiz categories from that data.
3. The user selects a category and chooses a question count. The available count options depend on the number of questions in the selected category.
4. The application presents the selected questions in shuffled order. For each question, it validates the numbered answer against the available choices, records the response, and displays whether it was correct along with an explanation when provided.
5. The quiz displays progress as the user works through the questions, then shows the final score and percentage. Incorrect answers are listed for review with the user's answer and the correct answer.
6. The CLI asks whether the user wants to play again; confirming restarts the category-selection flow.

## Prerequisites

- Node.js 18 or later (`engines` in `package.json`).
- npm to run the package scripts.

## Installation and setup

```sh
git clone https://github.com/rajkumarepam1/test-app.git
cd test-app
```

No external dependencies are declared, so no dependency installation is required.

## Environment configuration

No environment variables or environment configuration files are specified in the repository.

## Usage

The configured start command is:

```sh
npm start
```

In Windows PowerShell, use `npm.cmd start` if `npm start` is blocked by the script execution policy.

This runs `node index.js`. The CLI prompts for a category and question count, then accepts numbered answers. Press Enter to continue between prompts; after the results, answer `y` at the replay prompt to begin another quiz.

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

- No test files, environment-variable requirements, build configuration, or deployment instructions were found in the listed contents.
- The package description emphasizes JavaScript learning; the included questions also cover Node.js and general programming.
