# Git hooks
This repo contains git hooks for Flutter Application or Plugin Development.

The purpose of this collection to gather some scripts which help to improve the quality of developed applications. I believe in fail-fast philosophy, thus I wrote these hooks.

In my mind, pre-commit hooks can reduce CI costs. Additionally, we will get quick feedback on our changes to the application.

## Description

This repo contains a __pre-commit__ hook for Flutter Application or Plugin development. It cleans the workspace and then runs `analyze` and `test` commands on the project.

## Requirements
The `flutter` command must be available on the `PATH`.

## How to use

Add the contents of this repo to your root project as a git subtree. You can just copy it into `.git/hooks` folder. However, if you do not want to lose the benefits of git, please follow the description below.

```
cd $PROJECT
git remote add flutter-git-hooks https://github.com/warnyul/flutter-git-hooks.git
git subtree add --prefix=git-hooks/ flutter-git-hooks master
```
__Any person who clones your project must symlink the folder into `.git` folder__

```
mv .git/hooks .git/hooks.old && ln -s ../git-hooks .git/hooks
```
## Update hooks
You can update the hooks inside your project if necessary. So, enter your project's folder and pull changes from remote.

```
cd $PROJECT
git remote add flutter-git-hooks https://github.com/warnyul/flutter-git-hooks.git
git fetch flutter-git-hooks master
git subtree pull --prefix=git-hooks/ flutter-git-hooks master
```

# License

    Copyright 2020 Balázs Varga

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
