---
name: 'Run-cache'
match: ['run-cache']
tooltip: >-
  A logging and replication mechanism of DVC for experiment runs. It maintains
  history of experiment runs without checking each result into Git.
  [📖](/doc/user-guide/concepts/run-cache)
---

# Run-Cache

Run-cache allows experiments to be run without being tied to the Git commits.
DVC can store all the experiment history in run-cache, basically replicating the
information in `dvc.lock` file and can report (or plot) the results of that
experiment later.

Internally DVC run-cache is a log of stages that have been run in the project.
It's comprised of `dvc.lock` file backups, identified as combinations of
dependencies, commands, and outputs that correspond to each other. `dvc repro`
and `dvc run` populate and reutilize the run-cache.

## Further Reading

- [Run-cache](/doc/user-guide/project-structure/internal-files#run-cache) in
  project structure.
- `dvc run` command reference.
- `dvc repro` command reference.
