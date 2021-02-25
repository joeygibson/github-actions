# github-actions

These are reusable [Github Action](https://github.com/features/actions) script for building projects in various langauges, for Linux, macOS, and Windows.

The `build.yml` file is run whenever a `commit` happens. It builds and tests the project

The `release.yml` file is run when a Git tag is present. It builds just like `build.yml`, but when done, it will create a release, and upload the artifacts.

These scripts work for me, though I don't claim they are perfect. If you have suggestions to make them better, please send me a pull request.

## Languages supported

* Rust
* Go
* Kotlin/Java using Gradle
* Kotlin/Java using Maven

## Using

1. In your project, run `mkdir -p .github/workflows` to create the main workflow directory
2. Copy the `.yml` files for your project's language to `.github/workflows`
3. If your language has a `scripts` directory in it, then run `mkdir scripts` and copy the `scripts/` files into it.
4. Change any instance of `joeygibson` to your Github username.
5. Commit your changes, and check the `Actions` tab in the Github UI for your project

Note: You may need to adjust the scripts depending on whether you use `master`, or the new `main` branch that Github is moving to.
