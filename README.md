# Data Science Example

This project demonstrates the setup and usage of a repo for data science projects, specifically showcasing the [DSLP](https://github.com/dslp/dslp/tree/main) branching strategy.

## Table of Contents
- [Data Science Example](#data-science-example)
  - [Table of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Pre-Commit Hooks](#pre-commit-hooks)
  - [DSLP Branching Strategy](#dslp-branching-strategy)
    - [Collaboration Branches](#collaboration-branches)
      - [Main](#main)
      - [Development (Optional)](#development-optional)
    - [Feature and Issue Branches](#feature-and-issue-branches)
    - [Data Branches](#data-branches)
    - [Explore Branches](#explore-branches)
    - [Experiment Branches](#experiment-branches)
    - [Model Branches](#model-branches)
  - [Contributing](#contributing)
  - [License](#license)

## Installation

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/RonMallory/data-science-example.git
   cd data-science-example
   ```

2. **Setup with Poetry**:

   Ensure you have [Poetry](https://python-poetry.org/docs/) installed:

   ```bash
   poetry install
   ```

   This command installs all the necessary dependencies specified in `pyproject.toml`.

## Pre-Commit Hooks

This project uses `pre-commit` to maintain code quality and consistency. The following hooks are in place:

( ... [same as above for hooks] ... )

## DSLP Branching Strategy

### Collaboration Branches

#### Main

The Main branch is the primary collaboration branch, serving as the source of truth for the repo. Everything in Main should be shippable.

#### Development (Optional)

Teams may opt for another collaboration branch, development. If used, development should be the target of pull requests for all features instead of Main. The development branch is then merged to Main as per the team's workflow.

### Feature and Issue Branches

These branches are created for each issue or feature. The naming convention is:

```
[issue-number]-descriptive-branch-name
```

Examples:

- `[issue-number]-calculate-cltv`
- `[issue-number]-custom-risk-scoring-function`

### Data Branches

Used for data ingestion pipelines for known datasets or for creating new datasets. Naming convention:

```
data/[issue-number]-dataset-name
```

Examples:

- `data/[issue-number]-customer-purchase-history`
- `data/[issue-number]-product-prediction-data`

[More on Data Branches Best Practices](#)

### Explore Branches

Used for collaborative exploration. Naming convention:

```
explore/[issue-number]-description-of-exploration
```

Examples:

- `explore/[issue-number]-customer-sales-data`
- `explore/[issue-number]-customers-multiple-accounts`

[More on Explore Branches Best Practices](#)

### Experiment Branches

Used for collaborating on experiments. Naming convention:

```
experiment/[issue-number]-experiment-description
```

Examples:

- `experiment/[issue-number]-sales-forecasts-baseline`
- `experiment/[issue-number]-sales-forecasts-automl`

[More on Experiment Branches Best Practices](#)

### Model Branches

Used to convert successful experiments into deployable models. Naming convention:

```
model/[issue-number]-descriptive-model-name
```

Examples:

- `model/[issue-number]-forecast-customer-sales-baseline`
- `model/[issue-number]-classify-customer-transcripts`

[More on Model Branches Best Practices](#)

## Contributing

1. Fork the project.
2. Create a branch based on the DSLP strategy: `git checkout -b feature/new-feature`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature/new-feature`
5. Submit a pull request against the appropriate DSLP branch.

## License

This project is licensed under the MIT License.
