# Porting notes

The committed Cargo.lock (format v3) predates parts of Cargo.toml; modern cargo re-resolves
dependencies on every fresh build and would rewrite the lockfile. compile.sh builds with the
re-resolved set (the lockfile itself is left untouched in the repo). Two help-text goldens are
sensitive to the resolved clap version and are excluded in local_ignored_tests.txt.
