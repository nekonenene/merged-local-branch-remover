# git-branch-delete-merged

This cli app deletes local branches that have been merged **also "Squash and merge"**.

## Installation

```sh
go install github.com/nekonenene/git-branch-delete-merged@v1
```

## Usage

### General usage

If you want to delete a branch that has merged into the `main` branch:

```sh
git-branch-delete-merged --base-branch main
```

And if the branch to delete exists, you will get a prompt like this:

```
Target branches: [dev1]

Are you sure to delete 'dev1' branch? [y|n|l]:
```

Please type one and press enter.

* **y**: yes
* **n**: no
* **l**: show latest 3 git logs

### Skip prompt

If you want to delete all merged branches without confirmation, `--yes` option will be useful.

```sh
git-branch-delete-merged --base-branch main --yes
```


## Thank you

[not-an-aardvark/git-delete-squashed](https://github.com/not-an-aardvark/git-delete-squashed) is the reference code that helps finding branches which has squashed and merged.
