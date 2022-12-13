
# DEVOPS TASK

Implementing a Deployment Pipeline using Ansible and GitHub Actions for invocation


## Structure

`.github/workflows` contains the workflow to trigger the playbook

`venvs` contains the requirements.txt files which will create the virtual environments on the target server

`README.md` for documentation

`ansible` the playbook that gets triggered by the workflow

## Details of the implemented task

- The runners are already configured (using *github provided runner*)
- The pipeline sets up the Python, lints the playbook and based on the result runs it
- The pipeline runs on every **push** operation into the main branch
- The operating system is **Ubuntu 20.04**
- The vens will be installed in */opt/python_venvs/*
- The name of the txt files (requirements files) will be the names of the virtual environments
- The pipeline creates multiple venvs, depending on how many **.txt** files are in the repository
- Only execute the installation of packages on changed files

## Installation and usage

Clone the repository, put the appropriate changes into the files, commit and push

```sh
git clone https://github.com/ultramaks/test_task.git
git commit -am 'OUR_CHANGES'
git push
```
Check the [Action](https://github.com/ultramaks/test_task/actions) tab to see how the GitHub action ran the workflow

## Author

- [@Maxim Filippov](https://github.com/ultramaks)
