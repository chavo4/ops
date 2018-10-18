[![Build Status](https://travis-ci.org/chavo4/ops.svg?branch=master)](https://travis-ci.org/chavo4/ops)

# Prerequisite:
Make a [GitHub token](https://github.com/settings/tokens) and export it as follow:
```
export  TF_VAR_github_token=<Your GitHub token>
```
Be sure you have installed "rbenv", if not follow below:
```
brew install rbenv
rbenv install 2.3.1
rbenv local 2.3.1
rbenv versions //to check if version is 2.3.1
```
add the following to your ~/.bash_profile:

```
eval "$(rbenv init -)"
true
export PATH="$HOME/.rbenv/bin:$PATH"
```

source ~/.bash_profile

**Usage example:**

1.  Fork the copy of chavo4/ops - clone it
- Or
2.  Download a ZIP with following link:
```
https://github.com/chavo4/ops/archive/master.zip
```
 - Or open it with GitHub Desktop:
```
https://github.com/chavo4/ops.git
```
3. Than you can test it with following commands:
```
kitchen list
kitchen converge
kitchen verify
```
The result should be as follow:

```

  ✔  check_website: http GET on https://github.com/chavo4/example-kitchen
     ✔  http GET on https://github.com/chavo4/example-kitchen status should cmp == 200
     ✔  http GET on https://github.com/chavo4/example-kitchen body should match "My awesome codebase"


Profile Summary: 1 successful control, 0 control failures, 0 controls skipped
Test Summary: 2 successful, 0 failures, 0 skipped

```

4. Destroy it after the test:
```
kitchen destroy
```
