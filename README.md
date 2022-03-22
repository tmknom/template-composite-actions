# composite-action-template

A template of the Composite Action.

## Getting Started

### Creating a repository from a template

1. Above the file list, click `Use this template`.
2. Use the Owner drop-down menu, and select the account you want to own the repository.
3. Type a name for your repository, and an optional description.
4. Choose a repository visibility.
5. Click `Create repository from template`.

Then, you can generate a new repository with the same directory structure and files as this repository.

### Creating a new Composite Action

Write code for the new Composite Action to the following files:

- [action.yml](/action.yml)
- [test.yml](/.github/workflows/test.yml)

See details: [GitHub documentation](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action).

### Updating the CODEOWNERS

Update [CODEOWNERS](/.github/CODEOWNERS) to define individuals or teams that are responsible for code in a repository.

### Updating the README

Write `README.md` with usage, inputs, outputs, environment variables, `GITHUB_TOKEN` permissions
for your Composite Action.

A template of the `README.md` is under the horizontal rule.

---

## Description

Fix me.

## Usage

```yaml
- uses: your/new-action@v1
  with:
    param: "Update usage"
```

## Inputs

N/A

## Outputs

N/A

## Environment variables

N/A

## `GITHUB_TOKEN` Permissions

N/A

## Developer Guide

### Requirements

- [GNU Make](https://www.gnu.org/software/make/)
- [GitHub CLI](https://cli.github.com/)

### Update documents

Update usage automatically in [README.md](/README.md).

```shell
make docs
```

### Release

#### 1. Bump up to a new version

Run the following command to bump up.

```shell
make bump
```

This command will execute the following steps:

1. Update [VERSION](/VERSION)
2. Update [README.md](/README.md)
3. Commit and push
4. Create a pull request
5. Open the web browser automatically for reviewing pull request

Then review and merge, so the release is ready to go.

#### 2. Create a new GitHub Release

Run the following command to create a new release.

```shell
make release
```

This command will execute the following steps:

1. Push tag
2. Create a new GitHub Release as a draft
3. Open the web browser automatically for editing GitHub Release

#### 3. Publish actions in GitHub Marketplace

Edit to publicize the GitHub Release.

1. Click the edit icon on the right side of the page
2. Edit the release notes
3. Click `Publish release`

Then, the new version are published in GitHub Marketplace.
Finally, we can use the new version! :tada:

## License

Apache 2 Licensed. See LICENSE for full details.
