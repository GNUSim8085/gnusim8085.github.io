---
layout: default
title: Contribute
---
# How to contribute

### Code (patches)
You can submit patches for bug fixes or feature implementations. If you come up with patch for some new functionality then please log a 'wishlist' bug first. Check the existing list of [bugs](https://github.com/GNUSim8085/GNUSim8085/issues)

### Documentation
Our application does not have any end user documentation yet. The git master branch has basic framework for generating user documentation in HTML format. If you have good autotools skills you can help in achieving this goal. Once we have figured out how to ship documentation in cross platform manner you can contribute the actual content.
Meanwhile we distribute some sample programs with our application to help users learn assembly programming. You can always contribute your own programs.

### Testing
As with most Free software applications ours is mainly tested by user community. Please test the application as much as possible and file any bugs you find. You can focus the testing on a specific platform (ex. Windows) or specific area of application (ex. memory instructions).
Following are some areas where more testing is needed:

* Printing support on Windows - Currently printing does not work as expected on Windows. This will be fixed in version 1.3.8. Any feedback from Windows users will be great.

### Translations
[![Translation Status](https://hosted.weblate.org/widgets/gnusim8085/-/287x66-black.png)](https://hosted.weblate.org/engage/gnusim8085/?utm_source=widget){:target="_blank"}

Last release is translated in 12 languages. Some of them are incomplete. You can help us complete translations or add a new one using weblate. Click above link for opening the weblate page.

{::comment}
### Porting
Even though our application was originally written for Linux distributions it has been ported to Windows now. We are interested in porting the application to other operating systems such as Mac OS X but do not have sufficient resources for this. You can help in this regard. Please get in touch with us on developers mailing list (list name to be confirmed).
{:/comment}
