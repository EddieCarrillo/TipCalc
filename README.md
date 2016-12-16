# Pre-work - *Tippy*

**Tippy** is a tip calculator application for iOS.

Submitted by: **Eduardo Cariillo**

Time spent: **X** hours spent in total

## User Stories

The following **required** functionality is complete:

* [x] User can enter a bill amount, choose a tip percentage, and see the tip and total values.
* [x] Settings page to change the default tip percentage.

The following **optional** features are implemented:
* [x] UI animations
* [x] Remembering the bill amount across app restarts (if <10mins)
* [x] Using locale-specific currency and currency thousands separators.
* [x] Making sure the keyboard is always visible and the bill amount is always the first responder. This way the user doesn't have to tap anywhere to use this app. Just launch the app and start typing.

The following **additional** features are implemented:

- [x] Light, Dark, and Blue color themes

## Video Walkthrough 

Here's a walkthrough of implemented user stories:

<img src='http://i.imgur.com/link/to/your/gif/file.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />

GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while building the app.
I had an annoying bug when I tried to use UserDefaults to save the bill
across app restarts it would not save. But when I used to UserDefaults to
save the index of the default index it would be fine. So, I was confused and
I realized I did not call synchronize after saving the bill. After putting
in the synchronize it still did not save the bill value. So after a painful few hours I figured that I was making the call to calculateTip in my viewWillLoad lifecycle function and it always returned a 0 b/c the view never finshed being created an always returned an invalid string and then 0. So moving the call the viewDidAppear fixed the bug.
## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.