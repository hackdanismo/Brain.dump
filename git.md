# Git

+ [GitHub](#github)
  + [Profile](#profile)
  + [GitHub Actions](#github-actions)

## GitHub

### Profile
To add a profile `README` on the homepage of the `GitHub account`:

+ Create a repo with the same name as the account. For example, if the `GitHub` account is named `hackdanismo`, create a repo also named `hackdanismo`. This should be `public`.
+ Add a `README.md` file into this repo. This will be the `README` that appears on the main part of the account page.

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
