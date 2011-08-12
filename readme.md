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

* Added a slightly adjusted variant of [Remarkdown CSS][remarkdowncss] by Florent Verschelde as default style

* Removed references to Google's CDN (Modernizr + jQuery)


## Gir-CMS as repository-based wiki (Example: Git)

Gir-CMS works great as repository-based wiki. 

### Requirements and Setup

You need a repository for all text-files on the same server as your Gir-CMS installation. Every contributor to the wiki needs write access to this repository. If you don't have such a repository yet, have a look at [Gitosis][gitosis] or at [Gitolite][gitolite] (which seems better maintained).

If you already have this repository the setup is straight forward:

Add a post-receive git-hook to the repository on the server `/path/to/repository/.git/hooks/post-receive` with the following content:

<pre>
#!/bin/sh  
GIT_WORK_TREE=/path/to/gir-cms/files/pages git checkout -f
</pre>

After every push to the repository is "deployed" directly to the "file-database" of Gir-CMS.

**Attention:** If you already have content in this folder make sure to backup it and add these files to the repository *before* deploying the first time automatically.

[html5boilerplate]: http://html5boilerplate.com
[remarkdowncss]: http://covertprestige.info/css/remarkdown/
[gitosis]: http://eagain.net/gitweb/?p=gitosis.git
[gitolite]: https://github.com/sitaramc/gitolite
