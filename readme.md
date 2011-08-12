# Gir CMS

Gir CMS aims to be as lightweight and easy as possible while still maintaining a
certain amount of extensibility. It is named after the Invader Zim character
because of the authors obsessiveness with both the cartoon character and this
project.

While [HTML5 Boilerplate][html5boilerplate] is the basis for the template the
project is designed to be dynamic enough to (with a little effort) serve most
text based formats. You are also able to code in any standards you want.

## Requirements

* Apache 2.2+ w/mod_rewrite
* PHP 5+

## Installation

1. Upload the files, make sure the **cache** directory and **files/errors.log**
are writable.

2. Set up the **files/config.php** file.

3. Check/Change RewriteBase in the root **.htaccess** file.

4. Setup or delete the favicon in **files/extras**.

5. Setup or delete the humans.txt and robots.txt in **files/extras**.


## Changelog (for this Fork)

* Added a slightly adjusted variant of [Remarkdown CSS][remarkdowncss] by Florent Verschelde as default Style

* Removed references to Google's CDN (Modernizr + jQuery)


[html5boilerplate]: http://html5boilerplate.com
[remarkdowncss]: http://covertprestige.info/css/remarkdown/