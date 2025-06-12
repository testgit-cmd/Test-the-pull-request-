#!/bin/bash

# List of branches to create PRs from
branches=("feature-1" "feature-2" "feature-3")

# Target base branch
base_branch="main"

for branch in "${branches[@]}"
do
  gh pr create --base "$base_branch" --head "$branch" --title "PR from $branch" --body "Auto-created pull request from $branch"
done
