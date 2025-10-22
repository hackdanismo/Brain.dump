# Git

+ [GitHub](#github)
  + [GitHub Actions](#github-actions)

## GitHub

### GitHub Actions
When creating a new `GitHub` repo with a `README.md` file, GitHub only creates the markdown file and does not create a `.github` directory. Optionally, a licence and a `.gitignore` file can be added. To create the `.github` directory containing a `workflows` folder, where `GitHub Actions` can be created:

```shell
$ mkdir -p .github/workflows
```

When a commit is made to a repo, GitHub itself will create the `.github` directory/folder.

Within this `workflows` folder, create a `.yml` file (e.g. `hello.yml`). This is the file for `GitHub Actions`. All `GitHub Actions` created within a repo are found in the `Actions` tab.

+ This action triggers on every push to any branch.
+ Runs a single job on the latest Ubuntu runner.
+ Checks out the necessary repository (standard first step).
+ Prints: `Hello, World!` to the `GitHub Actions` log.

```yml
name: Hello World

on: [push]

jobs:
  say-hello:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Say hello
        run: echo "Hello, world!"
```

The settings in the repo need to be updated to publish to `GitHub Pages`.
