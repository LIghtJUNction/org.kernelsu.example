# KernelSU Modules Repo Example

[中文](docs/README_CN.md) | **English**

---

## Important Notes

- You may only upload your own modules. If you have explicit permission from a developer to upload their module, it is fine as well, but both of you need to keep in mind that the uploader's name will be mentioned as author.
- Modules must be compliant with the law and must not act in malicious ways. The operator of this site will not take any responsibility (or give support) for uploaded modules.
- Only default branches will be processed.

## Module Release Requirements

### Publishing Immutable Releases

To enhance security, this organization has enabled the **Immutable Releases** feature. You will not be able to move or delete Git tags, or modify or delete release assets. Additionally, creating an immutable release automatically generates a release attestation, which is a cryptographically verifiable release record containing the release tag, commit SHA, and release assets.

> [!NOTE]
> Immutable releases include protection against repository resurrection attacks. Even if the repository is deleted and a new repository with the same name is created, tags associated with immutable releases from the original repository cannot be reused.

## Module Information

### Module Name *

The Description of repository details.

### Module ID *

The repository name.

> The id of the module - has to be the same for all versions!

### Meta Module *

The `metamodule` field in `module.json` file.

> Set to `true` if this is a metamodule, otherwise set to `false`.

### Summary

The `summary` field in `module.json` file.

> A brief description of the module, will be displayed outside the list, no formatting is supported.
> Leave blank to use trimmed value of full text as the summary.

### Description *

Contents in `README.md` file.

### Support/Discussion URL *

The Website of repository details.

> Link to a site where users can get support for and discuss about your module. (e.g. your github issue)

### Source Code URL

The `sourceUrl` field in `module.json` file.

> Link to the source code of your module if you published it.

### Additional Authors

The `additionalAuthors` field in `module.json` file.

| Field | Type | Description | Optional |
| ----- | ---- | ----------- | -------- |
| `type` | String | "add" or "remove" | No |
| `name` | String | The name of author | No |
| `link` | String | The link of author | Yes |

Example in `module.json`:
```json
{
  "additionalAuthors": [
    {
      "type": "add",
      "name": "tiann",
      "link": "https://github.com/tiann"
    },
    {
      "type": "add",
      "name": "Ylarod",
      "link": "https://github.com/Ylarod"
    },
    {
      "type": "add",
      "name": "KernelSU-Bot"
    },
    {
      "type": "remove",
      "name": "someoneInContributorsWillRemove"
    }
  ]
}
```

> In case you have developed the module together with somebody else, but they don't have a GitHub account. You can write their names and links into the `module.json` file.
> All `Outside Collaborators` in this repository will be added by default.

### Visibility

If you want to hide the module:
- **Hide from repository**: Change repository to private in Repository Settings.

## Versions

We use GitHub releases as a version update.

Version Name and Version Code will be parsed from `module.prop` in the module within release assets.

### Version Name *

The `version` field in `module.prop`.

> This is the human-readable version number.

### Version Code *

The `versionCode` field in `module.prop`.

> The technical version, used when checking for updates. Newer versions always need to have a higher number than previous versions.

### Release Type *

Set via the `This is a pre-release` checkbox.

| Type | GitHub Release Type |
| ---- | ------------------- |
| Stable (low risk of bugs) | Release |
| Beta (some bugs to be expected) | Pre-release |

> Classification how risky it is for users to install this version. By default, only stable versions will be shown.

### Changes

The Release Description.

> A list of changes (new features, bugfixes) in this particular version.
