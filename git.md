# How to write meaningful commit messages

1. Use the imperative mood in the subject line
1. Limit the subject line to 50 characters
1. Capitalize the subject line
1. Do not end the subject line with a period
1. Separate subject from body with a blank line
1. Use the body to explain what and why
1. Wrap the body at 72 characters

This note is based on a [blog post](https://chris.beams.io/posts/git-commit)
by Chris Beams.

# Atomic commits
An “atomic commit" consists of changes related to one task, one logical unit.

## Atomic Approach
* Commit each fix or task as a separate change
* Only commit when a block of work is complete
* Commit each change separately

## Benefits
* Easy to roll back without affecting other changes
* Easy to make other changes on the fly
* Easy to merge features to other branches
* Supports a structured programming workflow

For more details read the
[blog post](https://www.freshconsulting.com/atomic-commits) by Sean Patterson.
