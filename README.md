# PR build previews for mystmd documentation

1. `.circleci/config.yml`: builds docs in CircleCI.

   After adding that file, activate your repository in CircleCI.

3. `.github/workflows/circleci.yml`: set up a pointer to the CircleCI build artifact

   To use (3), you must add a secret called
   `CIRCLECI_ARTIFACT_REDIRECTOR_TOKEN` as per the
   [`scientific-python/circleci-artifacts-redirector-action`
   instructions](https://github.com/scientific-python/circleci-artifacts-redirector-action?tab=readme-ov-file#example-usage).
   The token is *generated* on CircleCI and *added to* GitHub under
   Settings -> Secrets and variables -> Actions -> Repository secrets.

Now, when you make a PR to your repo, you should see a build preview of the docs.
