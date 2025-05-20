# conftest-demo
Hi and welcome to this demonstration of the Open Policy Agent for use to audit Ansible code.

## How does it work?
We have a CI pipeline defined in .github/workflows/ci.yml
This pipeline does three main steps.

1. Installs conftest
2. Fetches the OPA policy from https://github.com/mglantz/conftest-policy and puts it in a directory called policy.
3. Runs 'conftest test' on all the playbooks found in the repository.

## What does this accomplish?
Before any pull requests are merged, and at the point of merges / commits to main, we run our conftest. This can prevent Ansible code from being merged, if it breaks any policy we have defined.

