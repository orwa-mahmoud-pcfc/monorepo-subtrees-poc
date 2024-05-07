# Monorepo Project POC

This monorepo integrates multiple projects (`repo1` and `repo2`) using Git subtrees. This setup allows for the independent development of each project while still maintaining a unified repository structure.


## Repository Structure

- `/repo1`: Contains the Project 1 codebase, managed as a subtree.
- `/repo2`: Contains the Project 2 codebase, managed as a subtree.

## Cloning the Repository

To clone this monorepo, use the following command:

```bash
git clone https://github.com/orwa-mahmoud-pcfc/monorepo-subtrees-poc.git
```

## Managing Subtree Updates

### Pulling Changes from Subtrees

To incorporate updates from the original repositories of `repo1` or `repo2` into the monorepo, follow these commands for each subtree:

#### For `repo1`
```bash
git subtree pull --prefix=repo1 https://github.com/orwa-mahmoud-pcfc/repo1.git main
```
#### For `repo2`
```bash
git subtree pull --prefix=repo2 https://github.com/orwa-mahmoud-pcfc/repo2.git main
```

- The `--prefix` option specifies the local path to the subtree.
- The repository URL: the actual URL of the subtree's original repository.
- `main` indicates the branch from which to pull.

### Pushing Changes to Subtrees

If you have made changes within the subtree directories in the monorepo and need to push these back to the original repositories, use:

#### For `repo1`
```bash
git subtree push --prefix=repo1 https://github.com/orwa-mahmoud-pcfc/repo1.git main
```
#### For `repo2`
```bash
git subtree push --prefix=repo2 https://github.com/orwa-mahmoud-pcfc/repo2.git main
```

- Ensure the `--prefix` correctly points to the directory of your subtree.
- The repository URL: the actual URL of the subtree's original repository.
- `main` is the branch you are pushing to.


