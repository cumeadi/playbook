## Codebase

> One codebase tracked in revision control, many deploys

**An app is always tracked in a version control system.** We use [git](git.md) to track any changes in the code of a repo.

There is only one codebase per app, but there will be many deploys of the app. We usually have one deploy for the following environment: local, development, staging and production.

The codebase is the same across all deploys, although different versions may be active in each deploy. The most stable release should be deployed on staging and production environment.
