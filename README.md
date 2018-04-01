# Project 7 - WordPress Pentesting

Time spent: 12 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Stored Cross-Site Scripting (XSS) --Hover
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: <img src="https://github.com/nicoleio712/Week7/blob/master/XSS_Hover_Over_Attack.gif" width="800">
  - [ ] Steps to recreate: Go to the Klikki website and copy the longer line of XSS code (a link alert). Logged in as admin, create a new post. Switch the mode from visual to text and delete any text there already. Paste the attack code line in the text box and publish the post. Upon viewing the post, hover over the link and the alert will pop up.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) Unauthenticated Stored Cross-Site Scripting (XSS) --Long Comment
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: <img src="https://github.com/nicoleio712/Week7/blob/master/XSS_Long_Post_Attack.gif" width="800">
  - [ ] Steps to recreate: Go to the Klikki website to copy the documented line of attack XSS code (a 'hello world' alert). Log out of admin account and visit the Wordpress site as a regular user. Paste the attack code in a comment on one of the posts. Google a 64KB text file and copy all of its contents. Paste the content in the space where the "AAA (64KB) AAA..." is in the line of code. Post the comment.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) Authenticated Stored Cross-Site Scripting via Image Filename
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough: <img src="https://github.com/nicoleio712/Week7/blob/master/XSS_attack_WP_real.gif" width="800">
  - [ ] Steps to recreate: Logged in as admin, go to the Media section and add a new image. Once the image has uploaded, click on it and change the image title to: "<script> alert('attack') </script>". View the attachment page afterwards and note the alert has popped up.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
4. (Optional) Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: <img src="https://github.com/nicoleio712/Week7/blob/master/XSS_Youtube_attack.gif" width="800">
  - [ ] Steps to recreate: Logged in as admin, create a new post. Copy and paste up until the "v=" part of any YouTube video url. Type <script>alert('attack')</script> after the "v=". Highlight the url and press the linking icon. Attempt to link the resulting url.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

none

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Challenges were mostly in figuring out in which sequence to administed the exploits. Looking in old documentation was dense at times, but actually the bugs were fairly easy to spot once I had a small aresenal of techniques to try.

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

