# template-composite-actions

A template of the Composite Actions, see [Usage](https://github.com/tmknom/template-composite-actions/wiki/Usage).

## Description

Fix me.

## Usage

```yaml
- uses: your/new-action@v1
  with:
    param: "Update usage"
```

<!-- actdocs start -->

## Inputs

N/A

## Outputs

N/A

<!-- actdocs end -->

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
