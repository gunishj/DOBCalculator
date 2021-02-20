# DOBCalculator Android App

Repository for the DOBCalculator Android App for Calculating your age in number of days.

[![Build Status](https://travis-ci.org/fossasia/DOBCalculator-android.svg?branch=development)](https://travis-ci.org/fossasia/DOBCalculator-android)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/dd728d91bb5743ff916c16c1251f8dd5)](https://www.codacy.com/app/praveenkumar103/DOBCalculator-android?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=fossasia/DOBCalculator-android&amp;utm_campaign=Badge_Grade)
[![Mailing List](https://img.shields.io/badge/Mailing%20List-FOSSASIA-blue.svg)](https://groups.google.com/forum/#!forum/DOBCalculator-fossasia)
![Minimum API Level](https://img.shields.io/badge/Min%20API%20Level-23-green)
![Maximum API Level](https://img.shields.io/badge/Max%20API%20Level-28-orange)
![GitHub repo size](https://img.shields.io/github/repo-size/fossasia/DOBCalculator-android)
[![Gitter](https://badges.gitter.im/fossasia/DOBCalculator.svg)](https://gitter.im/fossasia/DOBCalculator?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Twitter Follow](https://img.shields.io/twitter/follow/pslabio.svg?style=social&label=Follow&maxAge=2592000?style=flat-square)](https://twitter.com/pslabio)

This repository holds the Android App for performing experiments with [DOBCalculator](https://DOBCalculator.io/). DOBCalculator is a tiny pocket science lab that provides an array of equipment for doing science and engineering experiments. It can function like an oscilloscope, waveform generator, frequency counter, programmable voltage and current source and also as a data logger. Our website is at https://DOBCalculator.io

## Buy

* You can get a DOBCalculator for free from the [Gunish's Shop](https://fossasia.com).
* More resellers are listed on the [DOBCalculator website](https://DOBCalculator.io/shop/).

## Communication

* The DOBCalculator [chat channel on Gitter is not yet set up](https://gitter.im/fossasia/DOBCalculator).
* Please also join us on the [DOBCalculator Mailing List hasn't been created](https://groups.google.com/forum/#!forum/DOBCalculator-fossasia).

## Roadmap
 - [x] First we need to get communication between Android App and DOBCalculator working.
 - [x] Select your date of birth.
 - [ ] wireless connectivity is not needed

## Screenshots

  <table>
      <tr>
       <td><img src="/docs/images/main.jpg"></td>
       <td><img src="/docs/images/date_picker.jpg"></td>
      </tr>
  </table>
 

## Video Demo
- [Vedio set up is not done Right now](https://www.youtube.com/watch?v=JJfsF0b8M8k).

## Features
|   **Feature**          | **Description**                                                   | **Status**         |
|------------------------|-------------------------------------------------------------------|--------------------|
| Home Screen            | Show status and version of DOBCalculator device                           | :heavy_check_mark: |
| Date Picker            | Exposes DOBCalculator instruments like date                  | :heavy_check_mark: |



## Contributions Best Practices

### Code practices

Please help us follow the best practice to make it easy for the reviewer as well as the contributor. We want to focus on the code quality more than on managing pull request ethics.

 * Single commit per pull request.
 * Reference the issue numbers in the commit message. Follow the pattern ``` Fixes #<issue number> <commit message>```
 * Follow uniform design practices. The design language must be consistent throughout the app.
 * The pull request will not get merged until and unless the commits are squashed. In case there are multiple commits on the PR, the commit author needs to squash them and not the maintainers cherrypicking and merging squashes.
 * If the PR is related to any front end change, please attach relevant screenshots in the pull request description.

#### How to `git squash`?

As a tip for new developers those who struggle with squashing commits into one, multiple commits may appear in your pull request mostly due to following reasons.

 * Intentionally adding multiple commit messages after each change without just `git add`ing.
 * Updating the current branch with the remote so a merge commit takes place.

Despite any reason, follow the steps given below to squash all commits into one adhering to our best practices.

 * Setup remote to upstream branch if not set before

`$ git remote add upstream https://github.com/fossasia/DOBCalculator-android.git`

 * Check into the branch related to the pull request

`$ git checkout <branch-name>`

 * Perform a soft reset to retain the changes while removing all the commit details

`$ git reset --soft upstream/development`

 * Add files to the staging area

`$ git add <file paths or "." to add everything>`

 * Create a new commit with a proper message following commit message guidelines

`$ git commit -m "tag: commit message"`

 * If you have already made a pull request

`$ git push -f origin <branch-name>`

### Branch Policy

We will be having the following branches in sometime
* **development** All development goes on in this branch. If you're making a contribution, you are supposed to make a pull request to _development_. Make sure it passes a build check on Travis.
* **master** This contains the stable code. After significant features/bugfixes are accumulated on development, we move it to master.
* **apk** This branch contains automatically generated apk file for testing.

### Code style

Please try to follow the mentioned guidelines while writing and submitting your code as it makes easier for the reviewer and other developers to understand.

 * While naming the layout files, ensure that the naming convention is followed .
 
## Developers

### Maintainers
The project is maintained by
- Gunish Jha ([@gunishj](https://github.com/gunishj))


### Alumni
- Gunish Jha ([@gunishj](https://github.com/gunishj))


## License

This project is currently licensed under the Apache License 2.0. A copy of [LICENSE](LICENSE) is to be present along with the source code. To obtain the software under a different license, please contact Gunish.
