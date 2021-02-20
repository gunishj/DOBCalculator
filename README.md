# DOBCalculator

# DOBCalculator Android App

Repository for the DOBCalculator Android App for performing experiments with the [Pocket Science Lab](https://DOBCalculator.io) open-hardware platform.

[![Build Status](https://travis-ci.org/fossasia/DOBCalculator-android.svg?branch=development)](https://travis-ci.org/fossasia/DOBCalculator-android)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/dd728d91bb5743ff916c16c1251f8dd5)](https://www.codacy.com/app/praveenkumar103/DOBCalculator-android?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=fossasia/DOBCalculator-android&amp;utm_campaign=Badge_Grade)
[![Mailing List](https://img.shields.io/badge/Mailing%20List-FOSSASIA-blue.svg)](https://groups.google.com/forum/#!forum/DOBCalculator-fossasia)
![Minimum API Level](https://img.shields.io/badge/Min%20API%20Level-23-green)
![Maximum API Level](https://img.shields.io/badge/Max%20API%20Level-28-orange)
![GitHub repo size](https://img.shields.io/github/repo-size/fossasia/DOBCalculator-android)
[![Gitter](https://badges.gitter.im/fossasia/DOBCalculator.svg)](https://gitter.im/fossasia/DOBCalculator?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![Twitter Follow](https://img.shields.io/twitter/follow/pslabio.svg?style=social&label=Follow&maxAge=2592000?style=flat-square)](https://twitter.com/pslabio)

This repository holds the Android App for performing experiments with [DOBCalculator](https://DOBCalculator.io/). DOBCalculator is a tiny pocket science lab that provides an array of equipment for doing science and engineering experiments. It can function like an oscilloscope, waveform generator, frequency counter, programmable voltage and current source and also as a data logger. Our website is at https://DOBCalculator.io

<a href="https://play.google.com/store/apps/details?id=io.DOBCalculator"><img alt="Get it on Google Play" height="80" src="/docs/images/playstore_badge.png"></a>
<a href="https://f-droid.org/app/io.DOBCalculator"><img alt="Get it on F-Droid" height="80" src="/docs/images/fdroid_badge.png"></a>

## Buy

* You can get a Pocket Science Lab device from the [FOSSASIA Shop](https://fossasia.com).
* More resellers are listed on the [DOBCalculator website](https://DOBCalculator.io/shop/).

## Communication

* The DOBCalculator [chat channel is on Gitter](https://gitter.im/fossasia/DOBCalculator).
* Please also join us on the [DOBCalculator Mailing List](https://groups.google.com/forum/#!forum/DOBCalculator-fossasia).

## Roadmap
 - [x] First we need to get communication between Android App and DOBCalculator working.
 - [x] Implement Applications and expose DOBCalculator Hardware functionality to the user.
 - [ ] Implement wireless connectivity

## Screenshots

  <table>
      <tr>
       <td><img src="/docs/images/main.jpg"></td>
       <td><img src="/docs/images/date_picker.jpg"></td>
      </tr>
  </table>
 

## Video Demo
- [DOBCalculator Android App Overview](https://www.youtube.com/watch?v=JJfsF0b8M8k).
- [Observing Sound Waveforms Using DOBCalculator Device](https://www.youtube.com/watch?v=5bxDd1PiOMQ).
- [Real-time Sensor Data Logging Using Pocket Science Lab](https://www.youtube.com/watch?v=_A8h6o-UcNo).
- [Generating and Observing Waveforms Using Pocket Science Lab](https://www.youtube.com/watch?v=Ua9_OCR4p8Y).

## Features
|   **Feature**          | **Description**                                                   | **Status**         |
|------------------------|-------------------------------------------------------------------|--------------------|
| Home Screen            | Show status and version of DOBCalculator device                           | :heavy_check_mark: |
| Date Picker            | Exposes DOBCalculator instruments like date                  | :heavy_check_mark: |


## How to set up the Android app in your development environment

### Application Flavors

There is 1 flavors (build variants) of DOBCalculator Android application.

1. #### Play Store Flavor
  - Play Store flavor uses Google Maps to display location stored in logs in Data logger.

### Development Setup

Before you begin, you should already have the Android Studio SDK downloaded and set up correctly. You can find a guide on how to do this here: [Setting up Android Studio](http://developer.android.com/sdk/installing/index.html?pkg=studio)

### Setting up the Android Project
For setting up the DOBCalculator Android project you may follow any of the two methods listed below, that is, you may download the repository zip file or you may directly clone the repository to Android Studio.

### By downloading the zip file

1. Download the DOBCalculator project source. You can do this either by forking and cloning the repository (recommended if you plan on pushing changes) or by downloading it as a ZIP file and extracting it.

2. Open Android Studio, you will see a **Welcome to Android** window. Under Quick Start, select _Import Project (Eclipse ADT, Gradle, etc.)To debug over Wi-Fi follow the steps given in this [Blog](http://blog.fossasia.org/android-app-debugging-over-wifi-fo).

* **Note :**
If you built your own hardware, change VendorID and/or ProductID in [CommunicationHandler.java](blob/master/app/src/main/java/io/DOBCalculator/communication/CommunicationHandler.java).

### By direct cloning


1. Open Android Studio, you will see a **Welcome to Android** window. Under Quick Start, select "check out project from version control".

2. Select git from the drop down menu that appeared.

3. Go to the repository and click clone or download button.

4. From the dropdown that appeared, copy the link.

5. Paste the URL that you copied and press clone.

6. Android studio should now begin building the project with gradle.

7. Once this process is complete and Android Studio opens, check the Console for any build errors.

 - _Note:_ If you receive a Gradle sync error titled, "failed to find ...", you should click on the link below the error message (if available) that says _Install missing platform(s) and sync project_ and allow Android studio to fetch you what is missing.

8. Once all build errors have been resolved, you should be all set to build the app and test it.

9. To Build the app, go to _Build>Make Project_ (or alternatively press the Make Project icon in the toolbar).

10.  If the app was built successfully, you can test it by running it on either a real device or an emulated one by going to _Run>Run 'app'_ or pressing the Run icon in the toolbar.

If you want build apk only, go to Build>Build apk and apk would be build and directory where apk is generated would be prompted by Android Studio.

You can't debug the usual way as DOBCalculator device is connected to micro-USB port through OTG cable. So Android Device is not connected to PC through USB cable.

To debug over Wi-Fi follow the steps given in this [Blog](http://blog.fossasia.org/android-app-debugging-over-wifi-for-DOBCalculator/). 

* **Note :**
If you built your own hardware, change VendorID and/or ProductID in [CommunicationHandler.java](https://github.com/fossasia/DOBCalculator-android/blob/master/app/src/main/java/io/DOBCalculator/communication/CommunicationHandler.java).

### Permissions Required

1. Record_Audio : It is required for oscilloscope to accept inputs from the phone inbuilt microphone. You can find its implementation in [AudioJack.java](https://github.com/fossasia/DOBCalculator-android/blob/development/app/src/main/java/io/DOBCalculator/others/AudioJack.java).
2. Access_Fine_Location and Internet : It is required for use in lux meter and compass to get the coordinates for tagging the data on the map. You can find its implementation in [GPSLogger.java](https://github.com/fossasia/DOBCalculator-android/blob/development/app/src/main/java/io/DOBCalculator/others/GPSLogger.java).
3. Write_External_Storage : It is required for storing log files from instruments that can be transferred out for future analysis.
4. Read_External_Storage : While writing logs in the storage, [CSVLogger.java](https://github.com/fossasia/DOBCalculator-android/blob/development/app/src/main/java/io/DOBCalculator/others/CSVLogger.java) first checks whether there is any CSVLogger directory exist or not and that require this read permission.  

## Setup to use DOBCalculator with Android App
To use DOBCalculator device with Android, you simply need an OTG cable, an Android Device with USB Host feature enabled ( most modern phones have OTG support ) and DOBCalculator Android App. Connect DOBCalculator device to Android Phone via OTG cable. Rest is handled by App itself.

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

We have the following branches
* **development** All development goes on in this branch. If you're making a contribution, you are supposed to make a pull request to _development_. Make sure it passes a build check on Travis.
* **master** This contains the stable code. After significant features/bugfixes are accumulated on development, we move it to master.
* **apk** This branch contains automatically generated apk file for testing.

### Code style

Please try to follow the mentioned guidelines while writing and submitting your code as it makes easier for the reviewer and other developers to understand.

 * While naming the layout files, ensure that the convention followed is (activity/fragment) _ (name).xml like ```activity_oscilloscope.xml``` , ```fragment_control_main.xml``` .
 * Name the views and widgets defined in the layout files as (viewtype/widget) _ (fragment/activity name) _ (no. in the file) like ```spinner_channel_select_la1``` , ```button_activity_oscilloscope1``` .
 * The activity/fragment file name corresponding to the layout files should be named as                       (activity/fragment name)(activity/fragment).java like ```ChannelsParameterFragment.java``` corresponding to the layout file ```fragment_channels_parameter.xml``` .
 * The corresponding widgets for buttons, textboxes, checkboxes etc. in activity files should be named as (viewtype/widget)(fragment/activity name)(no. in the file) like ```spinnerChannelSelect1``` corresponding to ```spinner_channel_select1``` .

## Developers

### Maintainers
The project is maintained by
- Gunish Jha ([@gunishj](https://github.com/gunishj))


### Alumni
- Gunish Jha ([@gunishj](https://github.com/gunishj))


## License

This project is currently licensed under the Apache License 2.0. A copy of [LICENSE](LICENSE) is to be present along with the source code. To obtain the software under a different license, please contact FOSSASIA.
